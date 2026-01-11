

# 1E: Alt Sistem İş Akışı - Drivebase Detaylandırma

## Egzersiz: Tamponlar
Tampon yapımı her yılın FRC oyun kılavuzunda açıklanmıştır. Geçmişte, iki 2.5" çapında havuz noodlesu ve arkasında 5" boyunda 3/4" kalınlığında kontrplak levha olması gerekiyordu. En güncel tampon kuralları için en son oyun kılavuzuna bakın. Tampon kesimi ve yerden yükseklik kuralları yıldan yıla değişecektir.

### Tampon Modeli
Özellik ve assembly ağaçlarınızı düzenli tutmak için tamponları yeni bir part studio ve assembly'de yerleştirmeniz önerilir. Minimum detay seviyesi, tamponun blok modeli olmalıdır. Bazı takımlar üretime yardımcı olmak için tampon ahşabı, tampon ahşap delikleri, tampon ahşabı için açı braketleri ve diğer detayları modellemeyi seçebilirler. Gerekli detay seviyesini belirlemek için takım arkadaşlarınızla iletişim kurmalısınız.

### Talimatlar

**Drivetrain'inize tamponlar ekleyin.** Aşağıdaki talimat slaytlarından ilham alabilirsiniz.

<!-- <center>**Örnek Tampon Modelleme Slaytları**</center> -->
<!-- Slideshow container -->
<div class="slideshow-container">
    <!-- Full-width images with number and caption text -->
    <div id="slide1" class="mySlides fade">
        <figure>
            <img src="../images/bumper/bumper-0.webp" style="width:100%">
            <figcaption>0. Tamponlar assembly'si drivetrain assembly'sine eklenmiş tamamlanmış durumda. </figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper/bumper-1.webp" style="width:100%">
            <figcaption>1. Tampon profili ile Main Layout Sketch part studio'da yeni bir sketch oluşturun. 3/4" yerden yükseklik ve tampon ile çerçeve arasında 1/4" boşluk önerilir.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper/bumper-2.webp" style="width:100%">
            <figcaption>2. Tamponlar için drivetrain klasöründe yeni bir part studio oluşturun. Origin Cube'u ekleyin ve drivetrain ve tampon sketch'lerini Main Layout Sketch'ten derive edin.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper/bumper-3.webp" style="width:100%">
            <figcaption>3. Tamponların blok modelini oluşturmak için tampon profilini drivetrain üst layout sketch'inin kenarları boyunca sweep edin.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper/bumper-4.webp" style="width:100%">
            <figcaption>4. İsteğe bağlı olarak köşelere bir fillet ekleyin. Takımınız tampon havuz noodlesularını nasıl sararsa ona göre boyutlandırın.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper/bumper-5.webp" style="width:100%">
            <figcaption>5. İsteğe bağlı olarak tamponlar için ahşabı modelleyin. Bu üretim amaçları için yararlı olabilir.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper/bumper-6.webp" style="width:100%">
            <figcaption>6. Drivetrain klasöründe bir tampon assembly'si oluşturun ve tüm bileşenleri ekleyin. Tüm bileşenleri gruplandırmayı ve origin cube mate connector'ü orijine mate etmeyi unutmayın.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/bumper/bumper-0.webp" style="width:100%">
            <figcaption>7. Tampon assembly'sini drivetrain assembly'sine ekleyin.</figcaption>
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

Tampon part studio ve assembly'sini drivetrain'den ayrı tutmak, drivetrain özellik ağacını daha temiz tutar ve üst düzey assembly'de tamponları gizlemeyi/göstermeyi kolaylaştırır çünkü tüm tampon assembly'sini bir kerede gösterebilir ve gizleyebilirsiniz.




<br>
