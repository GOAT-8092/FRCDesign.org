

# 1E: Alt Sistem İş Akışı - Drivebase Detaylandırma

## Egzersiz: Elektronik Montajı

Referans tasarımda, Power Distribution Hub (PDH), ana şalter ve RoboRIO bellypan üzerine monte edilmiştir. [`Elektronik Montaj` Featurescript](https://cad.onshape.com/documents/95c00401c440b44ad8799ef5/w/1f1ebce01a3b8eb6fa102975/e/83cfa4ae1a46ea05581445c9 "Elektronik Montaj Featurescript Onshape Belgesi"){:target="_blank"}, elektronikler için montaj deliklerini oluşturmak için çok yararlı olabilir. Elektronikler için montaj deliklerini doğru bir şekilde üretemezseniz, (Kit of Parts'ta gelen) VHB bandı elektroniklerinizi güvenli şekilde sabitlemek için iyi bir seçenek olabilir.

### Bellypan Montaj Talimatları

**Drivetrain'inize bazı elektronik bileşenler için montaj ekleyin.** Aşağıdaki talimat slaytlarından ilham alabilirsiniz.

<!-- <center>**Örnek Elektronik Montaj Slaytları**</center> -->
<!-- Slideshow container -->
<div class="slideshow-container">
    <!-- Full-width images with number and caption text -->
    <div id="slide1" class="mySlides fade">
        <figure>
            <img src="../images/elec/elec-0.webp" style="width:100%">
            <figcaption>0. Tamamlanmış monte edilmiş elektronik.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/elec/elec-1.webp" style="width:100%">
            <figcaption>1. PDH ve RoboRIO için kutu çizimi çizin. Ayrıca ana şalter ve takımınızın kullandığı herhangi bir IMU (Pigeon 2.0, Canandygro, vb.) için çizim ve delikleri ekleyin. Bu boyutları satıcı web sitelerindeki pdf dosyalarında veya FRCDesignLib'deki CAD modellerini ölçerek bulabilirsiniz.</figcaption>
        </figure>
    </div>
    <div class="mySlides fade">
        <div class="slide-content">
            <iframe src="https://www.youtube.com/embed/_Yyt5wFeIDk?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
            <figcaption>2. PDH ve RoboRIO montaj deliklerini eklemek için <code>Elektronik Montaj</code> Featurescript'ini kullanın. İsteğe bağlı olarak PDH için delik boyutunu 0.159" çapına ayarlayın, bu (gerçekte tapped edilirse) montaj vidasının doğrudan bellypan'a vidalanmasına izin verir.</figcaption>
        </div>
    </div>
    <div class="mySlides fade">
        <figure>
            <img src="../images/elec/elec-0.webp" style="width:100%">
            <figcaption>3. FRCDesignLib'den elektronikleri ekleyin ve gerekli tüm bağlantı elemanlarını ekleyin. PDH #10-32 vidalar kullanır, RoboRIO #4-40 vidalar kullanır, Breaker 1/4-20 vidalar kullanır, Pigeon 2.0 #6-32 vidalar kullanır ve Canandgyro #8-32 vidalar kullanır.</figcaption>
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

!!! İpucu "Basitleştirilmiş Modeller"
    Assembly performansını artırmak için basitleştirilmiş elektronik modellerini kullanmanız önerilir. Basitleştirilmiş modeller hakkında daha fazla bilgiyi [Assembly En İyi Uygulamalar Sayfasında](/best-practices/assembly-setup/ "Assembly En İyi Uygulamalar Sayfası"){:target="_blank"} okuyabilirsiniz. Gecikmeyi azaltmak için basitleştirilmiş swerve modül modelleri de kullanılabilir.

### Robot Sinyal Işığı (RSL)

Her robotun ayrıca bir Robot Sinyal Işığı (RSL) olması gerekir. RSL'yi montaj etmek için kolay bir konum drive frame'in kenarıdır. Tipik olarak, sadece bir RSL gerekir ve "robotun en az bir tarafından 3 ft. (~ 100 cm) uzaklıkta dururken kolayca görülebilir" olması gerekir. En güncel RSL montaj kuralları için en son oyun kılavuzu kurallarını kontrol ettiğinizden emin olun.

**Stage 1D drivetrain'inize bir RSL için montaj ekleyin.** Aşağıdaki görselden ilham alabilirsiniz.

<figure>
    <img src="../images/elec/elec-rsl.webp" style="width:80%; border:5px solid #ADADAD; border-radius: 2%">
    <figcaption>1/8" kalınlığında polikarbonat plakadan yapılmış RSL montajı. Klasik RSL için montaj deliği 1" çapındadır. Hem klasik hem de yeni RSL modelleri FRCDesignLib'de bulunabilir.</figcaption>
</figure>

### Radyo

Her robotun ayrıca bir radyosu olması gerekir. Radyo Vivid Hosting'in [radyo montaj yönergelerine](https://frc-radio.vivid-hosting.net/getting-started/usage/mounting-your-radio "Vivid Hosting Radyo Montaj Yönergeleri"){:target="_blank"} uygun olarak robot üzerine monte edilmelidir.

<figure>
    <img src="../images/elec/elec-radio.webp" style="width:80%; border:5px solid #ADADAD; border-radius: 2%">
</figure>

<br>
