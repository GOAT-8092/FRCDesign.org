# 1D: Tasarım Metodolojisi - Basit Swerve Şasisi

## Montaj

Part studio artık tamamlandığına göre, şasi montajını oluşturabilirsiniz.

<!-- Previously, in Stage 1A when you created assemblies one of the parts in the group mate was fixed in place. However, this is not considered a good practice as it is not parametric. This is where the origin cube comes in: the origin cube has a mate connector placed at the origin of the part studio. -->

Önceki aşamadaki pratik egzersizlerde olduğu gibi, tüm parçaları ekledikten ve gruplandırdıktan sonra, origin küpünü montajın originine sabitlemelisiniz. Bu, part studio originini ve montaj originini hizalar.

### Talimatlar

Başlamak için **`Drivetrain` klasöründe `Drivetrain Assembly` adında yeni bir montaj sekmesi oluşturun**. Montajı tamamlamak için **slaytlardaki talimatları izleyin**.

<!-- <center>**Drivetrain Assembly**</center> -->
<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/assy-0.webp" style="width:100%">
      <figcaption>0. Montaj.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/assy-1.webp" style="width:100%">
      <figcaption>1. Part studio parçalarını montaja ekleyin. Daha önce olduğu gibi, sert bileşenleri Origin Cube ile grup mate yapın ve Origin Cube'u montaj originine mate yapın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/vPjp-Xay10s?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>2. FRCDesignLib'den basitleştirilmiş MK4i modülünü montaja ekleyin ve yerine mate yapın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/PA8D-PvsyF0?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>3. Modüllerin montajını tamamlamak için <code>Circular Pattern</code> montaj aracını kullanın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/assy-4.webp" style="width:100%">
      <figcaption>4. FRCDesignLib'den 3/16" Aluminum Blind Rivet (WCP) (.125" - .250" Grip Length) perçintini bellypan deliklerine ekleyin, sabitleyin ve çoğaltın. Köşebent modelleyip eklendiğinde cıvataların eklenmesi için her taraftaki görüntüde gösterilen üç deliği boş bıraktığınızdan emin olun.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/assy-0.webp" style="width:100%">
      <figcaption>5. Montajı tamamlamak için bileşenlerinizi klasörlere düzenleyin ve çoğaltmalarınızı adlandırın.</figcaption>
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

### Perçint Tutunma Uzunluğu

1A'da bahsedildiği gibi, parça kitaplığından eklenecek perçintleri seçerken, **grip length** için bir yapılandırmaya sahip olduklarını fark edeceksiniz. Bir perçintin tutunma uzunluğu, birlikte sabitleyebildiği malzemenin toplam kalınlığıdır. Uygun tutunma uzunluğunu seçtiğinizden emin olun, aksi takdirde kolayca çıkabilir veya malzemeyi birlikte sabitlemeyebilir.

<figure>
    <img src="../images/pop-rivet-steps.webp" width="100%" style="border:5px solid #ADADAD; border-radius: 2%">
    <figcaption>Görsel Kaynak: https://animalia-life.club/qa/pictures/types-of-pop-rivets</figcaption>
</figure>
<br>
