# 1D: Tasarım Metodolojisi - Basit Swerve Şasisi

## Düzen Çizimlerini Türetme ve Parça Modelleme

Artık düzen çizimini oluşturduğunuza göre, bireysel parçaları modellemeye başlayabilirsiniz. Tüp uzunluğu gibi parçaların kritik boyutları, düzen çizimi tarafından yönlendirilecektir. Bu şekilde, tüpler düzen çizimindeki şasi boyutundaki değişikliklerle otomatik olarak güncellenecektir.

### Talimatlar

Başlamak için **Belgenizde `Drivetrain` adında yeni bir klasör sekmesi oluşturun**. Ardından, **`Drivetrain` klasöründe `Drivetrain` adında yeni bir part studio oluşturun**. Part studio'yu tamamlamak için **slaytlardaki talimatları izleyin**. Origin Cube'un part studio'nuzdaki ilk özellik olması gerektiğini unutmayın.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/parts-0.webp" style="width:100%">
      <figcaption>0. Part studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/parts-1.webp" style="width:100%">
      <figcaption>1. Origin cube'u ekleyerek başlayın. Ardından, daha önce çizdiğiniz düzen çizimlerini Main Layout Sketch part studio'undan eklemek için <code>Derived</code> aracını kullanın. Düzen çiziminde değişiklikler yapılırsa bu özellik otomatik olarak güncellenecektir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/parts-2.webp" style="width:100%">
      <figcaption>2. Tüpleri modellemek için <code>Extrude Individual</code> ve <code>Tube Converter</code> Featurescripts'lerini kullanın. 2"x1" tüpler güç için 1/8" duvar olmalıdır, ancak 2"x2" tüp 1/16" duvar olabilir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/parts-3.webp" style="width:100%">
      <figcaption>3. Bellypan'ın bir köşesiyle başlayın. Köşe, swerve modülü için yer açmak için kesilir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/gk03kkl98NU?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>4. Kesitin iki iç köşesine 1" yarıçaplı sketch filtresi eklemek için <code>Fillet</code> sketch aracını kullanın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/ivUXyr0Lacs?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>5. Ardından, diğer üç köşeyi pattern yapmak için <code>Circular Pattern </code> sketch aracını kullanın. Bellypan'ı 1/8" kalınlığında extrude edin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/parts-6.webp" style="width:100%">
      <figcaption>6. Bellypan'ın alt yüzünü seçerek 0.25" yarıçaplı filtre eklemek için <code> Fillet All Edges</code> Featurescript'ini kullanın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/parts-7.webp" style="width:100%">
      <figcaption>7. Bellypan için montaj deliklerini ekleyin. 0.196" perçint ve cıvata deliklerini pattern yapmak için <code>Linear Pattern</code> ve <code>Circular Pattern</code> karışımını kullanın. 1C Egzersiz 1'de öğrenildiği gibi, cıvatalar perçintlerin zamanla gevşemesini önlemek için kullanılabilir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/mUVoTxoniCY?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>8. Delikleri bellypan'a extrude edin. Sketch doğru şekilde çizilirse, her bir deliği seçmenize gerek kalmamalıdır.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/parts-0.webp" style="width:100%">
      <figcaption>9. Son olarak, sketch'lerinizi adlandırın ve özellik ağacındaki bir klasöre düzenleyin. Ayrıca, bellypan'ın malzemesini Aluminum 6061 olarak ayarlayın ve parçalarınızı adlandırın.</figcaption>
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

### Türetme Özelliği

Bu bölümde, `Derived` özelliğiyle tanıştırıldınız. Bu özellik son derece güçlüdür ve modelleme için referansları etkinleştirmek için bir part studio'dan diğerine parçaları içe aktarmak için kullanılabilir. Ancak, bu işlevi aşırı kullanmamaya dikkat etmelisiniz çünkü part studio'larınızı önemli ölçüde yavaşlatabilir.

### Özellik Ağacı Organizasyonu

Bu noktada, Onshape modellemesi ve Featurescripts kullanımıyla giderek daha rahat hissetmelisiniz. Her zaman düzenli ve kullanımı kolay tutmak için çalışırken özellik ağacınızı temizlediğinizden emin olun. Özellik ağacı organizasyonu hakkında daha fazla bilgiyi [Feature Tree Best Practices](/best-practices/feature-tree-setup/ "Feature Tree Best Practices Page"){:target="_blank"} sayfasından öğrenebilirsiniz.

<br>

