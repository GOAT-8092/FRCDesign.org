# 1D: Tasarım Metodolojisi - Basit Swerve Şasisi

## Şasi Düzen Çizimleri

Başlamak için, şasinin bir düzen çizimini oluşturacaksınız. Bu, sürüş tüplerinin boyutunu ve konumunu belirleyecektir. Düzen, şasinin yan ve üst görünümünden çizilecektir. Swerve şasiniz için 26" x 26" yapacaksınız.

### Talimatlar

Başlamak için **`Stage 1D Robot` adında yeni bir Onshape Dokümanı oluşturun** ve içinde **`Main Layout Sketch` adında yeni bir part studio oluşturun**. Ardından, origin küp oluşturmak için `Origin Cube` Featurescript'ini kullanın. Düzen çizimini tamamlamak için **slaytlardaki talimatları izleyin**.


<!-- <center>**Drivetrain Layout Sketch Slides**</center> -->
<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/layout-sketches/layout-0.webp" style="width:100%">
      <figcaption>0. Son düzen çizimi.</figcaption>
    </figure>
  </div>



  <div class="mySlides fade">
    <figure>
      <img src="../images/layout-sketches/layout-1.webp" style="width:100%">
      <figcaption>1. Şasinin yan profilini Right Plane üzerinde çizin. Tüpü yerden 1.75" uzaklığa yerleştiriyoruz, bu MK4i modülleri için yerden tüpün altına kadar ofsettir.
                  Ardından, tekerleğin kapladığı alanı temsil eden tekerleks boşluk kutusunu çizin.
                  MK4i modülleri için kutu 4.625" genişliğindedir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/fE7Zhv1DYt0?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>2. Yan düzenin dikey çizgisindeki alt mate connector'ü kullanarak üst düzen çizimini oluşturun. Sketch düzlemleri için otomatik olarak oluşturulan mate connector'leri kullanmak çok kullanışlı bir araçtır. Üst görünümü almak için view cube üzerindeki "Top" butonuna basın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/HfoS699wNPc?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>3. Şasinin üst anahatını çizin. Dikdörtgeni bir kare yapın ve kenar uzunluğunu yan düzen tüpünün uzunluğuna eşit ayarlayın. Bu, üst düzenin boyutunun her zaman yan düzenle eşleşmesini sağlar, bu da tasarımı parametrik hale getirir. Sketch boyutu olmamasına rağmen sketch'in tamamen tanımlanmış olduğuna dikkat edin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/layout-sketches/layout-4.webp" style="width:100%">
      <figcaption>4. Tüpleri çizmek için, önceki kareden 1" daha küçük bir kare çizin.
                  Bu, dış çerçeveyi oluşturan dört 2"x1" tüpü temsil edecektir.
                  Ardından, 2"x2" tüpün üst profilini çizin.
                  Sağ alt köşede, kenardan her biri 4.25" ofsetli iki çizgi çizin.
                  Bu MK4i modülleri için gereken ofsettir. Diğer modüller farklı olacaktır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/5st3BiDfGdY?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>5. Dört tüpün tümü için kesiyi uygulamak için, çizgileri dört köşeye kopyalamak için <code>Circular Pattern</code> sketch aracını kullanırız.
                  <code>Circular Pattern</code> için önce örnek sayısını ve ardından dönme eksenini tanımlarız.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/layout-sketches/layout-0.webp" style="width:100%">
      <figcaption>6. Son olarak, sketch'lerinizi adlandırın ve özellik ağacındaki klasörlere düzenleyin. Sketchleriniz tamamen tanımlanmış olmalıdır.</figcaption>
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

Önceden açıklandığı gibi, bu üsten aşağı modelleme yöntemi çok güçlüdür çünkü en önemli boyutları tek bir yerde yakalamanızı sağlar. Ancak, düzen çizimlerini fazla detaylandırmamaya dikkat etmelisiniz. 2. Aşama boyunca düzen çizimleri pratiği yapacaksınız ve 3. Aşama'da çoklu belge uygulamalarıyla birlikte kullanarak tüm bir robot tasarlayacaksınız.

<br>
