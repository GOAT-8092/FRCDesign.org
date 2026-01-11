# 1C: Pratik Mekanizmalar

## Egzersiz 4: Teleskopik Hook

Bu egzersizde, bir teleskopik tırmanıcı modelleyeceksiniz. Bu mekanizma [WCP GreyT teleskopik bearing blokları](https://wcproducts.com/products/greyt-telescope "GreyT Telescope Product Page"){:target="_blank"} ve [REV MAXPlanetary](https://www.revrobotics.com/frc/maxplanetary-system/ "Rev MAXPlanetary System Product Page"){:target="_blank"} montaj şanzıman plakaları içerir. Modelleme yaparken hook ve şanzıman sketch'lerine dikkat etmeniz önerilir.

!!! warning
    Bu noktadan itibaren shaft'ların belirli uzunlukları ve belt'lerin offset'leri sağlanmayabilir, mesafeleri ayarlarken shaft'lara gidecek bileşenleri düşünmelisiniz. Gerekirse daha sonra bu uzunlukları değiştirmek tamamdır. Kendi mekanizmalarınızı yaptığınızda bunun için adım adım bir rehber olmayacak! Bu egzersizler, build season'a hazırlanmak için ilerledikçe size guard rails'i gradually geri çekmeye çalışır. Takılırsanız solution doc'a bakmaktan veya mentordan yardım istemekten çekinmeyin!

### COTS Bileşenlerinden Yararlanmak
Zaman kısıtlı bir build season'da COTS bileşenleri kullanmak çok önemlidir.
Her parçayı üretebilecek yeteneğe sahip olsanız bile, COTS parçalarına güvenmek, zamanınızı daha önemli görevlere harcamanızı sağlar - tasarımları rafine etmek veya test etmek gibi.
Bu, zamanınızı en çok etkilediği yerde harcamanızı sağlar, zaten hazır bulunan parçaları yeniden icat etmek yerine.

???+ Örnek "Egzersiz 4 COTS Bileşenleri"
    <div class="grid cards" markdown>

    -   <center><img src="../images/telescope/greyt.webp" width="100%"></center>

    -   <center><img src="../images/telescope/maxplanetary.webp" width="100%"></center>

    </div>

    <figure>
      <figcaption>Teleskopik bearing blokları, çoğu takım için üretimi zor ve zaman alacak karmaşık geometriye sahiptir.
                  REV MAXPlanetary, özel bir şanzımana ihtiyaç duymadan büyük bir şanzıman redüksiyonu elde etmenin kolay bir yoludur. (Fotoğraf Kaynakları: WCP, REV)</figcaption>
    </figure>

### Crush Blokları

3D-baskı crush blokları, bolt'ların plaka olmadan geçtiği assembly'lerde ince cidarlı tüpleri güçlendirmek için kullanılabilir.
Cıvataların gücü sıkma kuvvetlerinden gelir, ince duvarları destekleyecek hiçbir şey yoksa, tüp proper sıkma kuvvetini elde etmeden önce çökebilir.
Crush blokları yükü dağıtır, tam sıkma kuvvetine izin verirken tüpün yapısal bütünlüğünü korur.

Alternatif olarak, bir "crush plaka" da fastener kuvvetini dağıtmak ve crush blokla benzer bir etki elde etmek için kullanılabilir.

???+ örnek "Crush Blokları ve Crush Plakalar"
    <figure>
    <img src="../images/telescope/crush-block-plate.webp" width="65%">
    <figcaption>Bir 3D baskı crush bloğu (sol) ve crush plakası (sağ). Crush plakaları, crush bloğu takmanın zor olabileceği tüplerin ortası için iyi çalışır.</figcaption>
    </figure>

### Part Studio Talimatları

Kopyalanmış belgenizdeki **"Exercise #4 Part Studio" sekmesine gidin** ve bu egzersiz için part studio'yu tamamlamak için **slaytlardaki talimatları izleyin**.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-0.webp" style="width:100%">
      <figcaption>0. Final Part Studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-1.webp" style="width:100%">
      <figcaption>1. Right plane üzerinde telescope tüplerinin yan profil sketch'ini oluşturarak başlayın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-2.webp" style="width:100%">
      <figcaption>2. Tüpler için solid bodies oluşturmak için iki extrude kullanın. Sonra, Tube Converter Featurescript'i (veya shell özelliğini) kullanarak solid bodies'i delik patternsiz iki ince cidarlı tüpe dönüştürün.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-3.webp" style="width:100%">
      <figcaption>3. WCP bearing blokları için iç ve dış tüplere delikleri ekleyin. Boyutlar <a href="https://docs.wcproducts.com/greyt-telescope/overview-and-features/tubing-hole-pattern">WCP'nin belgelerinden</a> alınmıştır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-4.webp" style="width:100%">
      <figcaption>4. İç tüpün üstündeki crush bloğu modelleyin. Tüpün içindeki crush blok için 3D-baskı toleranslarını hesaba katmak için biraz clearance bıraktığınızdan emin olun. Hook'u modelledikten sonra crush bloktan geçen delikleri ekleyeceksiniz.</figcaption>
    </figure>
  </div>


  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-5.webp" style="width:100%">
      <figcaption>5. Hook'u sketchleyin. Solution belgesindeki sketch ilişkilerine dikkat edin.</figcaption>
    </figure>
  </div>


  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-6.webp" style="width:100%">
      <figcaption>6. Hook'u extrude edin, ardından montaj deliklerini tüp ve crush bloğu içinden geçecek şekilde extrude edin. Ayrıca hook spacer'ını ekleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/Kt2l8vujAUE?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>7. Hook 3d baskı spacer'ını modelleyin. Sketch imprinting etkinleştirildiğinde, 3d baskı bloğun başladığı yer için çizgiyi çizmemiz yeterlidir. Hook profilini sketch'e kopyalamak için <code>Use</code> özelliğini kullanmanıza gerek yoktur.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-8.webp" style="width:100%">
      <figcaption>8. Tüpün dışında şanzıman montaj plakasını sketchleyin. Şanzımanın düzgün bir şekilde assembly edilebilmesi için 3/8" clamping spacer'ları ve tüp arasında küçük bir 0.01" boşluk olmalıdır. 13.75 mm construction daire yuvarlatılmış hex spool'u temsil eder. Plakanın sol tarafındaki noktaya bir delik yerleştirilecektir.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-9.webp" style="width:100%">
      <figcaption>9. Yuvarlatılmış hex spool'a teğet bir çizgi oluşturarak pull down string'i sketchleyin. Bu çizgiyi ipin sweep'ini oluşturmak için kullanacağımızı, bu nedenle bu çizginin construction geometri olmaması gerektiğini unutmayın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-10.webp" style="width:100%">
      <figcaption>10. Plakayı extrude edin. Tüpe sıkılan yüzey kuvveti yayması için bu plaka pocket edilmeyecektir. İsteğe bağlı olarak, kısmen pocket edebilir ve tüpe sıkılan plakanın tarafında 1/16" malzeme bırakabilirsiniz.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-11.webp" style="width:100%">
      <figcaption>11. Şanzıman plakasına threaded olan bolt için bir 10-32 delik ekleyin, ardından plakayı diğer tarafa yansıtın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-12.webp" style="width:100%">
      <figcaption>12. Şanzıman spacer'ını ve shaft'ı modelleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-13.webp" style="width:100%">
      <figcaption>13. Sketch edilmiş ip çizgisinin ucundaki mate connector'ü kullanarak shaft'ın merkeziyle hizalanmış 3mm bir daire sketch'i oluşturun.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-14.webp" style="width:100%">
      <figcaption>14. Şanzımandan gelen dikey çizgi boyunca daireyi sweep ederek ipin modelini oluşturun.</figcaption>
    </figure>
  </div>


  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/parts-0.webp" style="width:100%">
      <figcaption>15. Özellikleri adlandırarak ve klasörlere koyarak part studio'yu tamamlayın. Ayrıca reference design'a göre malzemeleri atayın. </figcaption>
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

**Sonra, kopyalanmış belgenizdeki **"Exercise #4 Assembly" sekmesine gidin** ve bu egzersizi tamamlamak için **slaytlardaki talimatları izleyin**.

<div class="slideshow-container">
  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/telescope/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/ch1kZ_IOCjs?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>1. Climber bileşenlerini insert edin ve sadece base stage bileşenlerini Origin Cube ile bir araya gruplandırın. Bunun nedeni, inner stage'in base stage'e göre hareket etmesidir, bu yüzden onları bir araya gruplayamayız.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/assy-2.webp" style="width:100%">
      <figcaption>2. Inner stage bileşenlerini bir araya fasten edin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/Vt1ld7z8ovI?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>3. <a href="https://cad.onshape.com/documents/3f21b4b70302525a1e1f2c29/v/4ec8cc58f734f29f41a0fdb8/e/4646e6fc60ff8c4fe2a9d4dd" target="_blank">WCP GreyT telescope belgesinden</a> WCP GreyT telescope bearing bloklarını insert edin ve fasten edin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/i4Kcsdnsk8A?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>4. Inner stage'i constrain etmek için iki <code>Slider</code> mate kullanın. İki slider mate kullanarak (biri alt için, biri üst için), inner stage motion constraint base stage'teki uzunluk değişikliklerine parametrikdir. Açıkça bir seyahat uzunluğu belirtmek zorunda değiliz. </figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/assy-5.webp" style="width:100%">
      <figcaption>5. Spacer'ı fasten edin ve replicate edin. Shaft bearing'i plakaya ve shaft'a insert edin ve fasten edin. MAXPlanetary şanzımanının çıkışında başka bir bearing olduğu için plakada sadece bir bearing gerektirdiğimizi unutmayın, shaft'ı overconstrain etmek istemiyoruz.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/assy-6.webp" style="width:100%">
      <figcaption>6. FRCDesignLib'den MAXPlanetary şanzımanını ve NEO Vortex'i insert edin ve fasten edin. 25:1 dişli oranı ile 90 derece çıkış kullanacağız.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/assy-7.webp" style="width:100%">
      <figcaption>7. Gerekli tüm fastener'ları insert edin, fasten edin ve replicate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/assy-8.webp" style="width:100%">
      <figcaption>8. Şanzımanı yerine sabitlemek için kullanılan bolt'un yakın görünümü. Bu bolt şanzımanın yukarı aşağı kaymasını önler.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/telescope/assy-0.webp" style="width:100%">
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
    Siz ve/veya ekibinizden daha deneyimli bir üye/mentor [**CAD'inizi gözden geçirsin!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"} Assembly'nizin 27 instance'ı olmalıdır.

### Kesit Görünümleri

Kesit görünümleri, belirli bir düzlem boyunca keserek bir parçanın veya assembly'nin iç özelliklerini ortaya çıkarmanıza yardımcı olan kullanışlı bir araçtır. Kesit düzlemi olarak bir düzlem, düzlemsel yüz, silindir, koni veya mate connector seçebilirsiniz. Ayrıca kesit görünümüne belirli parçaları dahil etmeyi veya hariç tutmayı seçebilirsiniz.

!!! Tip "Kesit Görünümü Oluşturma"
    <figure>
      <iframe src="https://www.youtube.com/embed/6oiVBMGkCOs?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>Pinning bolt'un daha iyi bir görünümünü almak için kesit görünümü oluşturma.</figcaption>
    </figure>

<br>
