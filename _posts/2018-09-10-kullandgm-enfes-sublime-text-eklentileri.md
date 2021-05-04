---
layout: post
title: Kullandığım Enfes Sublime Text Eklentileri
description: Kullandığım Enfes Sublime Text Eklentileri
comments: true
edit_url: true
category: editor
tags: [ipucu, sublime]
---

Merhaba, sublime text editörünü kullananan arkadaşlara kendi kullandığım eklenti ve temaları blogumda paylaşmak istedim .)

## Sublime Text Eklenti Kurulumu

 Öncelikle hangi sürümü kullanıyorsunuz bilmiyorum ama ben güncel sürüm olan süblime text 3 sürümünü kullanıyorum. Paket yükleme modülümüzü yüklemek için view-> show console açıp sürümünüze göre gerekli kodları yapıştırıp entere basmanız gerekli [Sublime Text Eklenti Yükleme](https://packagecontrol.io/installation),eklentiyi yükledikten sonra ctrl + shift + p kombinasyonuyla paket menajerimizi açabiliriz. İnstall yazıp entere basın önünüze bir sekme daha gelecek kuracağınız paketin ismini yazın bu kadar : )

<!-- excerpt separator -->

## EMMET
Emmet kod yazmanızı hızlandıracak mükemmel bir eklentidir. Kod yazmaya başlayan arkadaşlara kesinlikle tavsiye etmiyorum ezberciliğe itiyor belirli bir seviyeden sonra kullanmanızı tavsiye ederim.

```html

#page>div.logo+ul#navigation>li*5>a{Item $} çıktısı şu şekilde olacaktır.

```

## Alignment
Bu eklentiyle benim gibi düzen takıntısı olan için :D Bu eklenti kodlarınızı hizalamaya ve düzenlemeye yarıyor. **Ctrl + alt + a** ya basarak düzene sokabilirsiniz.



## SublimeGit

Sublime Text için Git paketi,dökümanı için [Sublimegit Dökümantasyon](https://sublimegit.readthedocs.io/en/latest/)  adresini inceleyebilirsiniz.



## GitGutter

Sidebar tarafında projeniz üzeribde yaptığınız değişiklikleri gösteriyor. git status komutunun sublimedeki hali olarak düşünebilirsiniz.



## GitHubinator
 bu eklenti sublimetext içerisinde seçtiğiniz alanı github reponuzda aramaya yarıyor, acaba bunu nerede yazmışım derdine son



## GitOpenChangedFiles

Bu eklentinin gitgutter den farkı sadece değişiklik yapılmış satırları gösterip repo da aratıp toplama yapabilmesi :D **ctrl+shift+o** kısayol tuşunu kullanabilirsiniz.



## SublimeLinter

Kendi sınıflarınızı,sublime içerisinde ayarlamalar yapmanıza yarayan basit ama ilk başta bakınca bu ne lan acaba diye bakakalıyorsunuz, [http://www.sublimelinter.com](http://www.sublimelinter.com/) siteden biraz okuyunca yavaş yavaş çözeceğinizi düşündüğüm bir eklenti..( **SublimeLinter-jshint, SublimeLinter-php** ek olarak kurabilirsiniz)



## ChangeQuotes

 Bu eklentiyi sık kullanıyorum diyebilirim, özellikle satırdaki çift tırnakları tek tırnak yapma olayı pdoda işimi görüyor çok eringeçim :D Bunun haricinde paket sisteminde **SASS BABEL Siteleaf Liquid Syntax** aratarak renklendirme sınıf ve eklentilerini kullanabilirsiniz.

## SidebarEnhancements

Normalde sol taraftaki sidebarda sağ tık özelliklerinde çok fonksiyon yoktur gene proje içerisinde dosya oluştur felan fişman bu eklenti ona gerek kalmadan tüm işlemleri sol pencereden işinizi kolaylaştırıyor. View menüsünden Show Sidebar diyerek proje olmasa gösterim yapabilirsiniz.

## BracketHighlighter
Bu eklenti sayesinde parentez köşeli süslü taglar içerisindeki tüm kod düzenekleri daha düzenli daha renki bu sayede classlarınıza daha çabuk ulaşabilirsiniz.


## Gutter Color
Bu eklenti sayesinde renk seçimlerinizi ekstra bir program olmadan rahatça seçebileceksiniz. Ayrıca **Color Highlighter** renk kodlarınızı renkli görebilirsiniz.



## AlignTab
 VIM editörün tabular eklentisinden ilham alırak yapılmıştır.

 - Normal ifadeyi kullanarak hizala
- Özel boşluk, dolgu ve gerekçelendirme.
- Herhangi bir çizgi seçilmezse hizalama için akıllı algılama
- Çoklu imleç desteği
- Tablo modu ve Canlı önizleme modu özellikleri mevcuttur
- Daha fazlası için [Github](https://github.com/randy3k/AlignTab) sayfasına göz atın.

## AutoFileName
 Dosya yollarınızı otamatik olarak önünüze çıkartır. Olmayan bir dizin yazdığınızda öneriler çıkmaz. Css Js vb gibi dosyaları çağırırken ki yaptığımız hataları bir nebze olsada azaltır.



## HTML-CSS-JS Prettify
HTML, CSS, JavaScript ve JSON kod biçimlendiricisi



## DocBlockr

 Kod bloklarımızın üzerine açıklamalar yazarız ya işte buda o işe yarıyor /** Açıklama tab şeklinde kullanımı var diğer kullanımlar için [github](https://github.com/spadgos/sublime-jsdocs) sayfasına bakınız



## A File Icon
 Dosyaların uzantılarına göre simgeler atıyor sidebarın daha şık görünmesini ayrıca dosyaların karışmasında engelliyor.Küçük pencerelerde çalışanlar için ideal.



## Tema ?

Material Tema Kullanıyorum [https://github.com/equinusocio/material-theme](https://github.com/equinusocio/material-theme)

* Yeni kullandığım temalar ve pluginler (Özellikle PHP kodlayan arkadaşlar içindir) [https://github.com/yuceltoluyag/sublime-text-3](https://github.com/yuceltoluyag/sublime-text-3)
Ayarlarım



```textile

{

"always_show_minimap_viewport": true,

"bold_folder_labels": true,

"color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme",

"font_face": "Hack",

"font_options":

[

"gray_antialias",

"subpixel_antialias"

],

"font_size": 18,

"ignored_packages":

[

"Vintage"

],

"indent_guide_options":

[

"draw_normal",

"draw_active"

],

"line_padding_bottom": 3,

"line_padding_top": 3,

"material_theme_accent_acid-lime": true,

"material_theme_accent_blue": true,

"material_theme_accent_brba": true,

"material_theme_accent_bright-teal": true,

"material_theme_accent_cyan": true,

"material_theme_accent_graphite": true,

"material_theme_accent_indigo": true,

"material_theme_accent_lime": true,

"material_theme_accent_orange": true,

"material_theme_accent_pink": true,

"material_theme_accent_purple": true,

"material_theme_accent_red": true,

"material_theme_accent_scrollbars": true,

"material_theme_accent_sky": true,

"material_theme_accent_titlebar": true,

"material_theme_accent_tomato": true,

"material_theme_accent_yellow": true,

"material_theme_arrow_folders": true,

"material_theme_big_fileicons": true,

"material_theme_bold_tab": true,

"material_theme_bright_scrollbars": true,

"material_theme_bullet_tree_indicator": true,

"material_theme_compact_panel": true,

"material_theme_compact_sidebar": true,

"material_theme_contrast_mode": true,

"material_theme_disable_fileicons": true,

"material_theme_disable_folder_animation": true,

"material_theme_disable_tree_indicator": true,

"material_theme_panel_separator": true,

"material_theme_small_statusbar": true,

"material_theme_small_tab": true,

"material_theme_tabs_autowidth": true,

"material_theme_tabs_separator": true,

"material_theme_titlebar": true,

"material_theme_tree_headings": true,

"overlay_scroll_bars": "enabled",

"theme": "Material-Theme.sublime-theme"

}

```

