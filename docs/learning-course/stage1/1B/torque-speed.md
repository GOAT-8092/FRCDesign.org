# 1B: Güç Aktarımı

## Tork ve Hız

Güç aktarım organları tasarlarken, değiştirmeye çalıştığımız birbirine bağlı iki nicelik vardır: tork ve hız. Tork bir nesneye uygulanan döner kuvvete başvururken, hız o nesnenin ne kadar hızlı döndüğünü belirtir. FRC'de hız için kullanılan birim genellikle Dakikadaki Dönüş Sayısıdır (RPM). Tork için kullanılan birim genellikle Newton-Metre'dir (Nm).

!!! Note "Tork ve Hız"
    Hız ve tork mekanik sistemlerde ters ilişkilidir. Bu, birinin artarken diğerinin azaldığı ve tam tersi anlamına gelir. Örneğin, hız 4x azaltılırsa, tork 4x artırılır. Bunun nedeni enerjinin korunumu ilkesidir: çıktı enerjisi giriş enerjisiyle aynıdır (sürtünme gibi kayıpları yoksayarsak), bu nedenle hız mekanik yollarla azaltılırsa, tork artmalıdır.

### Mekanik Avantaj

Birçok mekanik sistem, daha büyük kuvvetler veya daha hızlı hızlar üretmek için enerjiyi bir biçimden diğerine dönüştürmek için enerjinin korunumu ilkesini kullanır. ***Mekanik avantaj*** bir sistemde çıkış kuvvetinin giriş kuvvetine oranıdır, ister bir kaldıraç, vida, dişli veya kasnak olsun, mekanik avantaj kuvvetin nasıl değiştiğini ölçmek için kullanılır.

Giriş ve çıkış dişlisinin/kasnağının diş sayısı arasındaki oran, o sistemin mekanik avantajını temsil eder. Buna aynı zamanda ***dişli oranı*** da denir ve belirli bir motorun belirtilen torku ve hızından gerekli bir tork veya hızı nasıl elde edeceğinizi anlamanın anahtarıdır.

Dişli oranı genellikle `n1:n2` formunda yazılır. Tork ve hız birbirine bağlı nicelikler olduğundan, oran tork veya hız perspektifinden anlaşılabilir. Tork perspektifinden, `n1` `n2` giriş torku için çıkış torkudur. Hız perspektifinden, `n1` `n2` çıkış hızı için giriş hızıdır.

!!! Example
    Bir sistemin dişli oranı 4:1'dir. Bu, çıkış torkunun giriş torkunun 4x'i olduğu ve çıkış hızının giriş hızının 1/4'ü olduğu anlamına gelir.

Tek aşamalı bir aktarma organı için (sadece iki aktarma bileşeni), `n1`, sürülen bileşenin boyutudur, `n2` ise süren bileşenin boyutudur.

### Oran Uygulamaları

Bir kol mekanizması verimli bir şekilde kontrol etmek için çok düşük RPM'ye ama çok torka ihtiyaç duyar, bu nedenle torku artırmak için hızın büyük bir *indirgenmesi* kullanılabilir. Bu kolun ağırlığına ve uzunluğuna bağlıdır, ancak 30:1'den 200:1'e kadar olabilir.

Shooter tekerlekleri veya intake ruloları genellikle hiç veya çok az indirgeme yapar ve bazı durumlarda motorun serbest hızından daha hızlı gitmeleri gerekebilir. Bu durumda hızı artırmak için *yükseltme* kullanılabilir, ancak sonuç olarak çıkış torku daha düşük olur. Mevcut motorların zaten yüksek hızda, düşük torklu çıkışa sahip olması nedeniyle, yükseltmeler genellikle 1:2'den fazla çıkmaz. 1:2 yükseltme hızı iki katına çıkarır ve girişin torkunu yarıya indirir.

!!! Tip
    Tek bir motorun sağlayabileceğinden daha yüksek hız ve daha yüksek tork gerektiren durumlar için daha fazla motor ekleyin.

<br>
