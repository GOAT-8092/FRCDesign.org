


# 1B: Güç Aktarımları

## Egzersiz 3: Kayış ve Dişli Aktarma

Bu egzersizde, dişliler ve kayış kullanan iki kademeli bir şanzıman modelleyeceksiniz. Bu şanzıman, daha önce Stage 1A'da öğrendiğiniz gibi çerçeve ve gusset gibi elemanları da içerir. Bu egzersizin amacı, modelleme becerilerinizi artırmaya devam etmektir.

!!! Uyarı "Hatırlatma!"
    Sketch'lerinizi her zaman tam olarak **tanımlayın**, özelliklerinizi **yeniden adlandırın** ve feature ve instance ağaçlarınızı **klasörlerle** düzenli tutun.

### Part Studio Talimatları

Kopyaladığınız belgede **"Exercise #3 Part Studio" sekmesine gidin** ve bu egzersiz için part studioyu tamamlamak üzere **slaytlardaki talimatları izleyin**.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-0.webp" style="width:100%">
      <figcaption>0. Final part studio.</figcaption>
    </figure>
    </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-1.webp" style="width:100%">
      <figcaption>1. Origin Cube özelliğini kullanarak başlayın (böylece kayış fonksiyonları daha sonra kullanılabilir). Ardından çerçeve için tube profillerini çizin. Egimli tube ve dikey tube arasında montaj toleransları için 1/8" boşluk vardır. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-2.webp" style="width:100%">
      <figcaption>2. Tube profillerini extrude etmek için <code>Extrude Individual</code> Featurescript'ini kullanın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-3.webp" style="width:100%">
      <figcaption>3. Dikdörtgenleri delik desenli 1x1 ince duvarlı tube'a (1/16" kalınlığında duvar) dönüştürmek için <code>Tube Converter</code> Featurescript'ini kullanın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-4.webp" style="width:100%">
      <figcaption>4. Basit bir L gusset sketch'i çizin</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-5.webp" style="width:100%">
      <figcaption>5. Gusset'i extrude edin</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-6.webp" style="width:100%">
      <figcaption>6. Alt tube'nın dış yüzünde şanzıman layout sketch'ini oluşturun. 60T ve 20T dişlileri olan iki dişliyi çizerek başlayın. 60T dişli output'tur ve onu 2" ve 4.5" boyutlarıyla verilen belirli bir konuma kısıtlamak istiyoruz.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-7.webp" style="width:100%">
      <figcaption>7. Ardından, başlangıçta eklediğiniz Origin Cube featurescript'indeki #PulleyPD_5mm() fonksiyonunu kullanarak pitch çaplarını hesaplamak için 5mm pitch 12T ve 36T kasnakları çizin. Ayrıca 36T kasnağı dikey tube'dan 0.25" olacak şekilde boşluklandırın. Bu adım dişlilerin konumunu tamamen kısıtlar.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-8.webp" style="width:100%">
      <figcaption>8. 60T HTD5 kayışı için #BeltCTC_5mm() fonksiyonunu kullanarak layout sketch'e kayış c-c'yi ekleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-9.webp" style="width:100%">
      <figcaption>9. İsteğe bağlı olarak iki kasnak daireyi bağlamak için iki teğet çizgi çizin. Bu kayışı temsil eder.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-10.webp" style="width:100%">
      <figcaption>10. Son olarak, motor için 2.5" bir daire sketch'in. Motoru egimli tube'dan 1/8" uzakta olacak şekilde boşluklandırın. Layout sketch artık tamamen tanımlanmış.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-11.webp" style="width:100%">
      <figcaption>11. Alt tube'nın dış yüzünde plaka sketch'ini oluşturun. İki 1.125" çapında rulman deliği çizerek başlayın. Motorun üzerindeki 12T kasnağın deliğe sığabilmesi için gerçek hayatta montaja yardımcı olmak için motor boss'u için 1.5" bir delik ekleyin. Bu, şanzıman montajını oluşturduğunuzda daha net olacaktır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-12.webp" style="width:100%">
      <figcaption>12. Motor için dairesel pattern ile 2" bolt daire ekleyin. Sol üstteki deliğin merkezini kasnaklar arasındaki merkez çizgisi ile çakışık olacak şekilde kısıtlayın (coincident, çizginin sonsuz uzantısını kullanır) </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-13.webp" style="width:100%">
      <figcaption>13. Plaka için tube montaj deliklerini ekleyin. Deliklerin tube'nın kenarlarını referans aldığına ve tube üzerindeki delikleri almadığına dikkat edin. Bu, modeli daha parametrik yapmak içindir, çünkü tube'daki değişiklikler deli konumlarını değiştirebilir ve şanzıman plaka sketch'ini bozabilir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-14.webp" style="width:100%">
      <figcaption>14. Centerpoint arcs ve teğet çizgiler kullanarak plaka outline'ını çizin. Plakanın altını 60T dişlinin pitch çemberinin kenarından 0.25" olacak şekilde boşluklandırın. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-15.webp" style="width:100%">
      <figcaption>15. Spacer'lar için iki delik ekleyin. Construction circle'lar 3/8" çapında spacer'ı temsil eder. Üst delik plakanın sol kenarı ile teğettir ve 2.5" motor daire ile teğettir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-16.webp" style="width:100%">
      <figcaption>16. Plakayı 1/4" kalınlığında extrude edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-17.webp" style="width:100%">
      <figcaption>17. Karşı tarafta, iç plaka için bir sketch oluşturun. Ortak geometriyi (delikler, outline) kopyalamak için <code>Use</code> sketch özelliğini kullanın. Motor deliklerini kopyalamayın, çünkü iç plakada motor gövdesi için bir kesik olacaktır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-18.webp" style="width:100%">
      <figcaption>18. Motor kesimi için bir arc ekleyerek plaka outline'ını tamamlayın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-19.webp" style="width:100%">
      <figcaption>19. İç plakayı 1/4" kalınlığında extrude edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-20.webp" style="width:100%">
      <figcaption>20. Motor kesimi için iki kenarda 3/16" yarıçapında fillet ekleyin. Yarıçap, 3/8" çapındaki spacer ile eşleşecek şekilde seçilir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-21.webp" style="width:100%">
      <figcaption>21. 3/8" çapında spacer'ı modelleyin. Spacer uzunluğunu parametrik tutmak için <code>Up to Face</code> son koşulunu kullanabilirsiniz.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
       <iframe src="https://www.youtube.com/embed/UBT5AGqBYW4?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>22. Kayış modelini oluşturmak için <code>Belt & Chain Gen</code> Featurescript'ini kullanın. Kayışın pitch'i 5mm ve genişliği 9mm'dir. Kayışın plaka ile çarpışmaması için referans düzlemini 0.5" olarak ofset edin. Kayışı basitleştirilmiş tutun, çünkü diş modellemeyi açmak part studioyu yavaşlatır. <code>Belt & Chain Gen</code> Featurescript'inin aynı zamanda kayışın pitch uzunluğunu hesapladığını ve bu sayede adım 7 ve 8'de doğru C-C hesaplayıp hesaplamadığımızı doğrulayabildiğimizi unutmayın. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-23.webp" style="width:100%">
      <figcaption>23. 1. kademe şaftını oluşturmak için <code>Robot Shaft</code> Featurescript'ini kullanın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-24.webp" style="width:100%">
      <figcaption>24. Output şaftını oluşturmak için <code>Robot Shaft</code> Featurescript'ini kullanın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-25.webp" style="width:100%">
      <figcaption>25. İsteğe bağlı olarak plakaları pocket edin. Başlamak için motor plakasının dış yüzünde bir sketch oluşturun ve struts oluşturmak için çizgiler çizin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-26.webp" style="width:100%">
      <figcaption>26. Önceki sketch'i seçerek pocket eklemek için <code>Part Lighten</code> Featurescript'ini kullanın. 0.15" genişliğinde kaburgalar ve 0.26" takım çapı kullanın. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-27.webp" style="width:100%">
      <figcaption>27. İç plakada bir sketch oluşturun ve strut çizgilerini çizin. Motor plakası pocket sketch'inden strut çizgilerini kopyalamak için <code>Use</code> sketch özelliğini kullanabilirsiniz.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-28.webp" style="width:100%">
      <figcaption>28. Önceki sketch'i seçerek pocket eklemek için <code>Part Lighten</code> Featurescript'ini kullanın. Yine, 0.15" genişliğinde kaburgalar ve 0.26" takım çapı kullanın. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/parts-0.webp" style="width:100%">
      <figcaption>29. Tamamlanmış part studio. Önemli sketch'leri ve parçaları adlandırın. Plakanın ve spacer'ların malzemesini 6061 Aluminum olarak ayarlayın. Tube, gusset ve şaftların malzemesi otomatik olarak ayarlanmış olmalıdır. </figcaption>
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

Artık part studioyu tamamladığınıza göre, bu egzersizi tamamlamak için kopyaladığınız belgede **"Exercise #3 Assembly" sekmesine gidin** ve **slaytlardaki talimatları izleyin**.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/DdvX_09Hd20?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption>1. Part studioyu montaja ekleyin ve sadece alt tube'ı sabitleyin. Tube'lar, plakalar ve gusset için group mate kullanın. Gusset'i kopyalayın ve tube'nın diğer tarafına mate edin. Ardından, spacer'ı plakaya mate edin ve <code>Replicate</code> aracını kullanarak spacer'ı replike edin. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/Rait0iVbiD0?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption>2. FRCDesignLib parçalarını kullanarak rulmanları ve şaftları monte edin. Rulmanı replike etmek için <code>Replicate</code> aracını kullanın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/3rhXrBgWlng?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption>3. FRCDesignLib parçalarını kullanarak 36T kasnağı, kayışı, motoru ve motor pinion kasnağını monte edin. Motor pinion'un şaftın altından 1/16" ofsetli olduğuna, böylece kayışla daha iyi hizalandığına dikkat edin. Ayrıca, kayışın sadece tek bir fasten mate gerektirdiğine, çünkü yönünün part studio'da nasıl modellendiğine göre belirlendiğine dikkat edin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
       <iframe src="https://www.youtube.com/embed/j-Tofk8_Nfs?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption>4. FRCDesignLib parçalarını kullanarak şaft spacer'larını ve dişlileri monte edin. Bu kez 60T dişli için pocket edilmiş bir dişli kullandığımıza dikkat edin. Pocket edilmiş dişliler, normal dişlilerle aynıdır, sadece ağırlığı tasarruf etmek için bazı malzemeler çıkarılmıştır. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/0yfIqvglCHw?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption>5. FRCDesignLib parçalarını kullanarak şaft tutma boltlarını monte edin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
       <iframe src="https://www.youtube.com/embed/h7ABxpXyMbY?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption>6. FRCDesignLib parçalarını kullanarak motor boltlarını, şanzıman boltlarını ve somunları monte edin</figcaption>
    </div>
  </div>
  <div class="mySlides fade">
    <div class="slide-content">
       <iframe src="https://www.youtube.com/embed/fd56NxBZHd8?rel=0&controls=1&showinfo=0" frameborder="0" allowfullscreen></iframe>
      <figcaption>7. FRCDesignLib parçalarını kullanarak gusset perçitlerini monte edin.</figcaption>
    </div>
  </div>
  <div class="mySlides fade">
    <figure>
      <img src="../images/exercises/exercise3/assy-0.webp" style="width:100%">
      <figcaption>8. Tamamlanmış montaj. Parçaları klasörlere sıraladığınızdan ve replicate özelliklerinizi adlandırdığınızdan emin olun. </figcaption>
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
    Sizin ve/veya takımınızın daha deneyimli bir üyesinin/mentorünün [**CAD'inizi incelemesini sağlayın!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"} Montajınızın 31 instance'ı olmalıdır.

Bu egzersizte, bazı çerçeve elemanlarıyla entegre edilmiş oldukça karmaşık bir şanzıman modellediniz. Bu noktada, sketch ve extrude araçlarına rahat olmaya başlamalısınız. Ayrıca, farklı ayarlarla oynayarak şu ana kadar kullandığınız Featurescript'lerdeki tüm seçeneklere aşina olmalısınız.



### Parametrik Modelleme

Modelinizin ne kadar parametrik olduğunu hissetmek için, layout sketch'teki belirli ana boyutları, örneğin tube'nın uzunluğunu, tube'nın açısını, kayışın uzunluğunu ve dişlilerin boyutunu değiştirmeyi deneyebilirsiniz. Hangi modifikasyonların sorunsuz güncelleneceğini ve hangilerinin CAD'de ek düzeltmeler gerektirdiğini oynayarak görün.

Bu tasarımlarda delik boyutlarının, malzemelerin vb. nasıl seçildiği konusunda merak edebilirsiniz. [Design Handbook](/design-handbook/ "Design Handbook Page"){:target="_blank"} sayfalarını inceleyerek veya takımınızla ve/veya DDS Discord'undaki diğer öğrencilerle ve mentorlarla tartışarak daha fazla bilgi edinmeniz teşvik edilir.

<br>

