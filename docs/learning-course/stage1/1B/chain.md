

# 1B: Güç Aktarımı

## Zincir ve Dişli Temelleri

Zincir ve dişli sürücüleri, kayış ve kasnak aktarma organlarına çok benzer. Birbirine bağlı halkalardan oluşan bir zincir ve zincirle meshleşen dişli tekerlekler olan dişliler olmak üzere iki ana bileşenden oluşurlar. Dişliler dönerken, zincirle etkileşime girer ve onu hareket ettirir, böylece gücü bir mildden diğerine aktarır. Bisikletler, güç iletmek için zincir kullanan günlük nesnelerdir. Zincirler uzun mesafelerde yüksek kuvvet iletmekte mükemmeldir.

<figure>
    <img src="../images/chain/chain-animation.gif" style="width:40%">
    <figpcation>Basit bir zincir ve dişli animasyonu. Dişlilerin aynı yönde döneceğini unutmayın.</figcaption>
</figure>

Girişten çıkışa tork ve hızı değiştirmek için, farklı boyutlarda dişliler kullanılmalıdır. Zincir aktarma organları için mekanik avantaj, dişlilere ve kasnaklara benzer şekilde, çıkış dişlisinin diş sayısının giriş dişlisinin diş sayısına oranı temelinde oluşturulur. Kasnaklara benzer şekilde, dişliler aynı yönde dönecektir.

### Zincir Türleri

FRC'de yaygın olarak kullanılan rulmanlı zincirin iki boyutu vardır: #25 ve #35 zincir, sırasıyla 0.25" ve 0.375" pitch'e sahiptir. Zincir için **pitch** her halkanın uzunluğudur. Zincirin *pitch uzunluğu* ise pitch'in (0.25" veya 0.375") halka sayısı ile çarpılmasıdır. Tam bir halkadan daha zayıf olan "yarım halka" kullanımını önlemek için çift sayıda halka kullanmaya çalışın. Bu, zincir pitch uzunluğunuzun 0.5"in bir katı olması gerektiği anlamına gelir.
<!--
Çap çapını hesaplamak için aşağıdaki denklem kullanılabilir:

<center>**`PD = Pitch / sin [180°/# of teeth]`**</center> -->

Ayrıca, **zincir boşluk çapı**, zincirin sarılmış olduğu dişlinin çapını tanımlar. Aşağıdaki denklem kullanılabilir:

<center markdown>**`Clearance Diameter = PD + Pitch`**</center>

Aşağıda bir dişlinin pitch'i, çap çapı, dış çap ve zincir boşluk çapının bir çizimi bulunmaktadır.

<figure>
    <img src="../images/chain/chain-diagram.webp" style="width:70%">
    <figcaption>Zincir dişlisi çap ölçümlerinin çizimi. (Görsel kaynak: <a href="https://docs.wcproducts.com/frc-build-system/belts-chain-and-gears/sprockets-and-chain">WCP</a>)</figcaption>
</figure>

FRC'de #25 zincir genellikle kullanılır, çünkü güçlüdür ve nispeten hafiftir. #35 bazen çok yüksek torklu aktarma organlarında kullanılır, ancak ağır ve hantaldır.

### Zincir Aktarma Organlarını Modelleme

Zincirin modelleme iş akışı, önceki sayfadaki kayışlar ile tamamen aynıdır. İki dişlinin çap çapına ve doğru merkezden merkeze mesafesine ihtiyacınız olacak.

[`Origin Cube` Featurescript](https://cad.onshape.com/documents/321c197a842fc5f1a29e6621/w/fc3cdd5ca7edcd93e02f13cc/e/2b321cb91b74224b9c14b433 "Origin Cube Featurescript Onshape Document"){:target="_blank"} fonksiyonunu kullanarak, bir zincirle bağlanmak istediğiniz noktalarda iki dişlinin çap çaplarını dimension yapın.

* `#SprocketPD_25(n)`: `n` dişli #25 pitch dişlinin çap çapını hesaplar.
    * Örnek: `#SprocketPD_25(16)` 16 dişli #25 pitch dişlinin çap çapını döndürür.

Kayışlar için kullandığınız aynı [`Belt & Chain Gen` Featurescript](https://cad.onshape.com/documents/53c0b14cad92676c14e04e97/w/1271c254ccb0a79563210195/e/7394c4a86d8d6c35c9a12041 "Belt & Chain Gen Featurescript Onshape Document"){:target="_blank"} ile zincirin 3D modelini oluşturun, ürettiği zincir halka sayısını kontrol edin, ardından doğru merkezden merkeze mesafeyi elde etmek için zincir halka sayısını kullanarak merkezden merkeze mesafenizi dimension yapın. Aşağıdaki Origin Cube fonksiyonunu kullanın:

* `#ChainCTC_25(n1, n2, n3)`: `n2` diş sayısına sahip dişliyi ve `n3` diş sayısına sahip dişliyi bağlayan `n1` halkalı #25 pitch zincirin c-c mesafesini hesaplar.
    * Örnek: `#ChainCTC_25(80,16,48)` 16 dişli dişliyi 48 dişli dişliye bağlayan 80 halkalı #25 pitch zincir için merkez mesafesini döndürür.


### Zincir Gergileri

Zincir ile tasarlarken bir zorluk, kullanıldıkça fiziksel olarak genişleyeceğidir. Bu, her halka arasındaki mesafenin hafifçe artacağı anlamına gelir ve bu da genel zinciri önemsiz olmayan bir şekilde uzatır. Zincir aktarma organı zincir germe dikkate alınarak tasarlanmadıysa, gevşek zincir düzeltmek zor olabilir. Henüz zincir germe yöntemlerini öğrenmeyecek olmasanız da, bu fikri aklınızda tutmalısınız.

Aşama 2'de, farklı robot mekanizma türleri bağlamında farklı zincir germe yöntemleri tanıtılır. [Design Handbook page](/design-handbook/ "Design Handbook Page"){:target="_blank"} da bu konuya daha derinlemesine girer.

!!! Example "Zincir Gerge Örneği"
    <figure>
        <img src="../images/chain/turnbuckle.webp" style="width:60%">
        <figcaption>Bir "turnbuckle" veya "inline" zincir gergi. Turnbuckle, zinciri sıkı tutmak için ayarlanabilen değişken uzunluklu bir halka olarak görev yapar. (Fotoğraf Kaynak: FRC 1538)</figcaption>
    </figure>

<br>
