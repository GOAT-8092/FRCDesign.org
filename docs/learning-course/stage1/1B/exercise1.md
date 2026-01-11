


# 1B: Güç Aktarımları


## Pratik Egzersizler
Pratik yapma zamanı! Daha önce Stage 1A Egzersizler Dokümanı ile yaptığınız gibi, aşağıdaki düğme aracılığıyla **Stage 1B Egzersizler Dokümanı'nın bir kopyasını oluşturarak** başlayın. Her egzersizin bir klasörü, bir "referans" sekmesi (final modelin nasıl görünmesi gerektiğine dair bir önizleme) ve egzersizi yapmanız için bir veya iki sekmesi vardır. Çalışmanızı sonradan kontrol etmeniz için çözümler de 1B Egzersiz Çözümleri Dokümanı'nda sağlanmıştır.

<center markdown>[1B Exercises Document (COPY THIS)](https://cad.onshape.com/documents/ce41613fac38db8c00e65020/w/a65651477167d5e36fe871c0/e/755940e52d82bddfdf7be61e "1B Exercises Onshape Document"){:target="_blank" .md-button .md-button--primary }
[1B Exercise Solutions](https://cad.onshape.com/documents/c6a8ec29479a2578841fb9f2/w/85094b3baa15a05c873920c9/e/47efe87a05a8318bffd60957 "1B Exercise Solutions Onshape Document"){:target="_blank" .md-button .md-button--primary } </center>

## Egzersiz 1: Basit Şanzıman

Bu egzersizde, basit bir tek kademeli şanzıman modelleyip monte edeceksiniz. Bu egzersizin amacı, çok basit bir dişli aktarımının nasıl modelleneceğini tanıtmaktır. Ayrıca, [`Robot Shaft` ve `Robot Spacer` Featurescripts`](https://cad.onshape.com/documents/9cffa92db8b62219498f89af/v/0d2ae9a0b843b03bdb63724f/e/99672d1e329b38e647d90146 "Alex's Featurescripts Onshape Document"){:target="_blank"} ve `Replicate` aracının nasıl kullanılacağını öğreneceksiniz. Ayrıca, dişliler ve motorlar gibi fastener dışındaki bileşenler için [FRCDesignLib parça kütüphanesini](../../course-setup/required-course-tools/part-library.md "Adding FRCDesignApp Tutorial Page"){:target="_blank"} kullanacaksınız.

!!! Not
    Egzersiz 1, CAD modellerine donanım (bolt ve cıvata) ekler. Donanım standartları hakkında daha fazla bilgi için [Design Handbook](/design-handbook/structure/fasteners/ "Design Handbook Fasteners Page"){:target="_blank"} sayfasını okuyabilirsiniz.

### Layout Sketches

Layout sketch, tasarımın geometrisini kesin detayları belirtmeden yakalayan bir taslaktır.
Sanki evin çerçevesi gibidir - genel yapıyı ve ana bileşenler arasındaki ilişkileri tanımlar, ancak duvarlar veya boya gibi son detayları içermez.
Ana boyutları layout sketch içinde tutmak, gerekli olduğunda kolayca ayarlamayı sağlar. Bundan sonra neredeyse tüm tasarımlarımızda layout sketch kullanacağız.

!!! İpucu "Motor"
    Bu egzersizte kullanılan motor, Falcon 500 adında bir CIM sınıfı motordur. Satın alma için durdurulmuş olsa da, birçok takım hala bazılarına sahiptir ve [Motors page](motors.md) sayfasında tartışıldığı gibi çoğu diğer FRC motorunun kullandığı aynı 2" montaj deliği desenini kullanırlar.

### Part Studio Talimatları
Kopyaladığınız belgede **"Exercise #1 Part Studio" sekmesine gidin** ve part studioyu tamamlamak için **slaytlardaki talimatları izleyin**.


<!-- <center>**Exercise 1 Instruction Slides**</center> -->
<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-0.webp" style="width:100%">
      <figcaption>0. Tamamlanmış Part Studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-1.webp" style="width:100%">
      <figcaption> 1. Şanzıman için layout sketch ile başlayın. 60T ve 12T dişliler için pitch çemberlerini çizin. Dişliler arasındaki merkezden merkeze mesafeyi kısıtlamak için pitch çemberlerini teğet olarak ayarlayın. İki dişlinin merkezlerini dikey olarak kısıtlayın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-2.webp" style="width:100%">
      <figcaption> 2. Motorun bağlı olduğu 12T dişlinin etrafına, motorun outline'ını temsil eden 2.5" çapında bir daire ekleyin. Layout sketch artık tamamlandı.  </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-3.webp" style="width:100%">
      <figcaption> 3. Motor plakası için yeni bir sketch oluşturun. Layout'u referans olarak kullanarak, rulman için 1.125" delik ve motor boss'u (motordan çıkan çıkıntı) için 1.25" delik çizin. Üretim süreçlerinize ve toleranslarınıza bağlı olarak, rulman deliklerini nominalden (1.125") biraz daha büyük veya daha küçük çizmeniz gerekebileceğini unutmayın. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-4.webp" style="width:100%">
      <figcaption> 4. Motor için 2" bolt daire üzerinde iki montaj deliği ekleyin. Sadece iki montaj deliği kullanırken, dairesel pattern kullanmaya bir alternatif olarak 2" <it>construction circle</it> çizip ve boyutlandırmak, sonra boltları daire üzerine çizmektir. Deliklerin açısını da kısıtladığınızdan emin olun; biz yatay kısıtlama kullandık.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-5.webp" style="width:100%">
      <figcaption>  5. İki plakayı birleştirmek için dört bolt deliği ekleyin. Construction geometrisini oluşturmak için center rectangle kullanın, böylece delikleri kısıtlamak için sadece iki boyut gerekir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-6.webp" style="width:100%">
      <figcaption> 6. Centerpoint arcs, çizgiler ve sketch mirror aracını kullanarak, deliklerin ve motor outline'ın etrafında plaka outline'ını çizin. Origin'in simetri çizgisi boyunca akıllı yerleşimi, right plane'i kullanarak plaka outline'ını ayna yapmanızı sağlar. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-7.webp" style="width:100%">
      <figcaption> 7. Motor plakasını 1/4" kalınlığında extrude edin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-8.webp" style="width:100%">
      <figcaption> 8. #10 serbest geçme, 3/8" ÇD (otomatik), 3/4" uzunlukta spacer eklemek için <code>Robot Spacer</code> Featurescript'i kullanın. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-9.webp" style="width:100%">
      <figcaption> 9. Spacer yüzünde outer plaka sketch'ini oluşturun. Motor plakasının deliklerini ve kenarlarını projeyecek şekilde <code>Use</code> sketch aracını kullanın, ancak <code>arc</code> araçlarından birini kullanarak üstte yuvarlak bir kesik ekleyin. Sketch'in büyük ölçüde <code>tangent</code>, <code>equal</code> ve <code>vertical</code> gibi kısıtlamalar kullanılarak tanımlanabileceğini unutmayın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-10.webp" style="width:100%">
      <figcaption>10. Outer plakayı 1/4" kalınlığında extrude edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/RDXcECn8uSI?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption>11. Output şaftı modellemek için <code>Robot Shaft</code> Featurescript'ini kullanın. Kullanılan ayarları izleyin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/parts-0.webp" style="width:100%">
      <figcaption> 12. Tamamlanmış part studio. Önemli sketch'leri ve özellikleri adlandırın. Plakaların ve spacer'ın adını, malzemesini (6061 Aluminum) ve görünümlerini parça listesinde parçalara sağ tıklayarak ayarlayın. Şaftın malzemesi otomatik olarak <code>Robot Shaft</code> Featurescript'inden belirlenir.</figcaption>
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

Montajı yaparken, **motor pinion dişlisini motora mate ederken bazı zorluklar yaşayabilirsiniz**.

Bir yüzdeki görünür mate connectorları, bir mate connector'a basmadan önce `Shift` tuşuna basarak kilitleyebilirsiniz. Bir eğitim için aşağıdaki videoyu izleyin.

<div class="slide-content">
  <iframe src="https://www.youtube.com/embed/zI8wBHeTfdc?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
  <figcaption>Shift tuşunu kullanarak mate sırasında inference'ları kilitleme</figcaption>
</div>


**Şimdi kopyaladığınız belgede "Exercise #1 Assembly" sekmesine gidin** ve **slaytlardaki talimatları izleyerek** egzersizi tamamlayın.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/kChIFuuLahU?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption> 1. Part studioyu montaja ekleyin ve şanzıman plakasını sabitleyin. İki plakayı birlikte group mate edin, sonra spacer'ı motor plakasına mate edin. Ardından, <code>Replicate</code> aracını kullanarak spacer'ı ve ilişkili mate'ini diğer spacer konumlarına replike edin. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/gKP-n5eKmjE?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption> 2. FRCDesignLib'den parçaları kullanarak rulmanları ve şaftı monte edin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/ZJCs0ms3I8A?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption> 3. FRCDesignLib'den parçaları kullanarak motoru ve motor pinion dişlisini monte edin. Motoru motor pinion'a fasten etmek için mate inference kilitlemeyi kullanmanız gerekecek: Nasıl yapılacağını öğrenmek için yukarıdaki dropdown'a bakın. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/mMP-kkl6AuY?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption> 4. FRCDesignLib'den parçaları kullanarak şaft spacer'ını ve dişliyi monte edin. Configurable parçaların instance listesinde mavi ızgara ikonu vardır. Dişlinin diş sayısının mate ettikten sonra 40T'den 60T'ye nasıl değiştirildiğine dikkat edin. Bu gibi configurable bileşenleri kullanmak, modellerinizi daha parametrik yapar çünkü bileşeni yeniden eklemeye ve mate etmeye gerek kalmadan değiştirebilirsiniz. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/SytVbO_-BrM?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption> 5. FRCDesignLib'den şaft tutma boltlarını ekleyin. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
       <iframe src="https://www.youtube.com/embed/D4OWWMYYwWM?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption> 6. Motor boltlarını, şanzıman boltlarını ve somunları FRCDesignLib parçalarını kullanarak ekleyin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise1/assy-0.webp" style="width:100%">
      <figcaption>7. Tamamlanmış montaj. Parçalarınızı klasörlere sıraladığınızdan ve replicate özelliklerinizi adlandırdığınızdan emin olun. </figcaption>
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
    Sizin ve/veya takımınızın daha deneyimli bir üyesinin/mentorünün [**CAD'inizi incelemesini sağlayın!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"} Montajınızın 18 Instance'ı olmalı ve yaklaşık 2.3 lbs ağırlığında olmalıdır.


### Configurable Parçalar

Bu egzersizte ilk şanzımanınızı yaptınız. Bunu yaparken, aynı parçanın varyasyonlarına izin veren güçlü bir araç olan parça konfigürasyonlarını da kullandınız. FRCDesignLib'den eklediğiniz dişliler configurable idi - diş sayısını yeni bir bileşen eklemeye gerek kalmadan kolayca değiştirebilmeniz sağlandı. Modellerinizi daha parametrik yapmak için müsait olduğunda configurable parçaları kullanmaya çalışın.

<br>

