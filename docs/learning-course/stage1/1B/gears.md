

# 1B: Güç Aktarımı

## Güç Aktarım Organları
FRC'de, en yaygın üç güç aktarım organı türü dişli, zincir ve dişli ve kayış ve kasnaktır. Hepsi aynı sonucu olan hız ve torku değiştirmeyi başarsalar da, her biri farklı durumlarda mükemmel olur. Aşağıdaki bölümlerde her biriyle ve bunları nasıl modelleyeceğinizle tanışacaksınız.

!!! Note
    Dişliler, kasnaklar ve dişliler, dişlerin ne kadar büyük olduğunu belirleyen profil standartlarına uyar. Bu, diş sayısı ile parçanın çapı arasındaki oranın sabit olduğu anlamına gelir. Farklı profil standartları vardır, ancak aynı profilin parçaları sadece birlikte meshleşebilir veya kullanılabilir.

## Dişli Temelleri

Dişliler, dönen miller arasında hareket veya gücü iletmek için birbirine meshleşen dişlere sahip mekanik cihazlardır. Birbirine uygun dişli tekerlekler gibidirler, tork aktarmalarına, hızı değiştirmelerine ve dönüş yönünü değiştirmelerine izin verirler.



<div class="grid cards" markdown>

- <center><img src="../images/gears/simple-gears.gif" style="width:100%"></center>

- <center><img src="../images/gears/gearbox-animated.gif" style="width:100%"></center>

</div>
<figcaption>Dişli meshleşme animasyonları. Meshleşmiş dişlilerin zıt yönde döneceğini unutmayın.</figcaption>

Girişten çıkışa tork ve hızı değiştirmek için, farklı boyutlarda dişliler kullanılmalıdır. Oranın dişlilerin diş sayısı ile ilgili olduğunu unutmayın. Dişler her zaman tek tek meshleşir, ancak farklı boyutlu dişliler için devir başına diş sayısı farklıdır, bu da dişlin yüzey hızı aynı olsa bile açısal hızda bir farka neden olur. Farklı dişli oranlarının görselleştirmesini görmek için aşağıdaki slaytlara tıklayın.

<center markdown>**Dişlilerle Hız ve Torku Değiştirme**</center>
<!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
<div id="slide1" class="mySlides fade">
    <figure>
        <img src="../images/gears/gear-reduction.webp" style="width:100%">
        <figcaption>1. 12 dişli bir dişli 84 dişli bir dişliyi sürer. Dişli oranı 84:12'dir, bu da 7:1 olarak basitleştirilebilir. Tork 7x artırılırken hız orijinal h hızın 1/7'sine düşürülür. (Görsel kaynak: <a href="https://docs.wcproducts.com/frc-build-system/belts-chain-and-gears/gears">WCP</a>)</figcaption>
    </figure>
</div>

<div class="mySlides fade">
    <figure>
        <img src="../images/gears/gear-upduction.webp" style="width:100%">
        <figcaption>2. 48 dişli bir dişli 24 dişli bir dişliyi sürer. Dişli oranı 24:48'dir, bu da 1:2 olarak basitleştirilebilir. Tork orijinal torkun 1/2'sine düşürülürken hız 2x artırılır. (Görsel kaynak: <a href="https://docs.wcproducts.com/frc-build-system/belts-chain-and-gears/gears">WCP</a>)</figcaption>
    </figure>
</div>

<div class="mySlides fade">
    <figure>
        <img src="../images/gears/gear-swap.webp" style="width:100%">
        <figcaption>3. Aynı boyut dişliler kullanılırsa, hızda ve torkta değişiklik yoktur. Ancak, girişten çıkışa kadar dişli sayısı çift ise dönüş yönü tersine çevrilir. Dişli sayısı tek ise yön aynı kalır. (Görsel kaynak: <a href="https://docs.wcproducts.com/frc-build-system/belts-chain-and-gears/gears">WCP</a>)</figcaption>
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

### Merkezden Merkeze Hesaplama

Dişlilerin ne kadar uzakta yerleştirileceğini hesaplamak için, merkezden merkeze mesafeyi hesaplamak için aşağıdaki formülü kullanabilirsiniz:


<center><code><b>C2C = 0.5 * PD1 + 0.5 * PD2</b></code></center>


Burada `PD1` ve `PD2` iki dişlinin *Çap Çapı*'dır. **Çap Çapı (PD)**, dişlinin diş merkezinden geçen hayali dairenin boyutudur. İki dişlinin çap çaplarının dişlilerin düzgün meshleşmesi için tangent olması gerekir. PD için denklem şöyledir:

<center><code><b>PD = (# of teeth) / DP</b></code></center>

Burada DP **diametral pitch** anlamına gelir. Şimdilik, her zaman 20 olduğunu varsayabilirsiniz. Merak ediyorsanız, Design Handbook sayfalarında bunun hakkında daha fazla bilgi edinebilirsiniz.

<figure>
    <img src="../images/gears/gear-diagram.webp" style="width:70%">
    <figcaption>Bir dişlinin çap çapı ve dış çapının çizimi. (Görsel kaynak: <a href="https://docs.wcproducts.com/frc-build-system/belts-chain-and-gears/gears">WCP</a>).</figcaption>
</figure>

### Dişli Aktarma Organlarını Modelleme

Modelleme sırasında, iki dişli arasındaki merkezden merkeze mesafeyi ayarlamanın kolay bir yolu, dişlilerin çap çaplarına boyutlandırılmış iki daire çizmek ve ardından iki daireyi birbirine tangent olacak şekilde ayarlamaktır. Örneğin, 20 dişli bir dişliyi 60 dişli bir dişliye meshlemeniz gerekiyorsa, `20/20 = 1"` ve `60/20 = 3"` daire çizebilir ve iki daire arasında tangent constraint ekleyebilirsiniz.

<figure>
<img src="../images/gears/gear-cad.webp" style="width:60%">
<figcaption>İki çap çapı construction daire tangent kısıtlayarak dişli C-C mesafesini modelleme. Dairelerin çapları, diş sayısının DP'ye (bu durumda 20) bölünmesiyle hesaplanır.</figcaption>
</figure>

Hesaplanan çap çapını (Örneğin: sadece `3"` dimension girişi) girmek yerine, çap çapı fraksiyonunu girmeniz önerilir (Örneğin: `(60/20)"`), böylece dairenin neyi temsil ettiğini (dişli, kasnak veya dişli) ve kaç diş olduğunu kolayca görebilirsiniz.

!!! Tip
    Bir dimension'ın hangi ifadeden değerlendirildiğini sketch menüsündeki <code>Show Expression</code> onay kutusunu işaretleyerek gösterebilirsiniz. Sonuç önceki görüntü gibi görünecektir, bu da iki dişlinin 20 dişli ve 60 dişli bir dişli olduğunu ve her ikisinin de 20 DP olduğunu kolayca görmenizi sağlar.

<br>





