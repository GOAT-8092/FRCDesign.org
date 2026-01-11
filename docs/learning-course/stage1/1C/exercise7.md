# 1C: Pratik Mekanizmalar

## Egzersiz 7: Dikey Rollers

Bu egzersizde, bazı dikey rollers modelleyeceksiniz. Bu mekanizma Configurable Tube Roller System assembly'sini ve 3D baskı motor spacer'ını içerir. Modelleme yaparken layout sketch ve assembly mating'e dikkat etmeniz önerilir.

### Parça Sayısını Azaltmak İçin 3D Baskı
3D baskı spacer blokları oluşturmak için kullanılabilir.
İki bileşeni bağlamak için birden fazla spacer kullanmak yerine, tüm spacer'ları tek bir parçada birleştiren 3D baskı bir blok kullanmayı seçebiliriz, bu parça sayısını azaltır ve assembly'yi kolaylaştırır. Bu kavram ayrıca parça sayısını azaltmak için egzersiz 4'te climb hook üzerinde de kullanıldı.

Eğer bir 3D yazıcınız varsa, bu iyi bir seçenek olabilir.

???+ örnek "3D Baskı Spacer Bloğu"
    <figure>
      <img src="../images/vertical-rollers/3dp-spacer.webp" width="65%">
      <figcaption>Birden fazla spacer tek bir 3D baskı blokta birleştirilebilir parça sayısını azaltmak için. </figcaption>
    </figure>

### Part Studio Talimatları

Kopyalanmış belgenizdeki **"Exercise #7 Part Studio" sekmesine gidin** ve bu egzersiz için part studio'yu tamamlamak için **solution belgesine başvurun**. **Aşağıdaki talimat slaytları** sadece genel bir outline ve bazı önemli detaylar sağlar.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/parts-0.webp" style="width:100%">
      <figcaption>0. Final Part Studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/parts-1.webp" style="width:100%">
      <figcaption>1. Origin'den 3" yukarı offset bir mate connector üzerinde layout sketch oluşturarak başlayın.
                  Seri olarak birden fazla belt bağladığımız için sürtünmeyi azaltmak için her belt c-c'den 0.015" çıkarıyoruz. Bu verimliliği artırır, backlash'e mal olur ancak bu mekanizma için önemli değildir</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/parts-2.webp" style="width:100%">
      <figcaption>2. Rollers ve tüp konumu için bir sağ el referansı oluşturmak için <code>Mirror</code> sketch aracını kullanın. Roller konumlarını sürmek için roller çiftleri arasındaki mesafeyi kullanın. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/parts-3.webp" style="width:100%">
      <figcaption>3. Alt plakayı oluşturun. Sonra, alt plakadan 7" offset üst plakayı oluşturun.
                    Solution belgesindeki plaka sketch'lerine yakın dikkat edin.
                    1x1" tüp plug'unun birbirinden 3/8" aralıklı 4 delikli kare bir pattern gerektirdiğini unutmayın.
                    Hepsine ihtiyacımız yok bu yüzden sadece 2'sini kullanacağız.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/parts-4.webp" style="width:100%">
      <figcaption>4. İnce cidarlı 1x1 tüpü sketchleyin, extrude edin, sonra tube convert edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/parts-5.webp" style="width:100%">
      <figcaption>5. 3D baskı motor spacer bloğunu modelleyin ve 1" uzunluğunda extrude edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/parts-6.webp" style="width:100%">
      <figcaption>6. Belt'leri modelleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/parts-0.webp" style="width:100%">
      <figcaption>7. Özellikleri adlandırarak ve klasörlere organize ederek part studio'yu tamamlayın. Parça malzemelerini buna göre atayın.</figcaption>
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

**Sonra, kopyalanmış belgenizdeki **"Exercise #7 Assembly" sekmesine gidin** ve bu egzersiz için assembly'yi tamamlamak için **solution belgesine başvurun**. **Aşağıdaki talimat slaytları** sadece genel bir outline ve bazı önemli detaylar sağlar.

<div class="slideshow-container">
  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/assy-1.webp" style="width:100%">
      <figcaption>1. Part studio parçalarını assembly'ye ekleyin. Önceki gibi, rigid bileşenleri Origin Cube ile grup mate edin ve Origin Cube'u assembly origin'ine mate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/assy-2.webp" style="width:100%">
      <figcaption>2. Dikey 1x1 tüpe 1x1 Tüp Tapalarını ekleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/assy-3.webp" style="width:100%">
      <figcaption>3. Assembly'ye bir Kraken X44 ve 12t pulley insert edin. Pulley'i motora mate edin ve motoru spacer'a fasten edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/assy-4.webp" style="width:100%">
      <figcaption>4. FRCDesignLib'den "Tube Roller System" assembly'sini insert edin.
                  Genel roller uzunluğunu 7" olarak ayarlayın ve her uçta 24T pulley'ler kullanın.
                  Diğer 2 roller'ı kopyalayın ve fasten edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/assy-5.webp" style="width:100%">
      <figcaption>5. Belt'leri roller pulley'lere fasten edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/assy-6.webp" style="width:100%">
      <figcaption>6. Gerekli tüm fastener'ları insert edin, fasten edin ve replicate edin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/assy-7.webp" style="width:100%">
      <figcaption>7. Sol taraf assembly'sini sağ tarafa kopyalamak için Assembly Mirror kullanın. Yeni parçalar yapmamak için tüm öğelerin mirror stratejisini transform olarak ayarladığından emin olun.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/vertical-rollers/assy-0.webp" style="width:100%">
      <figcaption>8. Instance'larınızı klasörlere düzenleyerek assembly'nizi tamamlayın.</figcaption>
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
    Siz ve/veya ekibinizden daha deneyimli bir üye/mentor [**CAD'inizi gözden geçirsin!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"} Assembly'nizin yaklaşık 25 instance'ı olmalıdır.


<br>
