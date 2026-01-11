# 1D: Tasarım Metodolojisi - Basit Swerve Şasisi

## Üst Düzey Robot Montajı

Artık bir şasiniz olduğuna göre, bir _üst düzey robot montajı_ oluşturabilirsiniz. Üst düzey robot montajı, montaj hiyerarşisinde en üst düzeydedir. Montajları bu şekilde düzenlemek, hem CAD montajı hem de gerçek hayattaki montaj açısından şeyleri düzenli tutar.

Şasinizle gidecek bir üst düzey robot montajı oluşturacaksınız. Ekleyeceğiniz mekanizma, [1678'in 2023 robotunun](https://www.thebluealliance.com/team/1678/2023 "1678 2023 Blue Alliance Page") skor mekanizmasıdır. Skor mekanizması CAD'ine buradan erişilebilir:

<center markdown>[1678 2023 Skor Mekanizması Belgesi](https://cad.onshape.com/documents/28a750426de8e2bc17d5b900/w/8e79c6217ae2ce07ff57d900/e/a4d266d03289620078d13a80 "Team 1678 2023 Scoring Mechanism Onshape Document"){:target="_blank" .md-button .md-button--primary }</center>

### Talimatlar

Başlamak için, **`Main Layout Sketch` part studio'nun üzerinde yeni bir montaj sekmesi oluşturun** ve adını **`Top Level Robot Assembly`** koyun. Üst düzey robot montajını tamamlamak için **slaytlardaki talimatları izleyin**.

<!-- <center>**Top Level Robot Assembly**</center> -->
<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div id="slide1" class="mySlides fade">
    <figure>
      <img src="../images/top-level/top-level-0.webp" style="width:100%">
      <figcaption>0. Tamamlanmış üst düzey robot montajı.</figcaption>
    </figure>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/Vk3D0JNBKhI?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>1. Şasi montajını ekleyin ve origin cube'u montaj originine sabitleyin. Mate yapmak için origin cube'u göstermeniz gerekebilir.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <div class="slide-content">
      <iframe src="https://www.youtube.com/embed/KVQqbvh1NOE?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
      <figcaption>2. 1678 2023 skor montajını skor mekanizması linkini <code>Insert</code> menü metin kutusuna yapıştırarak ekleyin. Ardından, onun origin cube'unu montaj originine sabitleyin. Mate yapmak için montajın originine erişmek için şasinin origin cube'unu gizlemeniz gerekebilir.</figcaption>
    </div>
  </div>

  <div class="mySlides fade">
    <figure>
      <img src="../images/top-level/top-level-0.webp" style="width:100%">
      <figcaption>3. Tamamlanmış üst düzey montaj.</figcaption>
    </figure>
  </div>

  <!-- Next and previous buttons -->

<button class="prev" onclick="plusSlides(-1,0)"style="background-color: #000; color: #fff;">&#10094;</button>
<button class="next" onclick="plusSlides(1,0)" style="background-color: #000; color: #fff;">&#10095;</button>

  <!-- The dots/circles -->
  <div class="dotsContainer" style="text-align:center">
    <!-- Dots will be generated here -->
  </div>
</div>

!!! success "Doğrulama"
    Sekme yöneticiniz artık şöyle görünmeli:
    <figure>
    <img src="../images/tab-manager-2.webp" style="width:100%">
    </figure>

Üst düzey robot montajı bu kadar! Origin cube kullanımı montajları bir araya getirmeyi çok kolaylaştırır. Sonraki aşamalarda, origin cube ile esnek montajların (kollar, asansörler vb.) nasıl oluşturulacağını keşfedeceksiniz. İlgileniyorsanız, bir önizleme [buradan](/best-practices/assembly-setup/#utilizing-origin-cube-for-flexible-assemblies "Origin Cube Information Page"){:target="\_blank"} alabilirsiniz.

<br>
