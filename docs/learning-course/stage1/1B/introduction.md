

# 1B: Güç Aktarımı

## Giriş

Şu ana kadar oluşturduğunuz modellerin tümü yapısal bileşenlerdir, ancak bu bir robotu oluşturan şeyin sadece yarısıdır. Robotlarımızı hareket ettirmek ve skor yapmak için, genellikle döner hareket üreten motorlar kullanılır. Aşama 1B'de, temel *güç aktarım organlarını* modellemeye tanışacaksınız. Güç aktarım organları, motorun döner hareketini herhangi bir şeyi yapmak için dönüştürmek için kullanılan motorlar, rulmanlar, miller, dişliler, kayışlar ve zincirleri içerir.

Bu aşamada, güc aktarım organlarının temellerine odaklanacaksınız, CAD'de nasıl modelleneceklerine vurgu yaparak. Motor seçme ve güç aktarım organı oranlarını hesaplama süreci, kılavuzun Aşama 2'sinde birden fazla farklı mekanizma ile daha sonra keşfedilecektir.

### Örnekler

Aşağıda robotlarda bulunan farklı güç aktarım organı türlerinin bazı örneklerine bakın.

!!! Example "Robotlarda Güç Aktarım Organı Örnekleri"
    <center>**Güç Aktarım Organı Örnekleri**</center>
    <!-- Slideshow container -->
      <div class="slideshow-container">
      <!-- Full-width images with number and caption text -->
      <div id="slide1" class="mySlides fade">
          <figure>
              <img src="../images/examples/intake-rollers.webp" style="width:80%">
              <figcaption> Intake rulolarını döndürmek için kayış ve dişli güç aktarma organı. (Fotoğraf Kaynak: FRC 3647) </figcaption>
          </figure>
      </div>
      <div class="mySlides fade">
          <figure>
              <img src="../images/examples/intake-pivot.webp" style="width:80%">
              <figcaption> Intake'ı pivotlamak için dişli ve zincir güç aktarma organı. (Fotoğraf Kaynak: FRC 3647) </figcaption>
          </figure>
      </div>
      <div class="mySlides fade">
          <figure>
              <img src="../images/examples/shooter.webp" style="width:80%">
              <figcaption> Shooter tekerleklerini döndürmek için kayış ve dişli güç aktarma organı. (Fotoğraf Kaynak: FRC 3647)</figcaption>
          </figure>
      </div>
      <div class="mySlides fade">
          <figure>
              <img src="../images/examples/amp-arm.webp" style="width:60%">
              <figcaption> Küçük bir kolu döndürmek için dişli ve zincir güç aktarma organı. (Fotoğraf Kaynak: FRC 3647)</figcaption>
          </figure>
      </div>
      <div class="mySlides fade">
          <figure>
              <img src="../images/examples/arm-gearbox.webp" style="width:75%">
              <figcaption> Büyük bir kolu döndürmek için dişli ve zincir güç aktarma organı. (Fotoğraf Kaynak: FRC 3647)</figcaption>
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

Bu aşamada, bağımsız şanzıman şeklinde basit güç aktarım organlarını modellemeyi pratik etmek için tasarlanmış alıştırmalar vardır. Aşama 2'de, mekanizmalarla entegre edilmiş güç aktarım organlarını modellemeye başlayacaksınız.

<br>

