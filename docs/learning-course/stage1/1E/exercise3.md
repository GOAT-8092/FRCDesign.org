# 1E: Alt Sistem İş Akışı - Drivebase Detaylandırma


## Egzersiz: Bellypan Pocketing

Bazı takımlar ağırlığı azaltmak ve kablo bağlamayı kolaylaştırmak için bellypan'ı pocketlemeyi seçebilir. Pocketli bir bellypan yaklaşık 3-4 libre (1.4-1.8 kg) tasarruf sağlayabilir. Ancak, bu bellypan'ı kendiniz üretiyorsanız önemli ölçüde üretim süresi ekleyecek veya bir üretim hizmetinden (örn: [Fabworks](https://fabworks.com/ "Fabworks Sheet Metal Services"){:target="_blank"}) bellypan satın alıyorsanız maliyeti artıracaktır. Takımınızla ödünleleri dikkatli bir şekilde düşünmelisiniz.

### Talimatlar

**Eğer drivetrain'iniz için bellypan'ınızı pocketlemeyi seçerseniz**, `Part Lighten` [Featurescript](../../../resources/featurescripts.md "Featurescripts Sayfası"){:target="_blank"} kullanan slaytlardaki talimatları **takip edebilirsiniz**. Bellypan'ı pocketlemek için `Vent` veya `Part Lighten` [Featurescripts'lerini](../../../resources/featurescripts.md "Featurescripts Sayfası"){:target="_blank"} de kullanabilirsiniz. Her Featurescript arasında iş akışı biraz farklı olsa da, genel fikir aynıdır. Güç ve kolay modelleme için elmas deseni önerilir.

<!-- <center>**Örnek Bellypan Pocketing Slaytları**</center> -->
<!-- Slideshow container -->
<div class="slideshow-container">
    <!-- Full-width images with number and caption text -->
    <div id="slide1" class="mySlides fade">
        <figure>
            <img src="../images/pocket/pocket-0.webp" style="width:100%">
            <figcaption>0. Pocketli bellypan. </figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/pocket/pocket-1.webp" style="width:100%">
            <figcaption>1. Dikeyden 45 derece ofset iki dik çizgi ve crosstube kenarından hafif ofset bir çizgi çizin. </figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/pocket/pocket-2.webp" style="width:100%">
            <figcaption>2. Dikey çizgileri bellypan'ın üst kısmını tamamen kaplayana kadar doğrusal desen yapın. Bunlar ana kaburgalar olacak.
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/pocket/pocket-3.webp" style="width:100%">
            <figcaption>3. Üst kaburgaları bellypan'ın alt kısmına ayna yapın.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <div class="slide-content">
            <iframe src="https://www.youtube.com/embed/ZvEMMgEf420?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
            <figcaption>4. Montaj deliklerinin bir kaburgadan çok uzak olması sonucunda oluşabilecek adaları bağlayın. Video, kaburgalar eklerken lighten özelliğinin son sonucunu görmenize izin veren potansiyel bir iş akışı gösterir.</figcaption>
        </div>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/pocket/pocket-0.webp" style="width:100%">
            <figcaption>5. Bellypan'ı pocketlemek için bir pocketing Featurescript kullanın. Önerilen ayarlar 0.15" genişliğinde kaburgalar ve 3/16" takım yarıçapıdır.</figcaption>
        </figure>
    </div>
    <!-- Next and previous buttons -->
    <button class="prev" onclick="plusSlides(-1,0)" style="background-color: #000; color: #fff;">&#10094;</button>
    <button class="next" onclick="plusSlides(1,0)" style="background-color: #000; color: #fff;">&#10095;</button>
    <!-- The dots/circles -->
    <div class="dotsContainer" style="text-align:center">
        <!-- Dots will be generated here -->
    </div>
</div>



<br>
