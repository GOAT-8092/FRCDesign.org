# 1A: Onshape Temelleri - Bölüm 2
## Giriş

Bu noktada, çeşitli şekil ve boyutlarda boru çerçeveleri oluşturma konusunda bir uzman olmalısınız. Bu çerçeveler takılacak bir şey olmadan bir arada kalmayacaktır. İşte burada plakalar devreye girer. Bu bölüm öncelikle çeşitli amaçlar için plakaların nasıl modelleneceğine odaklanacaktır.

### Plakalar Nedir?

FRC'de plakalar her yerde kullanılır ve birkaç farklı malzemeden yapılır.

Plakaların FRC'de iki ana işlevi vardır: yapısal parçaları **birbirine bağlamanıza** olanak tanır ve motorlar, miller veya mekanizmalar gibi şanzıman bileşenlerini çerçeveye **montajlamanıza** olanak tanır. Sadece iki parçayı birbirine bağlamak için kullanılan bir plakaya bazen gusset veya bracket de denir.

Aşağıda FRC'de kullanılan plakaların iki örneği bulunmaktadır.

???+ Example "Plaka Örnekleri"

    <div class="grid cards" markdown>

    -   <center markdown><img src="/img/learning-course/stage1a/9442-plate.webp" width="100%"></center>

    -   <center markdown><img src="/img/learning-course/stage1a/604-plate.webp" width="100%"></center>

    </div>

    <figure>
      <figcaption>Mekanizmaları monte etmek ve çerçeveleri bir arada tutmak için kullanılan gusset'ler (Fotoğraf Çredits: FRC 604, FRC 9442)</figcaption>
    </figure>



### Arka Plan

Borularınız her zaman 0.5 inç artışlarla olduğu için, plakalarınız dengesiz mesafeler arasındaki boşluğu doldurmanıza olanak tanır. Bu, plakaların CNC ile üretilmesi ve tamamen keyfi delik aralıklarına izin vermesi nedeniyle mümkündür.

Plakaları tasarlarken düşünmek için ana şey bu keyfi delik aralığıdır. Bir plakanın amacı, montaj deliklerini istediğiniz yere yerleştirmektir; plakayı oluşturan malzeme sadece montaj deliklerini konumlandırmak ve destek çizgileri oluşturmak için vardır, örneğin üçgen gusset kullanırken.

Bir plaka sketch'i delikler için dairelerden, büyük köşe filletleri için yaylardan ve şekli tamamlamak için çizgilerden oluşur. Bir plakanın şeklini yaparken, verilen bir plakadaki tüm montaj deliklerinin etrafına bir ip bağlandığında oluşacak şekli düşünün. İşte çok basit bir plaka için bu kavramı gösteren bir video. Burada takip etmenize gerek yok, sadece izleyin.

<figure>
    <iframe width="768" height="432" src="https://www.youtube.com/embed/mXzX9wmipV8?controls=1&rel=0&showinfo=0&vq=hd1080" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</figure>

Bu video ayrıca `tangent` constraint'ini gösteriyor! Bu, plakalar tasarlarken en sık kullanılan constraint'lerden biridir, çünkü her montaj deliğinin etrafında plakanın çevresini oluşturmak için bir yay olacaktır. Tangent constraint, bir yay veya daire için teğet bir çizgi oluşturmamıza olanak tanır. Plakamızı "pürüzsüzleştirmek" için bu önemlidir. Keskin kenarlar istemiyoruz!

---

## Egzersiz 1: Plaka İş Akışı

**Göreviniz iki rulman deliği olan çok basit bir plaka yapmaktır.** Rulmanlar FRC'de hareket eden parçalardaki sürtünmeyi azaltmak için her yerde ortaya çıkar. Bu, önceki videoda gösterilen ile aynı tür plakadır.

Başlamak için, şablon belgenizin kopyasındaki "Bölüm 2" klasöründeki "Egzersiz 1: Plakalar" part studio'yunu bulun ve birkaç plaka şekli oluşturmayı pratiğini yapmak için aşağıdaki plaka iş akışını takip edin.

???+ Question "Plaka İş Akışı"

    1. Her rulman deliğinin etrafına bir yay çizin, yaylardan birini deliğin 0.25" uzağında olacak şekilde dimensionlayın
    2. Equal constraint'ini kullanarak iki yayı yarıçap olarak eşit yapın
    3. Yayları birbirine bağlayan çizgiler çizin
    4. Her şeyi hizalamak için çizgileri yaylara teğet yapın

!!! info "İpucu"

    Sketch yaparken constraint'ler kazayla oluşabilir. Bir yayın bir kısmı kazayla yatay veya dikey olarak kısıtlanabilir.

    **Constraint'leri silebilirsiniz**, bir sketch öğesinin (çizgi, yay, daire vb.) üzerine gelerek, silmek istediğiniz constraint'in simgesine tıklayarak (ilgili öğeler vurgulanacaktır) ve klavyenizdeki `delete` tuşuna basarak.

    **Geometri oluştururken shift tuşunu basılı tutmak otomatik kısıtlamayı da kapatır.**
    Sıkışırsanız rehberlik için videoya tekrar bakabilirsiniz.

---

### Tamamlandı mı?

Bitirdikten sonra, plaka taslağınızı silin ve **süreç doğal hissedene kadar bu adımları 2-3 kez tekrarlayın veya adımlara bakmamaya çalışın. Size bakmayı bırakmanıza yardımcı olmak için iş akışı açılır menüsünü kapatabilirsiniz.

**Plakaya üçüncü bir rulman deliği eklemeyi deneyin!** Sadece tek bir FRC sezonunda bile düzinelerce plaka yapacağınızdan, bu adımlarla rahat olmak bir zorunluluktur.

İş akışıyla rahat olduğunuzda, bir sonraki egzersize geçmekten çekinmeyin.

<br>
