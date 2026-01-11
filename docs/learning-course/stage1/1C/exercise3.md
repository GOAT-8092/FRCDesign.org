# 1C: Pratik Mekanizmalar

## Egzersiz 3: Ball Shooter

Egzersiz 3'ten başlayarak, talimat slaytları sadece parça parça talimatlar ve önemli detaylar sağlayacaktır.
Kesin özellik detayları için, egzersiz çözümleri belgesine başvurmalısınız.
Bu, egzersizler giderek daha az rehberlik edilen gelecek egzersizler için sizi hazırlamak içindir.

Bu egzersizde, çok basit 2.5" ball shooter modelleyeceksiniz.
Bu mekanizma 3D-baskı kasnaklar, 3D-baskı ramp ve nut şeritleri içerir. Modelleme yaparken layout sketch'lere dikkat etmeniz önerilir.

### 3D-baskı Kasnaklar
Şimdiye kadar, assembly'lerinizde sadece COTS kasnak kullandınız.
Ancak, 3D-baskı kasnaklar harika bir alternatiftir çünkü daha ucuzdurlar, kolayca bulunabilirler (3D yazıcınız olduğu varsayımıyla) ve yüksek derecede özelleştirilebilirler.

3D-baskı kasnaklar, FRCDesignLib ve Robot Pulley Featurescript'te bulunanlar gibi kasnak üreticileri kullanılarak kolayca oluşturulabilir.
Ancak, shaft arayüzüne yakın dikkat edilmelidir. 3D-baskı hex profilleri kolayca sıyırabilir, bu nedenle torku daha iyi transfer etmek için metal bir insert (WCP veya Thrifty Bot gibi satıcılardan) kullanılmalıdır.
Aşağıda farklı tipte insert'li 3D-baskı kasnak örneklerine bakın.

???+ örnek "3D-baskı Kasnak Insertleri"
    <figure>
      <img src="../images/shooter/3dp-pulleys.webp" style="width:80%">
      <figcaption>Hex shaft için hex insert'li (sol), Kraken motorları için SplineXS insert'li (orta) ve NEO/CIM motorları için pinion gear insert'li (sağ) 3D-baskı kasnaklar. </figcaption>
    </figure>

!!! Warning
    3D-baskı kasnak delikleri kolayca aşınır, bu yüzden her zaman metal bir insert veya pinion gear insert kullanmalısınız.
    COTS insert'ler satın almanın ucuz bir alternatifi, onları [Fabworks](https://www.fabworks.com "Fabworks Sheet Metal Cutting"){:target="_blank"} gibi bir laser kesme hizmetinden sipariş etmektir. Büyük miktarlarda (~20 parça), her biri sadece yaklaşık 1$ tutar.

### Nut Şeritleri
Nut şeritleri, genellikle dik plakaları veya plakayı tüpe bağlamak için kullanılan çok yönlü yapısal bir bileşendir.
WCP, REV ve Last Anvil gibi satıcılar #10-32 veya #8-32 tapped delikli 6" uzunluğunda segmentlerde nut şeritleri sunar.
Bu nut şeritleri çok sağlamdır ve kolayca herhangi bir uzunluğa kesilebilir.
Tamamladığınız egzersizde, nut şeritleri shooter'ı herhangi bir yüzeye kolayca monte etmenizi sağlar.

???+ örnek "Nut Şeritleri"
    <figure>
      <img src="../images/shooter/nut-strips-real.webp" style="width:65%">
      <figcaption>Nut şeritleri bir plakayı tüpe veya bir plakayı dik bir plakaya bağlamak için kullanılabilir. (Fotoğraf Kaynakları: FRC 4414)</figcaption>
    </figure>

### Blok Motorlar
Mekanizmalar oluştururken, bazen özel parçalar oluştururken belirli COTS bileşenlerine başvurmanız gerekir. Çoğu zaman sketch'lerde construction geometri işe yarasa da (motor outlines gibi), bazen daha karmaşık referanslara ihtiyaç duyarsınız. Part studio'ya tam bir detay bileşeni derive etmek (yüklenme sürelerini önemli ölçüde yavaşlatabilir) yerine, bu egzersizde kullanılan FRCDesignLib'den "block motor" gibi "block" geometrisi oluşturabilir veya derive edebilirsiniz.

<figure>
  <img src="../images/shooter/block-motor-example.webp" style="width:90%; border:5px solid #ADADAD">
</figure>

FRCDesignLib'den bir block motor insert ederken, Onshape'in derived parçaları nasıl ele aldığı nedeniyle "Differentiation Variable" kullanmak önemlidir. Her block motora benzersiz bir değer atamak, part studio'nuzdaki bu hataları önler.

### Part Studio Talimatları

Kopyalanmış belgenizdeki **"Exercise #3 Part Studio" sekmesine gidin** ve bu egzersiz için part studio'yu tamamlamak için **slaytlardaki talimatları izleyin**.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-0.webp" style="width:100%">
      <figcaption>0. Final Part Studio.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-1.webp" style="width:100%">
      <figcaption>1. Right plane üzerinde layout sketch oluşturun. 4" shooter wheel, 2" feeder wheel ve ball path ile başlayın. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-2.webp" style="width:100%">
      <figcaption>2. Right plane üzerinde, belt'ler, pulley'ler ve motorlarla yeni bir sketch oluşturun. En alttaki construction çizgi shooter'ımızın altını tanımlar.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-3.webp" style="width:100%">
      <figcaption>3. Layout sketch plane'inden 1.375" offset bir mate connector'ü sketch plane olarak kullanarak, side plate'i sketchleyin. Shooter hood etrafında #10-32 clearance delikleri sketchlemek için circular pattern kullanın. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-4.webp" style="width:100%">
      <figcaption>4. Plakayı 1/4" olarak extrude edin, ardından Right plane boyunca yansıtın. Mirror kullanıyoruz çünkü opposite side plate motorlar için ekstra bir cutout haricinde aynıdır.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-5.webp" style="width:100%">
      <figcaption>5. Motor montajını mirrored plakadan kaldırmak için bir cutoff boundary sketchleyin. Imprinting'in etkinleştirildiğinden emin olun. Plaka outlineının kendisi extrude'da kullanılacağı için tüm bölgeyi sketchlemenize gerek yok.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-6.webp" style="width:100%">
      <figcaption>6. Mirror edilmiş parçadaki motor montaj bölgesini extrude ederek geometriyi parçadan kaldırın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-7.webp" style="width:100%">
      <figcaption>7. Plakaların arasına giden büyük 3D print'i modelleyin. Layout veya part geometrisini kullanarak ihtiyacınız olan dimension sayısını minimize etmeye çalışın. Genişliğin parametrik olduğunu sağlamak için "Up to face" extrude kullanın.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/rGf0Vt8ahOQ?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>8. 3D-baskı parça kenarlarının tümüne 3/16" yarıçaplı fillet eklemek için <code>Fillet All Edges</code> Featurescript'ini kullanın. Parçanın yüzeyini seçmek için şu anda seçili olmayan tüm bileşenleri şeffaf veya gizli hale getiren <code>Isolate</code> aracını kullanabilirsiniz.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/DUJ8MbPS4Zg?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>9. FRCDesignLib'den bir block motor insert edin. Block motor'u motor bore'una transform etmek için <code>Transform</code> özelliğini kullanın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-10.webp" style="width:100%">
      <figcaption>10. HTD 5mm pitch belt'leri ekleyin. Belt'in tam sayıda dişe sahip olduğunu sağlamak için pitch uzunluğunun 5 mm'nin katı olduğunu iki kez kontrol edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/wFNDLm2Tisc?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>11. <code>Robot Shaft</code> featurescript kullanarak shooter wheel ve feeder wheel shaft'ını modelleyin.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/L8HWApw3luM?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>12. Feeder wheel'ı fasten etmek için layout sketch üzerinde bir mate connector ekleyin. Mate connector'ün sahibini feeder shaft olarak ayarlayın. Bu mate connector iki plakanın merkez noktasını işaretler ve assembly'de yardımcı olur.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-13.webp" style="width:100%">
      <figcaption>13. Shooter wheel shaft'ına bir mate connector eklemek için önceki adımları tekrarlayın. Shooter wheel shaft'ını mate connector sahibi olarak seçtiğinizden emin olun.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/parts-0.webp" style="width:100%">
      <figcaption>14. Özellikleri adlandırarak ve klasörlere organize ederek part studio'yu tamamlayın. </figcaption>
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

**Sonra, kopyalanmış belgenizdeki **"Exercise #3 Assembly" sekmesine gidin** ve bu egzersizi tamamlamak için **slaytlardaki talimatları izleyin**.

<div class="slideshow-container">
  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/shooter/assy-0.webp" style="width:100%">
      <figcaption>0. Final assembly.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/assy-1.webp" style="width:100%">
      <figcaption>1. Tüm part studio bileşenlerini insert edin. Shaft'lar ve belt'ler haricindeki tüm bileşenleri gruplandırın. Origin Cube'u origin'e fasten edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/7Zplj3xG83s?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>2. FRCDesignLib uygulamasından 4.5" uzunluğunda nut şeritleri insert edin ve fasten edin. Hangi tarafın plakaya fasten edildiğine yakın dikkat edin - komşu taraflardaki nut strip delikleri staggered edilmiştir.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/assy-3.webp" style="width:100%">
      <figcaption>3. İki NEO motorunu insert edin ve fasten edin. Bearing'leri insert edin, fasten edin ve replicate edin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/RsCl6xD8tMs?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>4. Shooter pulley'ı 24T 1/2" Hex w/ TTB insert ile configure edin.
                  Pulley ve TTB insert'i kopyalayıp yapıştırarak motor pulley'i oluşturun.
                  3/16" bir spacer kullanarak shooter pulley'ını shooter bearing'e fasten edin.
                  Sonra, motor pulley'ını belt'e fasten edin.
                  Son olarak, 8mm NEO shaft'ını 1/2" hex adapter'a fasten etmek için <code>Isolate</code> aracını kullanın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/vEuopW1B9r4?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>5. Feeder pulley'ı TTB 1/2" hex insert ile 36T olarak configure edin.
                  Motor pulley'ını 12T 20DP gear insert ile 18T olarak configure edin.
                  1/16" bir spacer kullanarak feeder pulley'ını feeder bearing'e fasten edin.
                  Sonra, motor pulley'ını belt'e fasten edin.
                  Son olarak, 12T motor pinion'unu fasten etmek için <code>Isolate</code> aracını kullanın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/assy-6.webp" style="width:100%">
      <figcaption>6. Shaft'ları pulley'lere fasten edin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/GuyhDXkKwho?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>7. Shooter ve feeder wheel'larını shaft centering mate connector'lere insert edin ve fasten edin.
                  Sonra, bearing'ler ve wheel'ler arasındaki boşlukları ölçmek için <code>Measure</code> aracını kullanın.
                  Wheel'lerin kenarlarındaki boşlukları doldurmak için spacer'lar oluşturun.
                  Son olarak, spacer'ları ve shooter wheel'ını feeder wheel'ın mate connector'ü boyunca yansıtmak için <code>Assembly Mirror</code> aracını kullanın.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/assy-8.webp" style="width:100%">
      <figcaption>8. 4" SDS Flywheel'i shooter'ın diğer tarafına insert edin ve fasten edin. </figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/assy-9.webp" style="width:100%">
      <figcaption>9. Gerekli tüm fastener'ları ve kalan donanımı insert edin, fasten edin ve replicate edin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/shooter/assy-0.webp" style="width:100%">
      <figcaption>10. Parçaları klasörlere düzenleyerek ve replicalarınızı adlandırarak assembly'nizi tamamlayın. Ayrıca ball'ı görselleştirmek için insert edip konumlandırabilirsiniz. </figcaption>
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
    Siz ve/veya ekibinizden daha deneyimli bir üye/mentor [**CAD'inizi gözden geçirsin!**](../1A/focusing-on-improvement.md "Focusing on Improvement Page"){:target="_blank"} Assembly'nizin 54 instance'ı olmalıdır.

### Isolate, Hide ve Make Transparent

Isolate aracı seçilenler hariç tüm diğer parçaları gizler, belirli bileşenlere odaklanmanıza yardımcı olur.
Hide aracı seçilen parçaları görünümden kaldırır, Make transparent ise seçilen parçaları kaldırmadan onları görmenizi sağlar, gizli bileşenlere erişmek için kullanışlıdır.

Parçaları silmek veya hareket ettirmek yerine, göreviniz için ihtiyacınız olan parçalara erişmek için bu araçları kullanmalısınız. Parçaları gizlerseniz, bir sonraki kişi için un-hide etmeyi unutmayın!

!!! Tip "Isolate, Hide ve Make Transparent"
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/I1nFphxKVXc?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>Assembly'ye yardımcı olmak için parçaları isolate edin, gizleyin veya şeffaf hale getirin.</figcaption>
    </div>

!!! Tip "Klavye Kısayolları"
    Onshape'deki diğer大多数 araçlar ve kısıtlamalar gibi, hide/show'un da güzel bir klavye kısayol kombinasyonu var. İmlecinizi bir parçanın üzerine getirin veya seçin ve gizlemek için `y` tuşuna basın. Aynı alana gidin ve parçayı un-hide yapmak için `shift+y` tuşuna basın.


<br>
