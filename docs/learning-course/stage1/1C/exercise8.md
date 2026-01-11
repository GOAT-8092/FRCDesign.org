# 1C: Pratik Mekanizmalar

## Egzersiz 8: İndeksleyici Centering

Bu egzersizde, 9.5" çapındaki toplar için bir centering indexer modelleyeceksiniz, [1678'in 2022 indexer'ına](https://www.youtube.com/watch?v=RiUaItTKomUhttps://www.youtube.com/watch?v=RiUaItTKomU "1678 2022 Robot Reveal Video"){:target="\_blank"} benzer. Bu mekanizma belt'ler, zincir, gear ve tüp crush blokları içerir. Modelleme yaparken plaka sketch'lerine dikkat etmeniz önerilir.

### Part Studio Talimatları

Kopyalanmış belgenizdeki **"Exercise #8 Part Studio" sekmesine gidin** ve bu egzersiz için part studio'yu tamamlamak için **solution belgesine başvurun**. **Aşağıdaki talimat slaytları** sadece genel bir outline ve bazı önemli detaylar sağlar.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/parts-0.webp" style="width:100%">
      <figcaption>0. Final Part Studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/parts-1.webp" style="width:100%">
      <figcaption>1. Top plane üzerinde layout sketch oluşturarak başlayın.
                  Önceki egzersizde olduğu gibi, roller arasındaki mesafeyi tanımlamak için indexer wheel'ı yansıtıyoruz.
      </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/parts-2.webp" style="width:100%">
      <figcaption>2. Extrude Individual ve Tube Converter kullanarak ince cidarlı 2x1 tüpleri modelleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/parts-3.webp" style="width:100%">
      <figcaption>3. Üst plakaları ve alt plakaları modelleyin.
                  Üst plakalar aynı düzlemde olduğu için aynı sketch'de modellenebilir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/parts-4.webp" style="width:100%">
      <figcaption>4. İlk delik sırasına kadar kadar tüpün içine uzanan temel bir crush bloğu modelleyin. Bolt'ların geçmesi için yan delikleri eklediğinizden emin olun. IRL assembly sırasında kurulumu kolaylaştırmak için kenarları chamfer edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/parts-5.webp" style="width:100%">
      <figcaption>5. <code>Belt & Chain Gen</code> Featurescript'ini kullanarak belt'leri modelleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/parts-6.webp" style="width:100%">
      <figcaption>6. Shaft'ları <code>Robot Shaft</code> Featurescript ile modelleyin. Daha uzun shaft'ların kesin uzunluğu bu egzersiz için biraz keyfidir, sadece gösterildiği gibi yarı uzun yapın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/parts-7.webp" style="width:100%">
      <figcaption>7. <code>Part Lighten</code> featurescript kullanarak plakaları pocket edin.
                  Tüm rib'leri otomatik olarak seçmek için tüm bir sketch seçebileceğinizi hatırlayın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/parts-0.webp" style="width:100%">
      <figcaption>8. Özellikleri adlandırarak ve klasörlere organize ederek part studio'yu tamamlayın. Parça malzemelerini buna göre atayın.</figcaption>
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

**Sonra, kopyalanmış belgenizdeki **"Exercise #8 Assembly" sekmesine gidin** ve bu egzersiz için assembly'yi tamamlamak için **solution belgesine başvurun**. **Aşağıdaki talimat slaytları** sadece genel bir outline ve bazı önemli detaylar sağlar.

<div class="slideshow-container">
  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/assy-1.webp" style="width:100%">
      <figcaption>1. Part studio parçalarını assembly'ye ekleyin. Önceki gibi, rigid bileşenleri Origin Cube ile grup mate edin ve Origin Cube'u assembly origin'ine mate edin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/assy-2.webp" style="width:100%">
      <figcaption>2. 2" uzunluğunda, 3/8" OD plaka spacer'larını insert edin, fasten edin ve replicate edin.
                1.25" uzunluğunda, 3/8" OD motor spacer'larını insert edin, fasten edin ve replicate edin.
                Alt gear plakasını 2" spacer'a kopyalayın ve fasten edin.
                1/2" yuvarlatılmış hex shaft bearing'lerini insert edin, fasten edin ve replicate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/assy-3.webp" style="width:100%">
      <figcaption>3. 3D baskı crush bloğunu diğer tüp uçlarına kopyalayın, fasten edin ve replicate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/assy-4.webp" style="width:100%">
      <figcaption>4. Motoru, motor pulley'ini, 1/2" hex insert'li 48T 3D baskı HTD pulley'ini, 30T gear'ları ve FRCDesignLib'den yapılandırılabilir spacer yığınlarını insert edin ve fasten edin. Belt'i pulley'e fasten edin. Ayrıca shaft'ları fasten edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/assy-5.webp" style="width:100%">
      <figcaption>5. Alt belt pulley'lerini insert edin ve fasten edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/assy-6.webp" style="width:100%">
      <figcaption>6. FRCDesignLib'den 6" REV Omni-wheel'lerini ve 1/2" Hex MAXHub'ları insert edin ve fasten edin. Hub'ları wheel'lere fasten edin ve wheel assembly'lerini uzun shaft uçlarına fasten edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/assy-7.webp" style="width:100%">
      <figcaption>7. Wheel'ların ve plakalar arasındaki boşluğu doldurmak için 1/2" Hex spacer'ları insert edin, configure edin ve fasten edin. Bunlar istiflenmiş COTS spacer'lar veya tercihe bağlı olarak tek bir özel spacer olabilir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/assy-8.webp" style="width:100%">
      <figcaption>8. Gerekli tüm fastener'ları insert edin, fasten edin ve replicate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/indexer-centering/assy-0.webp" style="width:100%">
      <figcaption>9. Assembly'yi tamamlamak için, bileşenlerinizi klasörlere düzenleyin ve replicalarınızı adlandırın.</figcaption>
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
    Siz ve/veya ekibinizden daha deneyimli bir üye/mentor [**CAD'inizi gözden geçirsin!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="\_blank"} Her şey mevcutsa, doğru modellenmişse ve doğru assembly edildiyse, assembly'nizde yaklaşık 80 instance olmalıdır.

<br>
