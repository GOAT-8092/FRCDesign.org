# Onshape'e Yeni

## Performans Ayarı

İlk hesap kurulumunuzdan sonra, Onshape uyumluluğu sağlamak için bir tarayıcı kontrolü çalıştıracaktır. Tarayıcınıza bağlı olarak, performansı iyileştirmek için ek adımlar atılabilir.

!!! Tip
    Mevcut performansınızı [Onshape Uyumluluk Kontrol Sayfasında](https://cad.onshape.com/check "Compatibility Check") test edebilirsiniz.

!!! Note
    Tarayıcı kontrolü başarısız olursa, farklı bir tarayıcı denemek isteyebilirsiniz. Şu anda, Chrome, Edge, Opera ve Arc gibi chromium tarayıcıları Onshape için en iyi desteklenen tarayıcılardır, ancak Firefox genellikle sorun olmadan çalışır. Safari iyi desteklenmemektedir.

### Chrome Performansını İyileştirme
Chrome kullanıyorsanız, işleme hızlarını artırmak için aşağıdaki ayarları değiştirmeyi deneyebilirsiniz.

- Öncelikle, chrome ayarlarına gitmek için arama çubuğunuza `chrome://settings/` yazın. "Mevcut olduğunda grafik hızlandırmayı kullan"ın etkinleştirildiğinden emin olun. Etkinleştirmek için güncellediyseniz chrome'u yeniden başlatın.

  <center><img src="/img/learning-course/course-setup/performance-tuning/graphicsacceleration.webp" style="width:80%;border:5px solid #ADADAD; border-radius: 2%"></center>

- `chrome://flags/` adresine gidin ve "Override Software Rendering List"i etkinleştirin:

  <center><img src="/img/learning-course/course-setup/performance-tuning/override-rendering-list.png" style="width:80%;border:5px solid #ADADAD; border-radius: 2%"></center>

- Son olarak, ANGLE grafik arka ucunuzu ayarlamayı deneyin:

  <center><img src="/img/learning-course/course-setup/performance-tuning/ANGLE-backend.png" style="width:80%; border:5px solid #ADADAD; border-radius: 2%"></center>

Lütfen performansın bireysel bilgisayar kurulumunuza bağlı olacağını unutmayın. Aşağıdaki süreci öneriyoruz:

- Bir ANGLE grafik arka ucu seçin: `chrome://flags/#use-angle`
- Yeniden Başlat düğmesine tıklayın
- [Performansınızı kontrol edin](https://cad.onshape.com/check "Compatibility Check")

Her bir arka uç için bu adımları tekrarlayın ve en performanslı olanı kullanın. İşte aynı makineden alınan bazı örneklerin hepsi.

<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure markdown="span">
      <img src="/img/learning-course/course-setup/performance-tuning/performance-examples/default.png" style="width:80%; data-description="The default configuration">
      <figcaption>Varsayılan yapılandırma</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure markdown="span">
      <img src="/img/learning-course/course-setup/performance-tuning/performance-examples/opengl.png" style="width:80%; data-description="OpenGL performance">
      <figcaption>OpenGL</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure markdown="span">
      <img src="/img/learning-course/course-setup/performance-tuning/performance-examples/D3D9.png" style="width:80%; data-description="Direct3D9">
      <figcaption>Direct3D 9</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure markdown="span">
      <img src="/img/learning-course/course-setup/performance-tuning/performance-examples/D3D11.png" style="width:80%; data-description="Direct3D11">
      <figcaption>Direct3D 11</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <figure markdown="span">
      <img src="/img/learning-course/course-setup/performance-tuning/performance-examples/D3D11on12.png" style="width:80%; data-description="Direct3don12">
      <figcaption>Direct3D 11 on 12</figcaption>
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

Yukarıdaki örnekte, Direct3D 11 OpenGL'i hafifçe geçmiştir, ancak her zaman böyle olmayacaktır.

<br>
