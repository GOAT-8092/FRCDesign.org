# 1C: Pratik Mekanizmalar

## Egzersiz 6: Yön Değişimi

Bu egzersizde, yön değiştirme dişlisi olan bir power transmission modelleyeceksiniz.
Bu mekanizma motorun yönünü tersine çeviren 1:1 dişli transmission özelliğine sahiptir, bu aynı motorla güçlendirilen ancak zıt yönlerde dönen iki farklı shaft istediğinizde yararlı olabilir.
Modelleme yaparken layout ve plaka sketch'lerine dikkat etmeniz önerilir.

### 3D Baskı, COTS ve Özel Alüminyum Spacer'lar
Şimdiye kadar, hem `Spacer` Featurescript ile oluşturulan özel spacer'ları hem de FRCDesignLib'den COTS 3/8" OD spacer'ları ([WCP Aluminum Spacer'lar](https://wcproducts.com/products/aluminum-spacers "WCP Aluminum Spacers Product Page"){:target="_blank"}) kullandınız.
COTS veya özel spacer kullanmanın artıları ve eksileri vardır ve ekibinizle tartışmalısınız.

3D baskı spacer'lar, 3D baskıları olan takımlar için harika bir seçenektir, ucuzdurlar ve kolayca üretilebilirler.
Alüminyum spacer kullanmak istiyorsanız ancak bunları kesmek için makinelere (örneğin bir torna) erişiminiz yoksa, COTS alüminyum spacer'lar iyi bir seçenek olabilir çünkü önceden stoklanabilirler.
Ancak, pahalı olabilirler ve sadece belirli uzunluklarda gelirler, ancak standart spacer uzunlukları için tasarlayarak bunu kolayca aşabilirsiniz.

???+ Örnek "Spacer Stoğu"
    <figure>
      <img src="../images/direction-swap/spacers.webp" width="100%">
      <figcaption>Spacer'lar 3D baskı (sol), COTS ön kesilmiş spacer'lar (orta) veya spacer stock'tan (sağ) evde üretilebilir. (Görüntü Kaynağı: WCP)</figcaption>
    </figure>

Modelleme yaparken, evde üreteceğiniz spacer'lar (örneğin 3D baskı veya [yuvarlak tube stock](https://wcproducts.com/products/shaft-stock "WCP Tube Stock Product Page"){:target="_blank"} kullanarak) için `Spacer` Featurescript'i kullanmanız ve COTS spacer'lar için yapılandırılabilir FRCDesignLib spacer'larını kullanmanız önerilir.
Bu, hangi parçaların özel ve hangilerinin COTS olduğunu netleştirmeye yardımcı olur.

### Part Studio Talimatları

Kopyalanmış belgenizdeki **"Exercise #6 Part Studio" sekmesine gidin** ve bu egzersiz için part studio'yu tamamlamak için **solution belgesine başvurun**. **Aşağıdaki talimat slaytları** sadece genel bir outline ve bazı önemli detaylar sağlar.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/parts-0.webp" style="width:100%">
      <figcaption>0. Final Part Studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/parts-1.webp" style="width:100%">
      <figcaption>1. Right plane üzerinde layout sketch oluşturarak başlayın. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/parts-2.webp" style="width:100%">
      <figcaption>2. Right plane'den 0.5" offset bir mate connector'ü sketch plane olarak kullanarak plakayı sketchleyin.
                  Plakanın kenarlarını tanımlamak için kullanılan clearance'lara yakın dikkat edin.
                  Motorun sol tarafındaki iki spacer'ın konumu, 3/8" OD spacer ve 2.5" motor clearance daire arasındaki teğetlik tarafından belirlenir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/parts-3.webp" style="width:100%">
      <figcaption>3. Sol gear ve spacer arasındaki mesafeyi göstermek ve yeterli clearance olduğunu doğrulamak için bir <code>Driven Dimension</code> kullanın. Driven dimension, driving dimension'in aksine, seçilen öğeler arasındaki mesafeyi sadece raporlar ve sketch geometrisini tanımlamadığını belirtmek için soluk gridir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/parts-4.webp" style="width:100%">
      <figcaption>4. Plakayı Right plane boyunca yansıtın ve motor cutout ekleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/parts-5.webp" style="width:100%">
      <figcaption>5. COTS spacer kullanmayı seçmezseniz, plaka spacer'ını oluşturmak için <code>Robot Spacer</code> Featurescript'ini kullanabilirsiniz.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/parts-6.webp" style="width:100%">
      <figcaption>6. Tüm shaft'ları ve belt'leri modelleyin. Bu noktada <code>Robot Shaft</code> ve <code>Belt & Chain Gen</code> Featurescripts'lerini kullanmakta çok rahat hissetmelisiniz.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/parts-7.webp" style="width:100%">
      <figcaption>7. İki plakayı pocket edin. Plakalar motor cutout haricinde aynı olduğu için, her iki plakayı pocket etmek için aynı sketch'i kullanabilirsiniz. Ribs ile sadece bir sketch oluşturun.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/parts-0.webp" style="width:100%">
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

**Sonra, kopyalanmış belgenizdeki **"Exercise #6 Assembly" sekmesine gidin** ve bu egzersiz için assembly'yi tamamlamak için **solution belgesine başvurun**. **Aşağıdaki talimat slaytları** sadece genel bir outline ve bazı önemli detaylar sağlar.

<div class="slideshow-container">
  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/assy-1.webp" style="width:100%">
      <figcaption>1. Part studio parçalarını assembly'ye ekleyin. Önceki gibi, rigid bileşenleri Origin Cube ile grup mate edin ve Origin Cube'u assembly origin'ine mate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/assy-2.webp" style="width:100%">
      <figcaption>2. Spacer'ı plakaya fasten edin ve replicate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/assy-3.webp" style="width:100%">
      <figcaption>3. Bearing'leri insert edin, fasten edin ve replicate edin. Ayrıca FRCDesignLib'den 2" flex wheel ve Kraken X60 motor insert edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/assy-4.webp" style="width:100%">
      <figcaption>4. Pulley'leri ve spacer'ları insert edin ve fasten edin.
                  Pulley'ler için, FRCDesignLib'den 1/2" hex insert'li 3D baskı HTD pulley'leri kullanabilirsiniz.
                  Ayrıca belt'leri yerine fasten edin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/assy-5.webp" style="width:100%">
      <figcaption>5. FRCDesignLib'den yapılandırılabilir bir spacer yığını insert edin. Uzunluk, pulley ve flex wheel arasındaki mesafe olmalıdır. Spacer yığını muhtemelen bir hata gösterecektir. Bu hata, yığında bulunmayan spacer uzunluklarını seçerek temizlenebilir. Alternatif olarak, kendi COTS spacer yığınızı yapabilir veya tek bir uzun özel spacer kullanabilirsiniz.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/assy-6.webp" style="width:100%">
      <figcaption>6. Tasarımı tamamlamak için gerekli tüm fastener'ları ekleyin ve replicate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/direction-swap/assy-0.webp" style="width:100%">
      <figcaption>7. Assembly'yi tamamlamak için, bileşenlerinizi klasörlere düzenleyin ve replicalarınızı adlandırın.</figcaption>
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
    Siz ve/veya ekibinizden daha deneyimli bir üye/mentor [**CAD'inizi gözden geçirsin!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"} Assembly'nizin yaklaşık 40 instance'ı olmalıdır.


### Driving ve Driven Dimension'lar

Sketch'lerde, driving dimension'lar geometriyi tanımlar ve kontrol eder, siyah görünür ve düzenlenebilir.
Driven dimension'lar ise açık gri renktedir ve mevcut geometriyi yansıtır, onu değiştirmez, belirli bir clearance veya kalınlığı sürdürmek gibi tasarım amacını korumak için kullanışlıdır.

Aralarında geçiş yapmak için dimension'ın üzerine sağ tıklayın ve bağlam menüsünden "Driving/Driven"ı seçin - yeni bir dimension sketch'i over-constrain ederse veya geometriyi değiştirmeden incelemeniz gerektiğinde kullanışlıdır.

!!! tip "Driving ve Driven Dimension'lar Arasında Geçiş"
    <figure>
      <video width="100%" controls>
        <source src="../images/direction-swap/driven-dims.webm" type="video/webm">
        Tarayıcınız video etiketini desteklemiyor.
      </video>
      <figcaption>Dimension'ın üzerine sağ tıklayarak driving'den driven'e ve tam tersine geçin. Driven dimension'ın diğer özelliklere göre güncellendiğine dikkat edin.</figcaption>
    </figure>

<br>
