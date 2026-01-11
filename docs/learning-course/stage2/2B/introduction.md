# 2B: Dingil Silisi Pivot

## Rotary Mekanizmalar
Rotary mekanizmalar, döner hareket ile mekanizmaların pivotlanmasını sağlar. Bu mekanizmalar birçok şekil ve boyutta gelir, ancak güçlendirilmiş pivotlar tasarlanırken izlenmesi gereken birkaç iyi uygulama vardır.

<figure><img align="left"  src="/img/learning-course/stage2-pivot/6036pivot.gif" width="46%" style="border:5px solid #ADADAD"><img align="right"  src="\img\learning-course\stage2-pivot\2910video.gif" width="48%" style="border:5px solid #ADADAD"></figure>
<center><figcaption>6036'un 2023 Kolu ve 2910'un 2023 Kolu</figcaption></center>

[Takım 2910'un 2023 robot reveal videosunu](https://youtu.be/R5r28-MQqzg?si=wgrmD0YIbUkkHDyv&t=65 "2910 2023 Reveal Video"){:target="_blank"} izleyerek pivotlayan kolunu aksiyon halinde görün.


### Pivot Sürücü Sistemler

İki tip pivot sürücü sistemi vardır: Dingil Silileri ve Live Axles. Aşağıdaki tablo iki tipin artılarını ve eksilerini karşılaştırır.


| **Mil Tipi** | **Açıklama**  | **Artıları**   | **Eksileri**  | **Resim** |
|---------------|------------------------------------------------------------|--------------------------|-----------------------------------|------|
| **Dingil Silisi** | Mil sabit kalır ve mekanizma onun etrafında pivotlanır.   | Daha güçlü, daha büyük mil, milin bükülme riski yok.| Güç transferi için ayrı bir yöntem gerektirir. Paketleme sorunlarına yol açabilir  | ![dead axle](\img\learning-course\stage2-pivot\dead-axle-side.webp){width=70%}
| **Live Axle** | Mil mekanizma ile birlikte döner. Genellikle hex miller ve hub'lar ile kullanılır.| Basit kurulum. Doğrudan güç transferi.  | Milin bükülme riski. Genellikle 1/2 hex ile yapılır, bu uygulama için çok zayıf olabilir| ![live axle](\img\learning-course\stage2-pivot\liveAxlePivot.webp){width=70%}

Bunlar arasında, dead axles (ve sonuç olarak koaksiyal tasarımlar) pivotlar için en iyi seçimdir, özellikle önemli miktarda yükü kaldırmaları gerekenler için.

Pivotlayan mekanizmaları tasarlarken bazı önemli noktalar şunlardır:

1. Pivotlayan "kol"un ağırlık merkezini pivot'a mümkün olduğunca yakın tutun.
2. Milin tamamen desteklendiğinden emin olun, kutu boru veya iç içe plakalar kullanarak.
3. Rijit bir destek yapısını koruyun.
4. Yapı genişse, ek rijitlik için her iki tarafı da güçlendirin.

### Uygulamalar & Örnekler

| **Mekanizma Tipi**       | **Açıklama**                                                                 | **Mil Tipi**                                                        | **Sürtünme Yönetimi**                                             | **Resimler**                                                                                                     |
|--------------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------------------|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **Bilek**                | Kısa, hafif rotary mekanizmalar. Bunlar genellikle yerden toplama veya eğim ayarları için izin vermek için görülür. | Bilekler için koaksiyal, live ve dead axles bulacaksınız.                 | Hem rulmanlar hem de bushings yaygındır.                           | <center><img src="\img\learning-course\stage2-pivot\973-wrist.webp" width="50%"></center>                           |
| **Büyük Pivotlar**         | Pink arms, pivotlayan asansörler ve büyük kollar dahildir.                           | Dingil silisi tercih edilir; ağır yükler için 35 zincir kullanmayı düşünün.     | Bushings daha yaygındır, ancak ince x contact rulmanları bazen kullanılır. | <center><img src="\img\learning-course\stage2-pivot\2910-pivot.webp" width="50%"></center>                           |
| **Yüksek Yük Kısa Pivot**| Atış açısını ayarlamak için shooter gibi tam mekanizmaları pivotlar.                   | Büyük pivotlar ile aynıdır.                                            | Hem rulmanlar hem de bushings kullanılır.                             | <center><img src="\img\learning-course\stage2-pivot\citrus-pivot.webp" width="50%"></center>                           |


Pivotlar için diğer mekanizma örnekleri ve derinlemesine bilgiler [pivots page](/mechanism-examples/pivots/ "Pivot Mechanism Examples Page"){:target="_blank"} sayfasında bulunabilir. Mekanizma temelleri sayfası henüz yapılmadı ama da yardımcı bir kaynak olacaktır.


<br>
