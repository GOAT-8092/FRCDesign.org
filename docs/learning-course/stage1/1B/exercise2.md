


# 1B: Güç Aktarımları

## Egzersiz 2: İki Kademeli Şanzıman

Bu egzersizde, iki kademeli bir şanzıman modelleyip monte edeceksiniz. Bu egzersizin amacı, daha gelişmiş şanzımanları modelleme pratiği yapmaktır. Ayrıca, parçaları hafifletmek için kullanılan [`Part Lighten` Featurescript`](https://cad.onshape.com/documents/028ca8fb10baf53e1f6fce96/v/821c8b51ed0953526b51926e/e/a8b9e45297aac9f5688c871d "Part Lighten Featurescript Onshape Document"){:target="_blank"}'in nasıl kullanılacağını öğreneceksiniz.

!!! Uyarı
    Bu aşama plakalarınızı part studioyu bitirdiğinizde hafifletmenizi istese de, bu en iyi pratik değildir. Tam bir mekanizma veya robot modellediğinizde, mekanizmaya veya tam robota tüm tasarım incelemeleri ve değişiklikler yapılana kadar **plakaları hafifletmek için beklemelisiniz**. Aksi takdirde, plaka veya mekanizma her değiştiğinde hafifletmeyi düzeltmek için zaman harcarsınız.

### Part Studio Talimatları
Kopyaladığınız belgede **"Exercise #2 Part Studio" sekmesine gidin** ve part studioyu tamamlamak için **slaytlardaki talimatları izleyin**.
<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/parts-0.webp" style="width:100%">
      <figcaption>0. Final Part Studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/parts-1a.webp" style="width:100%">
      <figcaption>1a. Şanzıman için layout sketch oluşturun. 20T dişliden 50T dişliye olan 2. kademe ile başlayın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/parts-1b.webp" style="width:100%">
      <figcaption>1b. 50T dişliye 12T motor pinion dişlisi olan 1. kademeyi çizin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/parts-1c.webp" style="width:100%">
      <figcaption>1c. Motorları 2.5" çapında bir daire olarak outline'ını çizin. Bu şanzıman için bitmiş layout sketch'tir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/parts-2.webp" style="width:100%">
      <figcaption>2. Plakanın profilini çizmek için yeni bir sketch oluşturun. Layout sketch'i referans alarak, 1.125" çapındaki rulman deliklerini ve 1.25" çapındaki motor boss deliklerini ekleyin. Ayrıca motor montaj deliklerini ekleyin. Geometriyi sol taraftan sağ tarafa ayna yapmak için <code>Mirror</code> sketch aracını kullanabilirsiniz. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/parts-3.webp" style="width:100%">
      <figcaption>3. Plakayı 1/4" kalınlığında extrude edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/parts-4.webp" style="width:100%">
      <figcaption>4. Şanzıman spacer'ını oluşturmak için <code>Robot Spacer</code> Featurescript'ini kullanın. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/hgIBEwiXtEc?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>5. İinci kademe şaftını oluşturmak için <code>Robot Shaft</code> Featurescript'ini kullanın. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/parts-6.webp" style="width:100%">
      <figcaption>6. Output şaftını oluşturmak için <code>Robot Shaft</code> Featurescript'ini kullanın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/parts-7.webp" style="width:100%">
      <figcaption>7. Plaka yüzünde bir sketch oluşturun ve pocketing kaburgaları için çizgiler çizin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/P3Snm7U0M_g?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>8. Önceki sketch tarafından oluşturulan kaburgaları seçerek plakayı pocket etmek için <code>Part Lighten</code> Featurescript'ini kullanın. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/parts-0.webp" style="width:100%">
      <figcaption>9. Tamamlanmış part studio. Sketch'leri, özellikleri ve parçaları adlandırın. Plakaların ve spacer'ın adını, malzemesini (6061 Aluminum) ve görünümlerini ayarlayın. </figcaption>
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

### Assembly Talimatları

**Ardından, kopyaladığınız belgede "Exercise #2 Assembly" sekmesine gidin** ve bu egzersizi tamamlamak için **slaytlardaki talimatları izleyin**.

<div class="slideshow-container">
  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/iz8vTGKxy7M?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>1. Part studioyu montaja ekleyin ve sadece şanzıman plakasını sabitleyin. Spacer'ı plakaya mate edin. Ardından, <code>Replicate</code> aracını kullanarak spacer'ı ve ilişkili mate'ini diğer spacer konumlarına replike edin. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/assy-2.webp" style="width:100%">
      <figcaption>2. Şanzıman plakasını kopyalayın ve yerine monte edin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/q-Ca99yyEDY?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>3. FRCDesignLib parçalarını kullanarak rulmanları ve şaftları monte edin. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/pEOxmxGMHPk?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>4. FRCDesignLib parçalarını kullanarak motoru ve motor pinion dişlisini monte edin. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/fMX8k8QicGQ?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>5. FRCDesignLib parçalarını kullanarak şaft spacer'larını ve dişlileri monte edin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/VJy8NSFISa0?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>6. FRCDesignLib parçalarını kullanarak şaft tutma boltlarını, motor boltlarını, şanzıman boltlarını ve somunları monte edin. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise2/assy-0.webp" style="width:100%">
      <figcaption>7. Tamamlanmış montaj. Parçaları klasörlere sıraladığınızdan ve replicate özelliklerinizi adlandırdığınızdan emin olun. </figcaption>
    </figure>
  </div>

  <!-- Next and previous buttons -->
  <button class="prev" onclick="plusSlides(-1,1)" style="background-color: #000; color: #fff;">&#10094;</button>
  <button class="next" onclick="plusSlides(1,1)" style="background-color: #000; color: #fff;">&#10095;</button>
  <!-- The dots/circles -->
  <div class="dotsContainer" style="text-align:center">
    <!-- Dots will be generated here -->
  </div>
</div>

!!! Success "Doğrulama"
    Sizin ve/veya takımınızın daha deneyimli bir üyesinin/mentorünün [**CAD'inizi incelemesini sağlayın!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"} Montajınızın 27 instance'ı olmalıdır.

Bu egzersizte, daha karmaşık şanzıman modelleme ve daha büyük montajları bir araya getirme pratiği yaptınız.



<br>

