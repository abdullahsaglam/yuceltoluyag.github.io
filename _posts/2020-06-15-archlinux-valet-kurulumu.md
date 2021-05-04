---
layout: post
title: Arch Linux Laravel Valet Kurulumu
description: Valet Linux , Linux minimalistleri için bir Laravel geliştirme ortamıdır. Vagrant yok, /etc/hostsdosya yok . Yerel tünelleri kullanarak sitelerinizi herkese açık olarak da paylaşabilirsiniz. Evet, biz de seviyoruz.
image: "/uploads/laravel-valet-kurulumu-linux.jpeg"
category: linux
tags: [linux, laravel]
series: "archlampp"
comments: true
edit_url: true
---
![laravel-valet-kurulumu](/uploads/laravel-valet-kurulumu-linux.jpeg)

# Merhaba

Valet Linux , minimalist geliştirme ortamını sevenler için Laravel geliştirme ortamıdır. [Vagrant](https://yuceltoluyag.github.io/virtualbox-vagrant-laravel-arch-linux/) yok, `/etc/hosts`ayarlamak  yok . Yerel tünelleri (Ngrok vb gibi) kullanarak sitelerinizi herkese açık olarak da paylaşabilirsiniz.
<!-- excerpt separator -->
Vale Linux sisteminizi, makineniz başladığında Nginx'i arka planda çalışacak şekilde yapılandırır. Ardından, **DnsMasq** kullanarak Valet `*.test`, makinenizde ki siteleri proxy ile tünel  oluşturup ilgili domaine yönlendirmesini sağlar.

Başka bir deyişle, kabaca 7mb RAM kullanan çarpıcı ve hızlı bir Laravel geliştirme ortamı. Valet Linux , [Vagrant](https://yuceltoluyag.github.io/virtualbox-vagrant-laravel-arch-linux/) veya [Homestead](https://yuceltoluyag.github.io/virtualbox-vagrant-laravel-arch-linux/)'in yerine geçmez, ancak esnek temeller istiyorsanız, aşırı hızı tercih ediyorsanız veya sınırlı miktarda RAM bulunan bir makinede çalışıyorsanız harika bir alternatif sunar.

* Bilgisayarınızda daha önceden kurulum yaptığınız [Lampp](https://yuceltoluyag.github.io/arch-linux-lampp-kurulumuphp7xmariadbmy/) ve türevleri varsa, devredışı bırakın yada kaldırınız.  Aksi takdirde hatayla karşılaşırsınız.

## Kurulum

 * Terminalinizi açıp şu komutu yapıştırın.

```bash
pacman -S nss jq xsel networkmanager
```
```bash
`pacman -S php`# php sürümü 5.6 dan yüksek olmalıdır ; `php -v` komutuyla kurulumdan sonra sürümü kontrol edin )
```


```bash
yay -S php71-mcrypt #cli, curl, mbstring, xml, zip gibi hatalar alıyorsanız kurmanız gereken paket
```

İsteğe bağlı paketler

[php-sqlite](https://wiki.archlinux.org/index.php/PHP#Sqlite) , [mysql / mariadb](https://wiki.archlinux.org/index.php/PHP#MySQL.2FMariaDB) , [php-pgsql](https://wiki.archlinux.org/index.php/PHP#PostgreSQL)

Benim kullandıklarım

```bash
yay -S php php-dblib php-fpm php-gd php-odbc php-pgsql php-sqlite
```

Composer kurun

```bash
yay -S composer
 ```

daha sonra  .bashrc içerisine  yapıştırın

```bash
PATH="$HOME/.config/composer/vendor/bin:$PATH"
```

artık composer hazır. Composer ile ilgili indirme sorunu yaşarsanız  [composer yavaş indirme sorunu çözümü](https://yuceltoluyag.github.io/composer-yavas-indirme-sorunu-cozumu/)

```bash
composer global require cpriego/valet-linux
```
Şimdi eğlenme zamanı : )

Ana dizine gidip Sites diye bir klasör oluşturuyorum.
```bash
mkdir ~/Sites
```
Sitesi içerisinde ki  her klasör bir domain ismi potansiyeli  taşımaktadır. Lütfen **abudik** **gubidik** isimler atamayın.

Oluşturduğum dizinin içerisine giriyorum.

```bash
cd ~/Sites
```
Dizin içerisinde
```php
valet park
```
komutunu veriyorum. Bu komutla beraber, bu dizinde ki tüm klasörler kayıt altına alınır. Örneğin ;
```php
laravel new blog
```
diyip blog isminde bir laravel projesi oluşturuyorum. Tarayıcımı açıp http://blog.test yazıyorum ta ta : ) İşte bu kadar.  Valet park komutunu önceden verdiğimiz için siz Sites dizini içerisinde ahmet diye bir dosya oluştursanız  http://ahmet.test  adresinden ulaşabilirsiniz.



## valet link komutu

 Bu komutla birlikte bir projenizi sunuma açmak istiyorsanız kullanılabilir.

```bash
valet link projeadi
```
şeklinde  link verebilirsiniz.

```bash
valet links
```

komutuylada daha önce linklediğini projelerinizi görebilirsiniz.

![laravel valet link archlinux](/uploads/laravel-valet-link-archlinux.png)


## Domain Uzantısını değiştirme

İlk kurulumda domain uzantısı .test  olarak gelir. Örneğin domain uzantımızı app,dev vb gibi isimler yapmak istiyorsanız

```
valet domain .app
```
vermeniz yeterlidir. Domain durumunu kontrol etmek için

```
valet domain
```
yazmanız yeterlidir.

Valet portunu değiştirmek isterseniz

```
valet port xxxx #port numarası yazmayı unutmayın
```

Değiştirdiğiniz port aktif olmuş mu, kontrol etmek için

```
valet port
```

Domain uzantısını app veya dev koyduğunuzda muhtemelen ssl hatasıyla karşılaşacaksınız.

```
valet secure laravel
```

ile ssl hatalarından kurtulabilirsiniz, evet bu kadar basit : ) İşlemi geri almak isterseniz

```
valet unsecure projeadi
```

<figure class="image is-16by9">
  <iframe class="has-ratio" width="640" height="360" src="https://www.youtube.com/embed/-Qdxa0XjkgQ?controls=0" frameborder="0" allowfullscreen></iframe>
</figure>
Kaynaklar :

* https://cpriego.github.io/valet-linux/index#installation
* https://cpriego.github.io/valet-linux/requirements.html#arch
