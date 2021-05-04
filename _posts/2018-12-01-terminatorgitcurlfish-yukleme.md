---
layout: post
title: terminator+git+curl+fish yükleme işlemi(terminali özelleştirme)
description: terminator+git+curl+fish yükleme işlemi(terminali özelleştirme)
category: linux
tags: [linux, terminal]
comments: true
edit_url: true
---

Merhaba, linux’ta en çok vakit geçirdiğimiz terminalimizi nasıl özelleştirebiliriz ? Aradığınız cevap tamda burada 💪 En çok vakit geçirdiğimiz elin adamının dediği gibi home home sweet home niteliğinde ki terminalimizi nasıl şekillendirebiliriz, konusuna değindim.
<!-- excerpt separator -->
Ubuntu'nun varsayılan olarak gelen terminali standart kullanımlarda iş görüyor ancak birden fazla terminalle çalışmanız gerektiğinde işler iyice karışıyor 😓 Linux ta her zaman ki gibi envaii çeşit alternatif var ancak ben **terminator** ve **fish** birleşimden ortaya çıkan karışımı lezzettli buluyorum.😉

-   Aynı ekran içerisinde bölünebilmesi(x-y ekseninde bile)
-   Kod renklendirme, kod tamamlama,önceki kullanılan kodları gösterme
-   Eklentiler ve temalar gibi bir çok özelliğinin bulunması terminatör kullanmak için binlerce sebeplerden birisi..

	-  [Oh My ZSH Kurulumu](https://yuceltoluyag.github.io/oh-my-zsh-kurulumu-tema-ve-eklentiler/) (diğer tavsiyem)

```shell
sudo apt-get install terminator #terminatoru yüklüyoruzt
```
-   [iterm2colorschemes.com](http://iterm2colorschemes.com/%C2%A0) sitesinden beğendiğimiz bir temanın ismini kopyalıyoruz. Github sayfasından terminator klasörüne girip beğendiğimiz temanın adını aratıyoruz.

```shell
sudo gedit ~/.config/terminator/config #kodlarımızı profile kısmının altına yapıştırıyoruz
```
```shell
bash #enter
```
```shell
sudo apt-get install fish #fish kurulumu fish #yazarak fishe giriş yapıyoruz simgenin değiştiğini görebilirsiniz.
```
```shell
chsh -s /usr/bin/fish #varsayılan terminalimizi değiştiriyoruz
```

-   [oh-my-fish](https://github.com/oh-my-fish/oh-my-fish) adresinden curl bağlantısı ile fishi kuruyoruz.
-   [oh my fish temaları](https://github.com/oh-my-fish/oh-my-fish/blob/master/docs/Themes.md) adresinden beğendiğiniz temayı omf install temaadı yazarak yükleyebilirsiniz.
-   [oh my fish eklentileri](https://github.com/oh-my-fish)  sayfasından eklentileri arayarak keşfedebilirsiniz. Tıpkı tema yüklemede olduğu gibi omf install eklentiadı yazarak indirebilirsiniz.

<figure class="image is-16by9">
  <iframe class="has-ratio" width="640" height="360" src="https://www.youtube.com/embed/h78f3V4p09E" frameborder="0" allowfullscreen></iframe>
</figure>