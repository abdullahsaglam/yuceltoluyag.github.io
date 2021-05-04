---
layout: post
title: Linuxta UEFI windows 10 format usb oluşturma resimli anlatım
description: Linuxta UEFI windows 10 format usb oluşturma resimli anlatım
image: "/uploads/linux_windows10_uefi.jpeg"
comments: true
edit_url: true
category: linux
tags: [linux, windows10]
---

Windowsan linuxa geçerken rufus benzeri programlar ile programlar ile kurulumu sorunsuz yapabilmekteyiz. Ancak linux tarafında wine kullanılsa dahi rufus programının düzgün çalıştığı söylenemez. Linux tarafında çok çeşitli uygulamalar mevcut fakat yeni kullanıcılar kullanmakta zorluklar çekmektedir.
<!-- excerpt separator -->
1.  [Windows10.iso](https://www.microsoft.com/tr-tr/software-download/windows10) dosyanız yoksa edinin.
2.  [WoeUSB programını yüklüyoruz.](https://github.com/slacka/WoeUSB)

```
sudo add-apt-repository ppa:nilarimogard/webupd8
sudo apt update
sudo apt install woeusb
```

USB diskimizi formatlıyoruz.
![linux_windows10_uefi](/uploads/linux_windows10_uefi.jpeg)

![linux_windows10_uefi_format](/uploads/linux_windows10_uefi_format.jpeg)

Burada dikkat etmemiz gereken nokta **USB diskimizi muhakkak NTFS formatında biçimlendirmeliyiz.Aksi halde ekranda ki gibi hata alacaksınız.**

![linux_windows10_uefi_format_error](/uploads/linux_windows10_uefi_format_error.jpeg)

**Woeusb** programını artık açabiliriz.İlk yere iso dosyasımızı seçiyoruz. Altaki ekranda hazırladığımız usb diskimiz seçili olmalıdır.![linux_windows10_uefi_disk](/uploads/linux_windows10_uefi_disk.jpeg)

İşlem tamamlandıktan sonra bilgisayarınızı yeniden başlatın ve boot edin.![linux_windows10_uefi_boot](/uploads/linux_windows10_uefi_boot.jpeg)


![linux_windows10_uefi_boot_2](/uploads/linux_windows10_uefi_boot_2.jpeg)

Gördüğünüz gibi linuxta windows 10 format usbsi hazırlamış olduk,hemde uefi :) Kişisel görüşüm, linuxa yeni başladıysanız birden bire geçmeyin ,afallayabilirsiniz. Şu yazımı okumadıysanız okumanızı tavsiye ederim => [Yeni Başlayanlar için Linux](https://yuceltoluyag.github.io/yeni-baslayanlar-hangi-linux-surumunu/)
