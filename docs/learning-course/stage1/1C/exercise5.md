# 1C: Pratik Mekanizmalar

Egzersiz 5'ten başlayarak, sadece tasarım sürecinin bir outline'ı ve önemli detaylar size sağlanacaktır. Bu, egzersizlerin daha az rehberlik olduğu stage 2 için sizi hazırlamak içindir.

Part studio'larınız ve assembly'lerinizde tasarım amacını yakalamaya ve en iyi uygulamaları sürdürmeye odaklanın. Solution belgesinin iş akışını izleyin.

## Egzersiz 5: Ters Çevrilmiş Şanzıman

Bu egzersizde, iki motorlu, iki kademeli ters çevrilmiş bir şanzıman modelleyeceksiniz. Bu tür şanzımanlara "ters çevrilmiş" denir çünkü output shaft input motorların ters yönüne işaret eder. Bu tarz şanzıman bazı durumlarda paketleme kısıtlamalarını karşılamak için istenebilir. Bu şanzıman ayrıca zincir gerginliği mekanizması olarak da görev yapar, şanzımanın zincir gerginliğini ayarlamak için montaj tüpü boyunca kaymasına izin verir. Hala servis yapılabilirken backlash'i önlemek için kolayca gerginleşmiş bir zincire sahip olmak önemlidir.

### Part Studio Talimatları

Kopyalanmış belgenizdeki **"Exercise #5 Part Studio" sekmesine gidin** ve bu egzersiz için part studio'yu tamamlamak için **solution belgesine başvurun**. **Aşağıdaki talimat slaytları** sadece genel bir outline ve bazı önemli detaylar sağlar.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/parts-0.webp" style="width:100%">
      <figcaption>0. Final Part Studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/parts-1.webp" style="width:100%">
      <figcaption>1. Şanzımanın monte olduğu tüpü modelleyerek başlayın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/parts-2.webp" style="width:100%">
      <figcaption>2. Tüp yüzünde layout sketch oluşturun. Layout sketch'e sadece gerekli bilgileri eklediğinizi hatırlayın. Bu durumda, sadece gear PD'leri ve motor OD'leri gereklidir. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/parts-3.webp" style="width:100%">
      <figcaption>3. Outer plate'i sketchleyin. Motoru tutmak için sadece iki cıvata gereklidir ve motor pinion ile gear arasındaki c-c çizgisine dik bir çizgi oluşturan iki deliği seçin. Bu, motor bolt'larının her zaman erişilebilir olmasını sağlar. Alt montaj bolt'ları normal delikler yerine slots olarak modellenmiştir. Bu, zinciri germek için tüm şanzımanın tüp boyunca kaymasına izin verir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/parts-4.webp" style="width:100%">
      <figcaption>4. Inner plate'i sketchlerken, motor ve inner plate'ler arasında clearance olduğunu doğrulayın. Plaka contour'unun pürüzsüz olması için tüm kenarların teğetliğine yakın dikkat edin. Ayrıca plakanın arka tarafının tüp mesafesinin çoğu için düz kaldığından emin olun. Bu düz yüzey, zinciri gergin tutmak için bir bolt tarafından itilir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/parts-5.webp" style="width:100%">
      <figcaption>5. Tüpün dışında küçük bir crush plaka modelleyin. Önceki egzersizde açıklandığı gibi bu, bolt kuvvetini yayarak tüpün assembly sırasında ezilmesini önler.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/parts-6.webp" style="width:100%">
      <figcaption>6. Şanzıman shaft'larını yapmak için <code>Robot Shaft</code> Featurescript'ini kullanın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/parts-7.webp" style="width:100%">
      <figcaption>7. Şanzıman plate'lerini pocket edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/parts-0.webp" style="width:100%">
      <figcaption>8. Assembly için hazırlanın, parçaları organize edin ve özellikleri adlandırın.</figcaption>
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

**Sonra, kopyalanmış belgenizdeki **"Exercise #5 Assembly" sekmesine gidin** ve bu egzersiz için assembly'yi tamamlamak için **solution belgesine başvurun**. **Aşağıdaki talimat slaytları** sadece genel bir outline ve bazı önemli detaylar sağlar.

<div class="slideshow-container">
  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </figure>
  </div>

  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/assy-1.webp" style="width:100%">
      <figcaption>1. Frame, şanzıman plate'leri, şanzıman spacer'ı ve shaft'ları assembly'ye ekleyin. Önceki gibi, rigid bileşenleri Origin Cube ile grup mate edin ve Origin Cube'u assembly origin'ine mate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/assy-2.webp" style="width:100%">
      <figcaption>2. Motorları ve bearing'leri insert edin ve fasten edin. Motoru doğru pinion ve shaft spacer'ları ile assembly ettiğinizden emin olun.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/assy-3.webp" style="width:100%">
      <figcaption>3. Power transmission bileşenlerini (gear'lar, pinion'lar, spacer'lar ve sprocket) insert edin ve fasten edin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/assy-4.webp" style="width:100%">
      <figcaption>4. Parça sayısını azaltmak için gear'ın her tarafında iki 1/4" spacer yerine tek bir 1/2" spacer kullanıyoruz. Gerçek hayatta, tek bir spacer varsa assembly çok daha kolaydır ve bearing'ler arasında gear'ı ortalamak için hiçbir maddi fayda yoktur.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/assy-5.webp" style="width:100%">
      <figcaption>5. Crush plakayı kopyalayın ve tüpün diğer tarafına mate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/assy-6.webp" style="width:100%">
      <figcaption>6. Az önce eklediğiniz crush plakanın diğer tarafına bir nutstrip fasten edin, bir bolt şanzıman plakasının düz yüzüne basın. Önceki açıklandığı gibi bu, şanzımanın zincir kuvvetinden kaymasını önler.</figcaption>
    </figure>
  </div>

  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/assy-7.webp" style="width:100%">
      <figcaption>7. Assembly'ye fastener ekleyin. Slotted deliklerdeki tüm fastener'ların bolt yükünü slot üzerinde düzgün bir şekilde yaymak için washer'lara sahip olduğundan emin olun. Hem bolt başında hem de nut'ta washer olmalıdır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flipped-gearbox/assy-0.webp" style="width:100%">
      <figcaption>8. Assembly'yi tamamlamak için, bileşenlerinizi klasörlere düzenleyin ve replicalarınızı adlandırın.</figcaption>
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
    Siz ve/veya ekibinizden daha deneyimli bir üye/mentor [**CAD'inizi gözden geçirsin!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"} Assembly'nizin 30 instance'ı olmalıdır.

### Interferans Tespiti

Hataları CAD'de yakalayın, gerçek hayatta değil! Her zaman CAD modellerinizi interferans gibi hatalar için iki ve üç kez kontrol edin. Yanlış bir parça slip through olur ve üretilirse, CAD'inizin doğruluğunu doğrulamak için ekstra 10 dakika size saatlerce yeniden çalışmadan tasarruf edebilir.

!!! warning "Interferans Tespiti"
    Check Interference aracı ile bir interferans tespit edilirse, kesişen hacimleri kırmızı ile vurgular.
    <figure>
      <img src="../images/flipped-gearbox/interference-check.webp" style="width:80%">
      <figcaption>Check Interference aracı tarafından tespit edilen motor ve plaka arasındaki interferans.</figcaption>
    </figure>

<br>
