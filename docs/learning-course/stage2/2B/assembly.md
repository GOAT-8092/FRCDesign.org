# 2B: Dingil Silisi Pivot

## Assembly

Bu alt sistem statik bir parça ve hareketli bir parça içerdiği için, bunları rijit (hareketsiz) assembly'lere ayırmak, sonra en üst seviyede birleştirmek istiyoruz. Bu, yükleme sürelerini önemli ölçüde hızlandırır.

### Base Assembly

Statik parçalar için bir assembly oluşturun, part studio'dan parçaları ve origin cube'ü yeşil işaret ile ekleyin ve bunları bir grup haline getirin. Origin cube'ü orijine sabitleyin. Part studio'dan kalan parçaları, MKCAD'den ve standart içerikten ekleyin, mümkün olduğunda replicate ve patterns kullanın.

<figure>
    <img src="/img/learning-course/stage2-pivot/Dead Axle Subassembly.webp" width="60%">
    <figcaption>Tamamlanmış Base Subassembly.</figcaption>
</figure>

### Arm Assembly

Mekanizmanın arm kısmı için bir assembly oluşturun ve assembly'yi tamamlamak ve rijit hale getirmek için yukarıdakiyle aynı şeyi yapın.

<figure>
    <img src="/img/learning-course/stage2-pivot/Arm Subassembly.webp" width="70%">
    <figcaption>Tamamlanmış Arm Subassembly.</figcaption>
</figure>

!!! Tip
    Aşağıda bir rijit assembly'nin instance listesi örneği verilmiştir. Rijit olduğunu gösteren sol üstteki ikona dikkat edin. Assembly içinde hala hareket edebilen şeyleri "serbestlik derecesi" ikonu ile (3 ekseni belirten 3 ok) söyleyebilirsiniz.
    <figure>
        <img src="/img/learning-course/stage2-pivot/deadAxleInstanceList.webp" width="80%">
        <figcaption>Bir rijit assembly'nin instance listesi.</figcaption>
    </figure>


### Top Level Assembly

Şimdi en üst seviye bir assembly oluşturun ve statik assembly'yi (orijine sabitleyin) ve intake arm assembly'yi ekleyin. Her iki assembly'deki origin cube'lardan gelen mate connectors arasında bir revolute mate oluşturun ve ona bir limit ekleyin. Bu deadaxle pivot assembly'yi tamamlar.

<center>
<figure>
    <img src="/img/learning-course/stage2-pivot/Top Level Pivot.webp" width="70%">
    <figcaption>Tamamlanmış Top Level Pivot Assembly.</figcaption>
</figure>
</center>

<br>
