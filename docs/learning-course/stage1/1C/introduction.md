# 1C: Pratik Mekanizmalar
## Giriş

Stage 1C'ye hoş geldiniz! Bu aşamada, CAD becerilerinizi pratik yapmak ve küçük detayları uygulama sayısız farklı mekanizma modelleyeceksiniz. Yol boyunca iş akışınıza yardımcı olmak için yeni COTS parçaları ve Onshape ipuçları ve püf noktaları tanıtılacaktır.

Bu mekanizmalar özellikle beceri pratiği yapmak ve kavramları tanıtmak için tasarlandığından, tam bir robot bağlamı dışında modellenmişlerdir.
Bu mekanizmalar bazı iyi tasarım tekniklerini içerse de, mutlaka tam sistemler değildir. Modeller kesinlikle CAD pratiği içindir ve gerçek robotlarda kullanılması önerilmez.

### Layout Sketches

Her mekanizma için Stage 1B egzersizlerinde tanıtılanlara benzer bir layout sketch kullanmaktan emin olun. Layout sketch'ler her ölçekte yardımcıdır, ana boyutları tek bir sketch'te tanımlamanızı sağlar, bu da gerekli olduğunda kolayca ayarlamayı sağlar.

!!! İpucu
    Tasarımı yönlendiren bileşenleri layout sketch'e ekleyin (örn. güç aktarımı, oyun parçası yolu, silindirler vb.), belirli parça detaylarını kendi sketch'lerinde ve özelliklerinde tutarken (örn. rulman delikleri ve plaka outline'ı için ayrı bir sketch, extrude edilecek).

<div class="slideshow-container">
  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
      <figure>
          <img src="../images/exercise1-layout.webp" style="width:80%">
      <figcaptions>Egzersiz 1 layout sketch. Layout sketch'te sadece önemli geometri detaylarının olduğuna dikkat edin.</figcaption>
      </figure>
  </div>

  <div class="mySlides fade">
      <figure>
          <img src="../images/exercise1-layout-final.webp" style="width:80%">
          <figcaptions>Egzersiz 1 yan görünüm. Layout sketch'in mekanizmanın geometrisini nasıl yönlendirdiğine dikkat edin.</figcaption>
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

!!! Not
    Layout sketch kavramı daha sonra robot bağlamında kullanmaya başladığınızda genişletilecektir.

### Tutarlı Originleri Koruma

Stage 1'in önceki bölümlerinde belirtildiği gibi, part studio ve montaj arasında tutarlı bir origin korumalısınız. Bunu başarmak için [`Origin Cube` Featurescript`](https://cad.onshape.com/documents/321c197a842fc5f1a29e6621/w/fc3cdd5ca7edcd93e02f13cc/e/2b321cb91b74224b9c14b433 "Origin Cube Featurescript Onshape Document"){:target="_blank"}'i kullanacaksınız. **Origin cube'un her part studio'da ilk özellik olduğundan emin olun.** Aşağıdaki slaytlar origin cube'un nasıl kullanılacağına dair bir demosyon sağlar.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/origin-cube-tutorial/origin-cube-tutorial-1.webp" style="width:90%">
      <figcaption>Origin Cube Featurescript'i part studio'daki ilk özellik olarak yerleştirin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/origin-cube-tutorial/origin-cube-tutorial-2.webp" style="width:90%">
      <figcaption>Mekanizmanızı modelleyin.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/H6y1S_cHLKk?rel=0&controls=1&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>Part studioyu yeşil tik işareti ile montaja ekleyin. Tüm statik parçaları Origin Cube parçası ile birlikte gruplandırın, ardından Origin Cube üzerindeki mate connector'ı montajın origin'ine fasten edin.</figcaption>
    </div>
  </div>

  <!-- Next and previous buttons -->
  <button class="prev" onclick="plusSlides(-1,1)" style="background-color: #000; color: #fff;">&#10094;</button>
  <button class="next" onclick="plusSlides(1,1)" style="background-color: #000; color: #fff;">&#10095;</button>
  <!-- The dots/circles -->
  <div class="dotsContainer" style="text-align:center">
    <!-- Dots will be generated here -->
  </div>
</div>

Bu adımları izlemek, montajın origin'ini asla değişmeyecek veya kaybolmayacak bir parçaya bağlamanızı sağlar. Origin cube'a göre diğer parçaların konumu, part studio ile tutarlı olacaktır, part studio'da şeyler değiştirilse bile. Bu, 2. aşama ve ötesinde kol veya asansör gibi esnek montajlar için özellikle yararlı olacaktır.

<br>

<!-- The following is just notes that can be used in the final content of the page.

Hatırlayın, pratik esastır – oluşturduğunuz CAD modelleri ne kadar çok olursa, o kadar usta ve verimli olursunuz. Klavye kısayolları kullanmak CAD iş akışınızı önemli ölçüde hızlandırabilir. Kötü alışkanlıklar geliştirmekten kaçınmak için en iyi pratiklere dikkat edin.


Bu geri bildirim formunu değiştirin ve her bölümün sonuna bir tane ekleyin? Veya bunu yapın ve bunu tutun ve soruları biraz düzenleyin ve burada kullanışlı içerik olduğu için bunu tutun ve 2. aşamanın sonuna bir tane ekleyin, çünkü burada tamamlanması gereken sürenin aldığı zaman gibi faydalı bilgiler var ve bunu daha küçük geri bildirim formlarından alamayabiliriz. Bilmiyorum, bunu çözeceğim

İsteğe bağlı olarak, aşama 0 ve 1 hakkında [bu geri bildirim formunu](https://forms.gle/J1QNvRkvpi7xyfuU8 "Learning Course Feedback Form"){:target="_blank"} doldurun. -->
