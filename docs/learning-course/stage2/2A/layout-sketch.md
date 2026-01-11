# 2A: Basic Shooter

## Layout Sketch

Top shooter'ınızı tasarlamak için izlemeniz gereken adımlar aşağıda özetlenmiştir. Referans doküman aşağıda sağlanmıştır:

<center markdown>[Shooter Reference Document](https://cad.onshape.com/documents/8f093edaad44b5702e92ddd9/w/fefbb7a7af099fc237c1513a/e/ad76a30633d5b293d92d8217 "Shooter Reference Onshape Document"){:target="_blank" .md-button .md-button--primary }</center>

### Initial Layout

1. Origin Cube Featurescript'i kullanarak Origin Cube'ü ekleyin.
2. Etkileşmeyi düşündüğünüz saha unsurlarını eskizleyin. Sabit bir hizalama yok, ancak "Power Port"un arkadaki golüne ateş etmeyi düşünüyorsunuz, bu yüzden oyun kılavuzunu ve saha düzeni çizimlerini referans alarak bir yan görünümden bunu eskizlemeniz gerekir. Robotunuzun merkezini beyaz "başlangıç çizgisinden" 15 inç uzakta tutacak şekilde onu orijinden 135 inç uzaklığa yerleştirin

<figure>
    <img src="/img/learning-course/stage2-shooter/Field Elements.webp" width="80%">
    <figcaption>Saha Unsurları Düzeni Eskizi</figcaption>
</figure>

3. Drivetrain + bumpers'ınızın yan görünümlerini eskizleyin.
4. Çerçeve çevreniz ve yükseklik sınırlamanızla bir dikdörtgen eskizleyin. Bu, tasarım yapacağınız yerde sınırlayıcı kutunuz olur.

### Shooter Düzeni

5. Flywheel konumunu, flywheel'lerin 4 inç çapında olacak şekilde eskizleyin.
6. Flywheel'lerle eş merkezli başka bir daire çizin, yarıçapı 0.5" daha küçük. Bu, topun compression'ını telafi etmek içindir.
7. Diğer iki daireyle eş merkezli başka bir daire çizin ve bu dairenin dışını 3" compression dairenin dışından 7 inç uzakta yapın. Bu büyük daire, topun yolunu belirtmek ve sonunda topun kayacağı eğilmiş polikarbonu belirtmek içindir.
8. Hood tekerleklerini, büyük dairenin dışına teğet olan iki 2 inç daire ekleyerek eskizleyin. Bir kayış hesaplayıcı kullanarak birbirlerinden boyutlarını belirleyin.
9. Atış açınızı saha unsuru yerleşimine sınırlamak için, hood ayarlanabilir olmadığından, 3" compression dairesi ve son hood tekerleği arasında bir çizgi oluşturun, Power Port'un arkadaki golünün merkezinden bu çizginin merkezine bir yay oluşturun ve bu adımda oluşturduğunuz ilk çizgiye normal yapın. Yayın yarıçapını, yaydan memnun kalana kadar ayarlayın. Yayın kendisi gerçek hayatta, golden ne kadar uzak olduğunuza bağlı olarak flywheel'lerin hızını ayarlayarak ayarlanabilir olabilir.

<figure>
    <img src="/img/learning-course/stage2-shooter/Constrained Shot Angle.webp" width="80%">
    <figcaption>Eskizlenen Shooter Top Trajektörisi</figcaption>
</figure>

10. Flywheel'ler için motorların nereye gitmesini istediğinize karar verin ve bir kayış hesaplayıcı kullanarak flywheel merkezinden uzaklıklarını boyutlandırın.

### Feeder

11. Şimdi shooter'ın nasıl beslendiğine karar verin. Bu, indexleme sisteminin geri kalanındaki alan miktarına bağlıdır, ancak burada topların önden beslendiği ve arkadan atıldığı bir S-shape feeder kullanıyoruz. Feeder tekerlekleri (yeşil compliant tekerlekler) için iki eş merkezli daire, tekerleklerin compression'ını hesaba katmak için 3" ve 2", 2" daireyi büyük top yolu daireyle eş merkezli yaparak oluşturun. Feeder tekerleklerinizle eş merkezli final büyük top yolu daresini ekleyin ve onu flywheel'lerin orijinal 3" compression dairesine teğet yapın.
12. Power cell'leri temsil eden 7" daireleri, top yolunu daha fazla göstermek için eskizleyin.

Şimdi ana layout eskizindeki tüm geometrinin tam olarak kısıtlandığından (siyah) emin olun. Gerekirse rastgele kısıtlanmamış geometriyi kısıtlayın.

<figure>
    <img src="/img/learning-course/stage2-shooter/Finished Master Sketch.webp" width="70%">
    <figcaption>Tamamlanmış Layout Eskizi</figcaption>
</figure>

<br>
