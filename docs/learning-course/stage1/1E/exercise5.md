# 1E: Alt Sistem İş Akışı - Drivebase Detaylandırma

## Egzersiz: Tampon Montajı

Batarya montajına benzer şekilde, iyi tampon montajı genellikle gözden kaçırılır. Sağlam bir tampon montaj sistemi size hiçbir maçı kazandırmazken, zayıf bir tampon montaj sistemi kesinlikle bir maçı kaybettirebilir. Zayıf tampon montajı [tampon hasarına](https://youtu.be/9mawtTD6v7M?si=RyM0fE6GrR4QlMEU&t=78 "3647 Tamponları Kırılıyor"){:target="_blank"}, uzun tampon değiştirme süresine veya hatta tamponlarınızın [düşmesine](https://youtu.be/pBUKxWKGV-Q?si=hmJtt9N6C7vGLFpL&t=42 "Tamponlar Düşüyor"){:target="_blank"} neden olabilir.

Referans tasarımda, threadli stud tampon montaj sistemi uygulanmıştır.

!!! Örnek "Threadli Stud Tampon Montaj Sistemi"
    <figure>
        <img src="../images/bumper-mount/stud-mount.webp" style="width:70%">
        <figcaption>Threadli stud tampon montaj sisteminin kesit görünümü. Threadli stud tampon ahşabına takılır ve somun tamponları çerçeveye karşı sıkı tutar.</figcaption>
    </figure>


### Talimatlar

**Drivetrain'inize istediğiniz tampon montajlarını ekleyin.** Aşağıdaki talimat slaytlarından ilham alabilirsiniz.
<!--
Tamponlar ve farklı tampon montaj seçenekleri hakkında daha fazla bilgiyi [Design Handbook](/design-handbook/) sayfalarından öğrenebilirsiniz.  -->

<!-- <center>**Örnek Tampon Montaj Modelleme Slaytları**</center> -->
<!-- Slideshow container -->
<div class="slideshow-container">
    <!-- Full-width images with number and caption text -->
    <div id="slide1" class="mySlides fade">
        <figure>
            <img src="../images/bumper-mount/bumper-mount-0.webp" style="width:100%">
            <figcaption>0. Tamamlanmış tampon montajları. </figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper-mount/bumper-mount-1.webp" style="width:100%">
            <figcaption>1. Tampon montajını modelleyin. Bu parça 3/16" kalınlığında alüminyum olmalıdır. Threadli stud yuvaya düşer.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper-mount/bumper-mount-2.webp" style="width:100%">
            <figcaption>2. Threadli stude vidalanan somun için pocket ekleyin. Bu somun tamponları çerçeveyle sıkı tutar. Pocket somunu güvence altına alır ve tamponun yukarı kalkmasını önler.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper-mount/bumper-mount-3.webp" style="width:100%">
            <figcaption>3. Fillet yapın ve isteğe bağlı olarak montajı pocketleyin. 0.15" genişliğinde kaburgalar ve 1/8" takım yarıçapı önerilir. </figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper-mount/bumper-mount-4.webp" style="width:100%">
            <figcaption>4. Montajı ekleyin ve <code>Group</code>'a ekleyin. Üç montaj daha kopyalayın ve drivetrain assembly'sine mate edin. Takımınız çok parçalı tamponlar çalıştırıyorsa (örn: iki C şeklinde tampon) tamponları güvence altına almak için daha fazla montaj eklemeniz gerekebilir.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper-mount/bumper-mount-0.webp" style="width:100%">
            <figcaption>5. Drivetrain assembly'sinde tamamlanmış tampon montajları.</figcaption>
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
