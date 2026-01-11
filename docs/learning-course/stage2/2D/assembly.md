# 2D: Kaskat Asansör

## Assembly

Bu alt sistem birden fazla hareketli parça içerdiğinden, dead axle pivot ve slapdown intake gibi, her aşama için rijit subassembly'ler oluşturulmalıdır.

### Base Stage Assembly

Statik parçalar için bir assembly oluşturun ve bunları eklemek ve rijit bir gövde oluşturmak için tipik süreci izleyin (origin cube, grup, orijine sabitle). Mevcut parçaları çoğaltarak, MKCAD'den ve standart içerikten kalan parçaları ekleyin, mümkün olduğunda replicate ve patterns kullanın.

<figure markdown="span">
    <img src="/img/learning-course/stage2-elevator/frameSubassembly.webp" style="width:85%">
    <figcaption>Tamamlanmış taban aşaması assembly</figcaption>
</figure>

### First Stage Assembly

Birinci aşama subassembly için aynı şeyi yapın.

<figure markdown="span">
    <img src="/img/learning-course/stage2-elevator/stage1Subassembly.webp" style="width:85%">
    <figcaption>Tamamlanmış birinci aşama assembly</figcaption>
</figure>

### Carriage Assembly

Ve son olarak carriage subassembly.

<figure markdown="span">
    <img src="/img/learning-course/stage2-elevator/carriageSubassembly.webp" style="width:75%">
    <figcaption>Tamamlanmış carriage assembly</figcaption>
</figure>

### Top Level Assembly

Şimdi en üst seviye assembly'yi oluşturun, subassembly'leri ekleyin (statik assembly'nin origin cube'ünü orijine sabitleyin) ve ayrı subassembly'lerdeki origin cube'lardan gelen referans mates'leri kullanarak asansörün hareketini tanımlamak için limitlerle slider mates'ler oluşturun.

<figure markdown="span">
    <img src="/img/learning-course/stage2-elevator/elevatorTopLevel.webp" style="width:75%">
</figure>

Bu bir kaskat asansör olduğu için, iki slider mate arasında 1:1 oranında "Linear Relation" assembly aracını kullanarak aşamaların hareketini gerçek hayatta olduğu gibi birbirine bağlayabilirsiniz.

<br>
