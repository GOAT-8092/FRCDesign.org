# 1C: Pratik Mekanizmalar

## Egzersiz 1: Düz Intake

Bu egzersizde, bir tür düz oyun parçası manipülatörünü modelleyeceksiniz. Bu mekanizma; canlı dingil uyumlu tekerlekler, bir kayış redüksiyonu ve tüp tapaları içerir.

### Tüp Tapaları
Tüp tapaları, basit ve sağlam yapılar inşa etmek için harika bir yoldur.
[WCP](https://wcproducts.com/products/tube-plugs "WCP Tube Plug Product Page"){:target="_blank"}, [REV](https://www.revrobotics.com/MAXTube-Endcaps/ "REV Tube Plugs Product Page"){:target="_blank"}, [Andymark](https://www.andymark.com/products/tube-plugs "Andymark Tube Plug Product Page"){:target="_blank"} ve [Last Anvil](https://lastanvil.com/products/1-x-1-x-0-0625-end-cap "Last Anvil Tube Plug Product Page"){:target="_blank"} gibi birçok satıcı çeşitli tüp boyutlarında sunar.
Plakaları tüplerin açık yüzüne bağlamak veya gusset kullanmadan tüpleri birbirine bağlamak için kullanılabilirler.

???+ Örnek "Tüp Tapaları"

    <div class="grid cards" markdown>

    -   <center markdown><img src="../images/flat-intake/high-tide-tube-plugs.webp" width="100%"></center>

    -   <center markdown><img src="../images/flat-intake/miso-tube-plug.webp" width="100%"></center>

    </div>

    <figure>
      <figcaption>Tüp tapaları gusset gerektirmeyen tüp-tüp (sol) ve tüp-plaka (sağ) bağlantıları oluşturmak için kullanılabilir. (Fotoğraf Kaynakları: FRC 4414, FRC 9442)</figcaption>
    </figure>

### Cıvata ve Perçin Kullanımı
1C egzersizleri boyunca, güçlü bir sezgi geliştirmek için çeşitli yapılar ve malzemeler için cıvata ve perçin kullanım teknikleri öğreneceksiniz.

Cıvatalar güçlüdür ve insanlar genellikle gereğinden fazla cıvata ve perçin kullanır. Sadece cıvata kullanırken genellikle bir parçanın köşelerini sabitlemek için 3-4 cıvata kullanabilir ve sorun yaşamazsınız, ancak ağırlığı minimize etmek veya tüplerin içinden tam geçmemeleri nedeniyle perçin kullanmayı tercih edebilirsiniz. Bu durumlarda, **zamanla gevşemelerini önlemek için her bağlantıda en az bir cıvata/mutareka çifti bulunduğu sürece** perçinleri kolayca aralayabilirsiniz. Bu hem bu egzersizde hem de egzersiz 8'de yapılır.

<figure>
  <img src="../images/flat-intake/bolt-and-rivet.webp" style="width:90%; border:5px solid #ADADAD">
</figure>

### Part Studio Talimatları

Kopyalanmış belgenizdeki **"Exercise #1 Part Studio" sekmesine gidin** ve bu egzersiz için part studio'yu tamamlamak için **slaytlardaki talimatları izleyin**.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-0.webp" style="width:100%">
      <figcaption>0. Final Part Studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-1.webp" style="width:100%">
      <figcaption>1. Layout sketch'i Right plane üzerinde başlatın. Önce alt tüpün şeklini sketchleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-2.webp" style="width:100%">
      <figcaption>2. Tüpün üstüne bir dikdörtgen çizin intake'in zeminini temsil etsin</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-3.webp" style="width:100%">
      <figcaption>3. Tekerlekleri temsil eden bir daire ve motoru temsil eden bir daire oluşturun. Onları doğru şekilde konumlandırmak için origin cube belt ctc fonksiyonunu kullanın, bu 1B Egzersiz 3'teki layout sketch'e benzer</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-4.webp" style="width:100%">
      <figcaption>4. Her iki kasnak için pitch dairelerini çizin ve kayış yolunu temsil etmek için bunları bağlayan çizgiler ekleyin. Kasnak dairelerini tanımlamak için origin cube PulleyPD fonksiyonunu kullanın</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-5.webp" style="width:100%">
      <figcaption>5. 2x1 tüpü temsil eden bir dikdörtgen çizin. Bu, tekerleklerden yukarı boyutlandırılmalı ve alt tüpün kenarıyla hizalanmalıdır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-6.webp" style="width:100%">
      <figcaption>6. Origin'den offset bir mate connector kullanarak yeni bir sketch oluşturun. Bu sketch, gösterildiği gibi "Right" yönünde offset olmalıdır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-7.webp" style="width:100%">
      <figcaption>7. Layout sketch'ten tüpler için dikdörtgenleri "Use" aracını kullanarak aktarın. Extrude etmeniz gerekeceği için bunların construction çizgileri olmadığından emin olun.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-8.webp" style="width:100%">
      <figcaption>8. Alt tüpü origin'e doğru 1" extrude edin ve üzerine Tube Converter uygulayın</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-9.webp" style="width:100%">
      <figcaption>9. 1x1 tüpün Right tarafında bir sketch başlatın. Imprinting'i devre dışı bıraktığınızdan emin olun. Layout sketch'teki motor ve tekerlek dairelerinin merkezine daireler ekleyin. Ayrıca use aracı ile CTC çizgisini aktarın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-10.webp" style="width:100%">
      <figcaption>10. CTC çizgisi üzerine bir daire çizerek bolt circle pattern oluşturun, ardından motor merkez noktası etrafında kopyalamak için pattern aracını kullanın. Bu pattern 8 deliğe sahip olmalı ve standart 2" motor bolt circle ile eşleşmesi için 2" çapına sahip olmalıdır. Bu pattern'deki 8 delikten sadece 3'üne ihtiyacımız var, bu yüzden geri kalanını construction delikleri yapın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-11.webp" style="width:100%">
      <figcaption>11. Alt tüp boyunca 2" aralıklı montaj delikleri ekleyin. Üst tüpte merkezlenmiş 1" aralıklı iki delik daha ekleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-12.webp" style="width:100%">
      <figcaption>12. Deliklerin etrafında plaka outlinesını çizin. Tüm kenar deliklerinin etrafına yaylar çizin ve bunları teğet çizgilerle birleştirin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-13.webp" style="width:100%">
      <figcaption>13. Plakayı oluşturmak için extrude edin. Slayt 9'da imprinting'i düzgün şekilde devre dışı bıraktıysanız, bu plakayı extrude etmek için seçmeniz gereken tek bir yüz olmalı.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-14.webp" style="width:100%">
      <figcaption>14. Bu plakayı Right plane boyunca yansıtarak bir referans plakası oluşturun. Bu plakayı ana plakadan kolayca ayırt edilebilmesi için anormal bir renge boyayın. Bu referans plakayı "zREF Plate" olarak adlandırın. Bu, onu insert menüsünün altında görünmesini sağlayacak ve assembly'de yanlışlıkla kullanılmasını zorlaştıracaktır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-15.webp" style="width:100%">
      <figcaption>15. Üst tüp şeklini extrude edin. Tüpü parametrik olarak referans plakasına extrude etmek için "Up to Face" ayarını kullandığınızdan emin olun.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-16.webp" style="width:100%">
      <figcaption>16. Bu yeni tüp üzerinde Tube Converter kullanın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-17.webp" style="width:100%">
      <figcaption>17. 1x1 tüpün üstünde bir sketch yapın, yine imprinting'i devre dışı bıraktığınızdan emin olun. Plakayı gösterildiği gibi sketchleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-18.webp" style="width:100%">
      <figcaption>18. Motor ve tekerlek delikleri arasında bir belt oluşturmak için `Belt & Chain Gen` Featurescript'ini kullanın. Starting offset ve seçtiğiniz construction dairelere dikkat edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-19.webp" style="width:100%">
      <figcaption>19. Robot Shaft Featurescript kullanarak wheel shaft oluşturun. Başlangıç mate connector'u kayışın ortasına yerleştirilmeli ve referans plakasının sol yüzüne kadar uzanmalıdır. Shaft, bearing flange'yi hesaba katmak için uçtan 1/16" offset olmalıdır. Shaft ayrıca wheel pulley içinden geçmesi için 9/32" başlangıç offset'ine sahip olmalıdır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-20.webp" style="width:100%">
      <figcaption>20. Artık tüm parçalarımız bittiğine göre, side plate'i pocket edebiliriz. Plakanın Right tarafında bir sketch oluşturun ve rib çizgilerini çizin. Sol üst çizgi üst bolt deliklerinden uzaklıkla boyutlandırılır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-21.webp" style="width:100%">
      <figcaption>21. Plakayı pocket etmek için Part Lighten Featurescript'i kullanın. Plakanın yüzeyini ve gösterildiği gibi tüm rib çizgi sketch'ini seçin.</figcaption>
    </figure>
  </div>

  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/parts-0.webp" style="width:100%">
      <figcaption>22. Part studio özelliklerinizi uygun klasörlere organize ettiğinizden emin olun.</figcaption>
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

**Sonra, kopyalanmış belgenizdeki **"Exercise #1 Assembly" sekmesine gidin** ve bu egzersizi tamamlamak için **slaytlardaki talimatları izleyin**.

<div class="slideshow-container">
  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <div class="slide-content">
      <img src="../images/flat-intake/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/H6y1S_cHLKk?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>1. Part studio'yu insert edin ve referans plakasını silin. Tüm bu bileşenleri bir araya gruplandırın ve origin cube'u assembly origin'e fasten edin</figcaption>
    </div>
  </div>
  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/_CIzPllEGyU?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>2. Alt tüpü ve plakayı diğer tarafa kopyalamak için Assembly Mirror aracını kullanın. Origin cube'un kenarının ortasındaki bir mate connector'ü mirror plane olarak kullanabilirsiniz</figcaption>
    </div>
  </div>
  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/pz9FJVzkWjg?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>3. Üst tüpe uyacak 1/16" Sleeve ile 2x1 Tüp tapalarını insert edin. Bu tüp tapalarını üst tüpün uçlarına mate edin.</figcaption>
    </div>
  </div>
  <div class="mySlides fade">
      <div class="slide-content">
        <iframe src="https://www.youtube.com/embed/aNM9l2OV1fY?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>4. Motoru, pulley ve shaft spacer'ları insert edin. Motor shaft parçalarını bir araya assembly edin ve Right tarafındaki side plate'e mate edin.</figcaption>
      </div>
    </div>
  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/iQ3y-yqWeA4?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>5. Wheel shaft için iki hex bearing insert edin ve plakalara mate edin.</figcaption>
    </div>
  </div>
  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/RMAst7Xcz4Y?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>6. Bir 1" Hex Spacer ve 2" Compliant wheel insert edin. Birbirlerine mate edin, ardından right bearing'e mate edin. Wheel ve spacer'ı shaft boyunca kopyalamak için Linear Pattern kullanın. Tekerlekleri tam olarak constrain etmek için sonuna bir 1/2" Spacer koyun.</figcaption>
    </div>
  </div>
  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/xrIZ7Ph1DAo?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>7. Shaft end screw'ları insert edin ve wheel shaft'ın her bir tarafına birer tane mate edin.</figcaption>
    </div>
  </div>
  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/quIf3misSe4?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>8. Yapı parçalarını birbirine fasten etmek için nuts, bolts ve rivet'leri kullanın. Fastener'lar çoğunlukla simetrik olduğu için işlemi hızlandırmak için assembly mirror'dan yararlanabilirsiniz.</figcaption>
    </div>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/flat-intake/assy-0.webp" style="width:100%">
      <figcaption>9. Parçaları klasörlere düzenleyerek ve replicalarınızı adlandırarak assembly'nizi tamamlayın.</figcaption>
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
    Siz ve/veya ekibinizden daha deneyimli bir üye/mentor [**CAD'inizi gözden geçirsin!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"}

### Parametrik Modelleme

Bu egzersizi tamamlamak için attığımız bazı adımlar basitleştirilebilirdi.
Örneğin, shaft'ı part studio'da düzgün şekilde konumlandır/hizala *gereklilik* yoktu.
Üst tüp için "Up to face" extrude kullanmamız *gerekti* yok.

Ancak, başlangıçta modelleme süresini hafifçe artırsalar da, geri dönüp düzenlerken ***önemli* derecede** zaman kazandırabilecekleri için bu teknikleri pratik yapıyoruz.
CAD yinelemeli bir süreçtir - modelleriniz ve tasarımlarınız ilk seferde mükemmel olmayacaktır, bu nedenle modelinizi değiştirmeyi daha kolay hale getirmek ve değişikliklere (örneğin, bu intake'in genişliğini değiştirmek) daha dayanıklı hale getirmek uzun vadede size zaman ve çaba kazandıracaktır.
En iyi uygulamaları kullandıkça, bunlar ikinci doğa haline gelecektir.

!!! question "Modelinizi Ayarlama"
    Egzersiz 1'de nelerin parametrik olduğunu ve nelerin olmadığını hissetmek için biraz oynayın. Genişlik, uzunluk, tüp konumları veya dişli oranı gibi şeyleri değiştirmeyi deneyebilirsiniz. Hangi boyutlar kolayca değiştirilebilir ve hangileri zordur? Hangi boyut değişiklikleri rebuild veya assembly hatasına neden olur?

<br>
