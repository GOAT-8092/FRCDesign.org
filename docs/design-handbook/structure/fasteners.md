# Bağlantı Elemanı Standartları

FRC'de yaygın olarak kullanılan bağlantı elemanları ve standartları rehberi. Çeşitli farklı uygulamalar ve kullanım durumları için her türlü şekil ve boyutta gelirler. Çekirdeğinde, robotunuzu inşa etmek için 2 veya daha fazla parçayı birbirine bağlamak için kullanılırlar.

## CAD'deki Bağlantı Elemanları

### Neden?

Tüm bağlantı elemanlarınızı CAD'inize koymak birkaç nedenle **çok önemlidir**. Donanımı CAD'inize koymak, parçalar arasındaki boşlukları kontrol etmenize, tam olarak ne sipariş etmeniz gerektiğini bilmeniz için doğru bir BOM'a sahip olmanıza ve takımınızın robotu monte etmesini kolaylaştırır.

### En İyi Uygulamalar

Farklı bağlantı elemanı türlerine girmeden önce, önce CAD en iyi uygulamalarından bahsetmeliyiz. Bağlantı elemanlarınızı yanlış şekilde belgeye koymak belgeyi yavaşlatacaktır.

Standart İçerik - Onshape, montajlarınıza import edilmeye hazır çok çeşitli bağlantı elemanlarına sahip "Standart İçerik" adında bir özelliğe sahiptir.

McMaster Carr - Bazen, Standart İçerik sekmesinin ihtiyacınız olan tam boyutta veya türde bağlantı elemanı olmayacaktır. İşte bir sonraki en iyi şeye gittiğimiz yer: McMasterCarr. McMaster'ın düşünebileceğiniz her türlü bağlantı elemanı vardır. En iyi şey? Her birinin ücretsiz olarak indirilebilecek kendi CAD dosyası vardır. Yani, ihtiyacınız olan bağlantı elemanı Standart İçerikte olmadığında ne yapacağınız bir zaman var mı? McMaster'a gidin, ihtiyacınız olan dosyayı indirin ve tekrar yolda olacaksınız.

Replicate Tool - Her montaj için benzersiz boyuttaki her bağlantı elemanını import etmeniz gerekir. Sonra, o donanım parçasını ihtiyacınız olan her yere kopyalamak için son derece yararlı "Replicate" aracını kullanın. Bu, yükleme sürelerini büyük ölçüde azaltır ve montajlarınızı önemli ölçüde temizler, sizin ve başkalarının CAD'inizde gezinmesini kolaylaştırır.

## Cıvatalar ve Somunlar

### Cıvatalar
| Cıvata Türü | Açıklama | Resim |
|:--------------:|:-------:|:-------:|
| Socket Head Cap Bolt (SHCS)| Standart cıvata, kullanılan daha büyük alet nedeniyle sökülmesi zordur | ![](images/bhcs.webp) |
| Button Head Bolt | Daha geniş, yuvarlak kafası vardır ve socket head cıvatasından daha incedir | ![](images/bhcs.webp) |
| Flathead/Countersunk Bolt | Malzeme ile hizalı olacak şekilde, girdiği deliğin countersink yapılmasını gerektirir | ![](images/fhcs.webp) |
| Shoulder Bolt | Rulman veya burç için küçük bir mill gibi davranmak üzere pürüzsüz bir kısmı olan cıvata | ![](images/shoulder-bolt.webp) |

### Somunlar
| Somun Türleri | Açıklama | Resim |
|:-------------:|:-------:|:---------:|
| Nylock Somunlar | Standart somun; somunun gevşemesini önlemek için naylon Inserts vardır |  |
| Düşük Profilli Nylock Somunlar | Standart nylock somundan daha incedir, daha ince bir somun ihtiyacınız olduğunda kullanılır |  |
| Rivsomunlar | Özel aletle monte edilir, tapping alternatifidir, perçite benzer ancak dişleri vardır |  |
| Heat Set Inserts | 3D Yazdırılmış parçalarda parçaya pirinç diş vermek için kullanılır, lehimleme ütüsüyle monte edilir |  |
| Tee Somun | Wood içine basılan somun, esas olarak tamponlarla kullanılır |  |
| Kanatlı Somun | Elle sıkılan somun, tamponları monte etmek için yararlıdır |  |
| PEM Somunlar | Tapping için çok ince bir malzemeye basılan bir somun; nasıl kullanılacağı için [Fabworks's Guide](https://www.fabworks.com/resources/guidelines/hardware) bakın |  |

### Emperyal Cıvata Boyutları
| Diş Boyutu | Kullanımlar | SHCS/BHCS Alet Boyutu |
|:-----------:|:---------:|:-------------------:|
| \#4-40 | Rio Montajı | 3/32 - 1/16 |
| \#6-32 |  | 7/64 - 5/64 |
| \#8-32 | VersaPlanetary | 9/64 - 3/32 |
| \#10-32 | Max Planetary; Neo, Vortex, Falcon, Kraken Montajı, Swerve Montajı; Tapped Rounded Hex | 5/32 - 1/8 |
| 1/4-20 | Daha fazla güç istediğiniz yerlerde kullanılır; tapped churro | 3/16 - 5/32 |

!!! Önemli
    Modern FRC genellikle iki farklı emperyal cıvata türü kullanır, #10-32 ve 1/4-20. FRC COTS bileşenleri esas olarak 10-32 bağlantı elemanlarını kullanır ve biraz çabayla, neredeyse exclusively #10-32 donanımı kullanan robotlar yapabiliriz. Genel olarak:

    - \#10-32 neredeyse her şey için kullanılır: milleri tutturma, motorlara vidalama, süper yapı vb.
    - 1/4-20, #10'ın sağlayabileceğinden daha fazla güç gerektiren yapısal uygulamalar için kullanılır.

### Metrik Cıvata Boyutları
Modern FRC'nin çoğu emperyal olsa da, monte etmek için metrik donanım kullanan birkaç bileşen hala vardır.

| Diş Boyutu | Kullanımlar | SHCS Alet Boyutu |
|:-----------:|:---------:|:-------------------:|
| M3 | Neo550 Motor Montajı, Ultraplanetary Şanzımanlar | M2.5 |
| M4 | 775pros Montajı, BAG motorları | M3 |
| M5 | Snowblower Motor Montajı | M4 |
| M6 | PDP Battery Lug Montajı | M5 |


Donanım around tasarım yaparken, **[delik aracını](https://cad.onshape.com/help/Content/hole.htm)** kullanmak veya tabloyu ezberlemek en iyisidir (Çok Yakında)

- \#10-32 donanımı standart bir oturum için **0.196 inç** delik çapı kullanır
- 1/4-20 donanımı standart bir oturum için **0.257 inç** delik çapı kullanır

## Perçinler

### Perçin Türleri

### Perçin Boyutları

## Tapped Bileşenler

**Çok Yakında**

## Cıvata Tutma

Nylock Somunlar

Loctite


## Kaynak

**Çok Yakında**

## Donanım Kaynağı

**Çok Yakında**

<!-- Farklı türde donanım ve onları nereden satın alacağınızı dahil mi? */



<br>
