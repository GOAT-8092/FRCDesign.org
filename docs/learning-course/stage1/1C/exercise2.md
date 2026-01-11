# 1C: Pratik Mekanizmalar

## Egzersiz 2: Dingil Silisi Rollers

Bu egzersizde, bazı dingil silisi roller modelleyeceksiniz. Silindirlerin, tekerleklerin veya hatta kolların döndürülmesi için "canlı" ve "ölü" olmak üzere iki dingil tipi kullanılabilir.

### Canlı ve Dingil Silisi Rollers

Stage 2'de canlı ve dingil silisi tasarımı hakkında daha fazla bilgi edineceksiniz, ancak şimdilik bilmeniz gereken tek şey, canlı dingil'de shaft'ı mekanizmayı döndürmek için güçlendirdiğimiz, dingil silisi'nde ise dönen parçayı doğrudan güçlendirdiğimizdir.
Canlı dingil'de shaft sabit bearingler üzerinde dönerken, dingil silisi'nde bearingler dönen parçadadır. Daha iyi anlamak için aşağıdaki görseli inceleyin.

???+ Örnek "Canlı vs Dingil Silisi Rollers"
    <figure>
      <img src="../images/dead-axle-rollers/dead-vs-live.webp" style="width:65%">
      <figcaption>Dingil silisi (sol) ve canlı dingil (sağ) roller'in kesit görünümü. Dingil silisi roller bearingler üzerinde durur ve doğrudan güçlendirilmelidir (bu durumda, entegre pulley yoluyla). Canlı dingil roller, hex shaft'ın daha aşağısındaki bir pulley'den güçlendirilir.</figcaption>
    </figure>

### Part Studio Talimatları

Kopyalanmış belgenizdeki **"Exercise #2 Part Studio" sekmesine gidin** ve bu egzersiz için part studio'yu tamamlamak için **slaytlardaki talimatları izleyin**.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-0.webp" style="width:100%">
      <figcaption>0. Final Part Studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-1.webp" style="width:100%">
      <figcaption>1. Layout Sketch için right plane üzerinde yeni bir sketch oluşturun. Pivot axle deliği ve etrafında bir bolt pattern ile başlayın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-2.webp" style="width:100%">
      <figcaption>2. Pivot deliğinin sol tarafındaki rollerlar arasında ilk belt run'ı sketchleyin.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-3.webp" style="width:100%">
      <figcaption>3. İlk belt run ile aynı uzunlukta ikinci bir belt run oluşturun.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-4.webp" style="width:100%">
      <figcaption>4. Rollerları temsil etmek için belt run'ların uçlarına 2" daireler ekleyin.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-5.webp" style="width:100%">
      <figcaption>5. Pivot noktasına doğru geriye dönük açılı ilk roller'den motor belt run'ını sketchleyin.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-6.webp" style="width:100%">
      <figcaption>6. Motoru temsil etmek için 60mm bir daire ekleyin, bu plakayı yaparken yararlı bilgi olacaktır.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-7.webp" style="width:100%">
      <figcaption>7. Layout sketch'ten offset bir plaka sketch oluşturun. Bu önceki egzersize benzer.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-8.webp" style="width:100%">
      <figcaption>8. Plaka sketch'ine bolt pattern ve pivot axle deliğini kopyalayarak başlatın ve rollerlar için bolt delikleri ekleyin. Ayrıca motor için bolt pattern ekleyin, bu önceki egzersizde aynı şekilde yapılmalıdır ancak 6 delikli pattern ile. Önceki gibi sadece 3'ünü gerçek delikler yapacağız. Geri kalanı construction daireler olacaktır.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-9.webp" style="width:100%">
      <figcaption>9. Önceki slaytta oluşturulan deliklere dayanarak plaka outlinesını çizin.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-10.webp" style="width:100%">
      <figcaption>10. Plakayı "Right" yönünde extrude edin.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-11.webp" style="width:100%">
      <figcaption>11. Motor belt'ini yapmak için Belt & Chain Gen kullanın. Belt'leri pulley'lere mate edeceğiniz için burada offset'ler önemli değil.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-12.webp" style="width:100%">
      <figcaption>12. İlk roller belt'ini yapmak için Belt & Chain Gen kullanın.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-13.webp" style="width:100%">
      <figcaption>13. İkinci roller belt'ini yapmak için Belt & Chain Gen kullanın.</figcaption>
    </figure>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/parts-0.webp" style="width:100%">
      <figcaption>14. Özellikleri adlandırarak ve klasörlere organize ederek part studio'yu tamamlayın. Plaka malzemesini polikarbonat olarak atayın. </figcaption>
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

**Sonra, kopyalanmış belgenizdeki **"Exercise #2 Assembly" sekmesine gidin** ve bu egzersizi tamamlamak için **slaytlardaki talimatları izleyin**.

<div class="slideshow-container">
  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/dead-axle-rollers/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/fDDM02mGCvg?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>1. Assembly'ye part studio'yu insert ederek başlayın ve origin cube ve plakayı bir araya gruplandırın. Sonra cube'u origin'e fasten edin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/0k2pSyg_nA0?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>2. Plakayı diğer tarafa kopyalamak için Assembly Mirror kullanın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/J_dtYxcaCL8?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>3. FRCDesignLib'den bir roller insert edin. Uzunluğun 24" olarak ayarlandığından ve bolt endcap'ların HTD seçeneğine ayarlandığından emin olun. İlk roller'ı side plate'deki deliklerden birine mate edebilirsiniz. Tek roller'ı diğer iki deliğe replicate edebilirsiniz. Gösterildiği gibi replicate için tüm assembly'yi seçtiğinizden emin olun.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/DqiNcoXHYNE?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>4. Belt'leri roller pulley'lere mate edin, belt'ler için center mate noktasını kullanın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/BnFXhMRt_us?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>5. Motoru, Pulley'i, Shaft Spacer'ları ve Shaft Bolt'u insert edin. Motor bileşenlerini bir araya assembly edin ve pulley'i belt'in merkezine mate edin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/WUW7gB-it7I?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>6. Her bileşenin yüzüne tıklayarak plaka ve motor arasındaki mesafeyi ölçün. Bu mesafeyi panonuza kopyalayın. FRCDesignLib Inserter'ı açın ve kopyaladığınız uzunlukta özel bir yuvarlak ID spacer insert edin. Diğer konfigürasyonları değiştirmenize gerek yok. Bu spacer'ı plakaya ekleyin ve diğer üç plaka deliğine eklemek için replicate kullanın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/FkXr6tEHoSc?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>7. Assembly'nize fastener ekleyin. Polikarbonat plakalara bolt'larken her bolt'ta washer kullanımına dikkat edin. Plakaların çatlamasını önlemek için en iyi uygulama washer kullanmaktır. Rollerlar 1/2" #10-32 bolt'larla bağlanmalıdır ve motor 1.75" #10-32 bolt'larla bağlanmalıdır.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
     <img src="../images/dead-axle-rollers/assy-0.webp" style="width:100%">
      <figcaption>8. Assembly'nizi klasörlerle organize edin</figcaption>
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
    Siz ve/veya ekibinizden daha deneyimli bir üye/mentor [**CAD'inizi gözden geçirsin!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"}.

### Benzersiz Parça Sayısını Minimize Etmek

3. roller'ın sadece bir ucuna belt bağlı olmasına rağmen her iki ucunda da 24T pulley olduğunu fark etmiş olabilirsiniz.
Yapılandırılabilir roller, belt olmayan uç için pulley seçmemenize izin verse de, benzersiz parça sayısını azaltmak için durumlar gibi bu durumlarda pulley'i tutmak avantajlı olabilir.
Bunu yaparak, tüm üç roller aynıdır, bu da parça takibi ve yedek parçaları kolaylaştırır.

<br>
