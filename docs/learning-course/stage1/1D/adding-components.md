# 1D: Tasarım Metodolojisi - Basit Swerve Şasisi

## Daha Fazla Parça Ekleme

Part studio içinde daha fazla parça modellediğinizde, bunları montaja daha öncekine benzer bir şekilde ekleyebilirsiniz. Insert tuşuna basın ve hemen yeşil onay işaretine tıklayın. Ardından, oluşturduğunuz ilk `Group`'u düzenleyin ve parçayı gruba ekleyin. Bunu yaparak, eklenen parçaların her zaman part studio içinde modelendiği yerde kalmasını sağlarsınız.

2"x2" tüpü 2"x1" tüpe bağlamak için bir köşebent (gusset) ekleyelim.

### Talimatlar

Başlamak için **`Drivetrain` klasöründeki `Drivetrain` Part Studio'ya gidin**. Köşebenti eklemek için **slaytlardaki talimatları izleyin**.

???+ Tip "Montaj Deliklerini Manuel Olarak Tanımla"
    Tüpteki delikleri yansıttığınızda veya köşebent featurescript'ini kullandığınızda, tüp dönüştürücüsü veya tüp uzunluğu değiştirilirse bu referanslar kolayca bozulabilir. Manuel olarak tanımlanan delikleri tüp kenarından ölçülendirmeye çalışın veya düzeltilmesi gereken şeyleri en aza indirmek için sadece bir deliği yansıtın ve lineer pattern kullanın.

    <figure>
      <img src="../images/define-holes.webp" style="width:60%; border:5px solid #ADADAD; border-radius: 2%">
    </figure>

<!-- <center>**Adding a Gusset**</center> -->
<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/add-0.webp" style="width:100%">
      <figcaption>0. Tamamlanmış şasi montajı.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/add-1.webp" style="width:100%">
      <figcaption>1. Gösterilen delikleri kullanarak crosstube'ı çerçevenin üstüne bağlamak için 1/8" kalınlığında bir köşebenti sketch ve extrude ile oluşturun.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/n8lWSdOV-Ks?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>2. Köşebenti montaja ekleyin ve <code>Group</code>'a ekleyin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/add-3.webp" style="width:100%">
      <figcaption>3. Her iki taraftaki bellypan'daki üç deliğe 2-1/2" #10-32 cıvataları ekleyin böylece diğer taraftaki köşebent deliklerinden geçer. Köşebent deliklerine nylock somunlar ekleyin. 1C'de öğrendiğiniz gibi, bu perçintelerin zamanla gevşemesini ve düşmesini önlemeye yardımcı olur.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/CC017qPw2Mk?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>4. Köşebente perçintleri eklemek için replicate özelliğini düzenleyin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/0O1ojhHTgMI?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>5. Origin küpünde bir mate connector kullanarak köşebenti, cıvataları ve perçintleri şasinin diğer tarafına aynalayın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/drivetrain/add-0.webp" style="width:100%">
      <figcaption>6. Tamamlanmış şasi montajı.</figcaption>
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

Montajınızdaki örnekleri klasörlere (yani çerçeve, swerve modülleri) sıraladığınızdan emin olun ve kullanılan tüm patternleri ve repliceleri adlandırın. Bu, ileride montaj içinde bileşenleri bulmanıza yardımcı olacaktır.

!!! success "Doğrulama"
    Sizin ve/veya ekibinizden daha deneyimli bir üyenin/mentorün [**CAD'inizi incelemesini sağlayın!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"}

    Montajınız yaklaşık 37.2 lbs ağırlığında olmalıdır.

    Sekme yöneticiniz aşağıdaki sekmelere ve klasöre sahip olmalıdır:
    <figure>
      <img src="../images/tab-manager.webp" style="width:100%">
    </figure>

### Detay Seviyesi

Robot donanımının her detayını (cıvatalar, perçintler, somunlar) modellemenin satın alma ve gerçek hayattaki montaj amaçları için faydalı olduğu belirtilmelidir, ancak kesinlikle gerekli değildir. Zaman değerli bir kaynaktır, özellikle yapım sezonu boyunca, bu yüzden en büyük getiriyi sağlayacağı şeylere harcamalısınız.

Onshape montajları için en iyi uygulamalar hakkında daha fazla detay [Assembly Best Practices Page](/best-practices/assembly-setup/ "Assembly Best Practices Page"){:target="_blank"} sayfasında yer almaktadır.


<br>
