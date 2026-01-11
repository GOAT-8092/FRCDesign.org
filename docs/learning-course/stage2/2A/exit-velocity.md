# 2A: Basic Shooter

## Exit Velocity

### Surface Speed

Oyun parçasının çıkış hızı öncelikle flywheel'in yüzey hızı tarafından kontrol edilir. Yüzey hızı, tekerleğin dakikadaki devir sayısı (RPM) ve çapı tarafından belirlenir. Çapı artırmak genellikle daha verimlidir çünkü daha düşük RPM ile aynı yüzey hızına ulaşır. Yaygın bir seçim 4 inç çapında bir tekerlektir. Tüm değişkenler arasında, RPM ve isteğe bağlı olarak atış açısı yazılımda kontrol edilebilen tek faktörlerdir.

Flywheel shooterlar için genellikle iki CIM sınıfı brushless motor kullanılır.

### Eylemsizlik

Bir seferde tek bir oyun parçası fırlatılırken, flywheel tekerlekleri için yaygın seçenekler stealth wheels, Colsons ve solid roller wheels'dur. Bu seçenekler tutarlı bir atış için yeterli enerji depolarlarken dayanıklıdırlar. Yüksek hızlarda genişlemeye veya arızalanma eğilimi gösterdikleri için compliant veya treaded tekerleklerden kaçının.

Oyun parçası her fırlatıldığında, flywheel enerji kaybeder ve oyun parçası tekerleğin hızına uyum sağladıkça yavaşlar. Birden fazla oyun parçası fırlatılırken, bu atışlar arasında gecikmelere neden olabilir. Flywheel'e kütle eklemek onun [moment of inertia](https://en.wikipedia.org/wiki/Moment_of_inertia "MOI Wikipedia Page"){:target="_blank"} artırır, bu da atış başına enerji kaybını en aza indirerek atışlar arasındaki süreyi azaltır. Takas, başlangıçta hedef hıza ulaşmak için daha uzun bir spin-up süresidir.

<br>

<div class="grid cards" markdown>

-   <center><img src="\img\learning-course\stage2-shooter\2056.gif" width="100%" style="border:5px solid #ADADAD; border-radius: 2%"></center>

-   <center><img src="\img\learning-course\stage2-shooter\118.gif" width="81%" style="border:5px solid #ADADAD; border-radius: 2%"></center>

</div>

<figure>
<figcaption> Takım 2056 ve 118, yüksek moment of inertia shooter tekerleği kullanarak hızlı bir şekilde atış yapıyor </figcaption>
</figure>
<br>

İvme ve iyileşme süreleri, motorlarınızı uygun şekilde dişlendirerek veya ek motorlar ekleyerek iyileştirilebilir.

### Referans Tasarım

Referans tasarımda, herhangi bir brushless CIM sınıfı motor yeterli olacaktır ama iki Kraken X60 motor kullanılmaktadır.

<figure>
<img src="/img/learning-course/stage2-shooter/motorsAndFlywheels.webp" width="60%" style="border-radius: 2%">
<figcaption>İki Kraken, shooter tekerleklerini, flywheel'leri ve hood tekerleklerine güç transfer eden bir kayışı sürüyor.
</figure>


### Flywheel Hesaplayıcı

Optimal diş oranını belirlemek için kullanışlı bir araç [ReCalc Flywheel Calculator](https://www.reca.lc/flywheel "ReCalc Flywheel Calculator"){:target="_blank"} aracıdır. Bu araç, giriş parametrelerine dayalı olarak spin-up süresi, iyileşme süresi ve tahmini mermi hızını hesaplar. Performansı optimize etmek için hedef shooter RPM'ini, diş oranını ve flywheel kütlesini ayarlayabilirken, bu oyun için mermi hızının 12 m/s'nin üzerinde kalmasını sağlayabilirsiniz. Bu shooter tasarımı için, [hesaplamalar](https://www.reca.lc/flywheel?currentLimit=%7B%22s%22%3A40%2C%22u%22%3A%22A%22%7D&efficiency=90&flywheelMomentOfInertia=%7B%22s%22%3A24.688%2C%22u%22%3A%22in2%2Albs%22%7D&flywheelRadius=%7B%22s%22%3A4%2C%22u%22%3A%22in%22%7D&flywheelRatio=%7B%22magnitude%22%3A1%2C%22ratioType%22%3A%22Reduction%22%7D&flywheelWeight=%7B%22s%22%3A3.086%2C%22u%22%3A%22lbs%22%7D&motor=%7B%22quantity%22%3A2%2C%22name%22%3A%22Kraken%20X60%2A%22%7D&motorRatio=%7B%22magnitude%22%3A1.33333%2C%22ratioType%22%3A%22Reduction%22%7D&projectileRadius=%7B%22s%22%3A2%2C%22u%22%3A%22in%22%7D&projectileWeight=%7B%22s%22%3A5%2C%22u%22%3A%22oz%22%7D&shooterMomentOfInertia=%7B%22s%22%3A16.056%2C%22u%22%3A%22in2%2Albs%22%7D&shooterRadius=%7B%22s%22%3A4%2C%22u%22%3A%22in%22%7D&shooterTargetSpeed=%7B%22s%22%3A3000%2C%22u%22%3A%22rpm%22%7D&shooterWeight=%7B%22s%22%3A2.007%2C%22u%22%3A%22lbs%22%7D&useCustomFlywheelMoi=0&useCustomShooterMoi=0 "ReCalc Calculations for Example ShooteR"){:target="_blank"} ReCalc ile yapıldı, bu da 4 inç shooter tekerlekleri için 4:3 redüksiyon ve iki 4 inç pirinç flywheel seçimine yol açtı.

!!! Note
    Redüksiyonlar veya upductions yüksek verimlilik ve düşük bakım nedeniyle kayışlarla yapılmalıdır. Flywheel'da 24 dişten daha büyük kasnaklar kullanın ve enerji transferini en üst düzeye çıkarmak ve kayış kaymasını önlemek için yüksek diş temasını sağlayın.

<br>
