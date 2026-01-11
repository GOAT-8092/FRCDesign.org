---
title: Stil Kılavuzu
description: Web sitesinin hedeflerine göre katkı için stil kılavuzu.
---

# Katkı Stil Kılavuzu

## Geleceğe Hazırlık ve Yararlılık

Yazdığınız içeriğin tüm kaynak seviyeleri için takımlar için yararlı olmasını sağlamak için, aynı zamanda gelecekte geçerliliğini korumak için amaç geniş ve yüzeysel olmak değil, derinlemeye gitmektir, böylece öğrencilere kavramların arkasındaki temel ilkeleri anlama becerisini sağlayabilirler, bunları kendi benzersiz durumlarına uygulayabilirler. Artıları ve eksiler bağlama göre değişir, ilkeller evrenseldir.

Aynı zamanda, takımlar tarafından kolayca erişilebilen ve/veya yaygın olarak kullanılan şeyler, billet şasi ve ball drive gibi dahil edilmemelidir, böylece kafa karışıklığını önlenir.

Öte yandan, sadece şeyi gerçekten yaparak keşfedebileceğiniz küçük detayları dahil etmek genellikle herkes için hayat kurtarıcıdır (örneğin, cat-dili bantını sökülmemesi için elektrik bandıyla bantlamak).

### Neden bu önemli?

1. Öğrencilerin bir karar vermesi için her şeyin artılarını ve eksilerini figuring out yapmamıza gerek yok. Yeni ürünler sürekli çıkar ve onlara becerilerini kazandırmak, öğrencilerin durumları için kimse düşünmeyeceği yaratıcı çözümleri bulmalarını sağlar.

2. Bu, öğrencilerin bir takımın neden belirli bir karar verdiğini anlamalarını ve tradeoff'ları biz açıkça söylmeden figuring out yapmalarını sağlar.

3. Geleceğe hazırlamayı ve bakımı önemli ölçüde azaltır. Meta değişirse, rekabetçi kalmak için bölümleri yeniden yapmak zaman alıcıdır. Proje ölür ve artık bakım yapılmazsa, bilgi çok daha uzun süre yararlı kalır.

4. Küçük detaylar genellikle en güvenilir başarılı robotlar ve olmayanlar arasındaki deneyim farkıdır. Deneyimi olmayan takımlar için hayat kurtarıcıdır ve deneyimli tasarım mentörlerinin inceleme iş yükünü azaltır.

### Bunu kolaylaştırmak için, işte birkaç ipucu:

1. Her kavram için uç noktalar bulabilirsiniz, böylece daha belirgin hale gelir (sürtünme tekerlekleri ve pirinç flywheel'ler atalet için).

2. Bir veya iki meta takım uygulaması bulabilir ve o karar için yapılmış temel tradeoff'ları figuring out yapmak kullanışlı olabilir. Bu, öğrenicilerin bu kavramların birbirleriyle nasıl ilişkili olduğunu anlamalarına yardımcı olur. Bu ayrıca mekanizma örnekleri için de geçerlidir.

3. "xyz'yi nasıl cad yaparım" ve gerçek hayattaki nüanslar belirli uygulamalar için çok yararlıdır. Örnekler arasında linkage sketch'lemek veya yüke bağlı olarak gerginlik yerleşimi vardır.

## gm0'nun Stil Kılavuzundan Esinlenen

Mutlaklarda uğraşmayın.

- sadece bir Sith mutlaklarda uğraşır
- seçenekleri karşılaştırmak için artı/eksi listeleri kullanın
- Neden bir şeyin iyi veya kötü olduğunu açıklayın
  - Örneğin, hepimiz biliriz ki deadaxle pivot'lar liveaxle'den daha iyidir. Ama sadece onların daha iyi olduğunu söylemeyin, şöyle deyin: "Deadaxle'ler, torkun doğrudan parçaya aktarıldığı için daha yüksek ikinci moment of alana sahiptir. Sonuç olarak, pivotunuz çok daha sağlamdır ve kırılmaya daha az eğilimlidir."
  - Benzer şekilde, Kraken motorların genellikle iyi olduğunu biliyoruz. Ama neden iyi olduklarını açıklayın, örneğin: "Drivetrain'inizde Kraken kullanmanızı öneririz, çünkü bunlar aşırı yüksek torklu motorlardır ve ivmelenmenizi iyileştirir. Ayrıca, wiring'lerini kolaylaştıran entegre Talon FX motor denetleyicilerine sahiptirler ve swerve odometrinizin hassasiyetine yardımcı olan yüksek çözünürlüklü bir encoder içerirler. Kraken motorların henüz stok REV Maxswerve modülleriyle uyumlu olmadığını ve diğer mevcut modüllerle eşleştirmek için WCP'den ek bir adaptör gerektirdiğini unutmayın."
- Yine de takımların keşfetmeye ve yenilik yapmekte özgür olduklarını vurgulayın, ancak gerçekçi beklentiler ayarlamaya yardımcı olun (aşağıdaki noktaya bakın)

FRCDesign.org rekabetçi bir bakış açısından bir kılavuzdur.

- İyi çalışmayan ve popüler olmayan şeyleri dışarıda bırakmaya çalışın; popülerse, dezavantajlarını açıklamaya değer (bkz. tank drive vs mecanum drive; tank drive'i, nispeten popüler ve basit bir drivetrain olarak açıklamak mantıklıdır, ancak mecanum drive, swerve çağında artık anlama alan bir drivetrain değildir ve çok az veya hiç itme gücü veya çekişi vardır.)

- Mümkün olduğunca görüşleri dışarıda bırakmaya çalışın. Birinci el deneyiminiz olmadığı şeyler hakkında otoriter bir dille konuşmaktan kaçının

FRC tasarım trendlerinin geçici ve geçici olduğunu unutmayın.

- Bir şeyin bir sezon popüler olması, her şey demek değildir. Bir zamanlar WCD ve sheet metal süper yapıları çok popülerdi, ancak bu onları bu kılavuzda önermemiz gerektiği anlamına gelmez. Bir şeyin neden popüler olduğunu ve tasarıma, işlevselliğe ve uygulamaya gerçekten ne gibi faydalar getirdiklerini düşünmek için elinizden geleni yapın.

<!-- Mekanizma örneklerini eklemek gerçekten bilgi transferine yardımcı olur.

Takımlara kredi: Başlık formatı: [Takım Numarası] [Takım Adı], (İlgili Başarı), [Sezon], (açıklama)

[] sürekli, () ise ilgili olduğunda demektir

Aynı takımın aynı parçasından birden fazla resminiz varsa, tekrarlamaktan kaçınmak için sadece sonuncusuna kredi verin.

Örnekler

11115 Gluten Free, Finalist Alliance Captain (Detroit), Relic Recovery, springloaded

8417 'Lectric Legends, Rover Ruckus, TPU intake flaps

7236 Recharged Green, Rover Ruckus, Misumi SAR3 -->

## Standartlar

### Dosya Biçimleri:

- Resimleri [squoosh](https://squoosh.app/ "sqoosh Resim Sıkıştırıcı"){:target="\_blank"} kullanarak .webp biçiminde sıkıştırın
- Daha uzun videoları bir Youtube gömme ile, daha kısa videoları bir webm dosyası ile gömün
- Resimleri `<center><img src="mutlak link" width="x%"></center>` kullanarak ekleyin

### Marka Standartları

Mümkün olduğunda marka standartlarına uyun.

- FIRST® Ticari marka yönergelerine uyun, [burada](https://www.firstinspires.org/sites/default/files/uploads/resource_library/UseofUSFIRSTandLEGOGroupTrademarksandCopyrightedMaterials.pdf "FIRST Ticari Marka Yönergeleri"){:target="_blank"} mevcuttur
- Bir sayfadaki _FIRST_ ve FRC'nin ilk örneği ® içermelidir (örneğin, FIRST®)
- _FIRST_ adını her zaman büyük harf ve italik yapın
- _FIRST_ adına possessive kullanmayın (örneğin, FIRST'in)
<!-- gm0 değil GM0 damn it; logoya bakın. -->
Bu ayrıca takım adları için de geçerlidir: takımları resmi olarak nasıl yazıldıkları gibi yazın
Bir takımın adını nasıl yazacağınızı bilmiyorsanız [The Blue Alliance](https://www.thebluealliance.com/ "The Blue Alliance"){:target="_blank"} kontrol edin

Yazarken "siz" (you) kullanabilirsiniz, ancak yazmayı daha az garip hale getirdiğinde. Ancak, aşırı kullanmaktan kaçının.

### Bağlantılar:

- Dış bağlantılar yeni bir sekmede açılmalıdır: `[Link Metni](link_url "Link Başlığı"){:target="_blank"}`
  - CAD belgelerine bağlantılar büyük ortalanmış bir buton kullanmalıdır: `<center markdown>[Link Metni](link_url "Link Başlığı"){:target="_blank" .md-button .md-button--primary}</center>`
  - Onshape belgeleri için bağlantı başlıkları `[Belge adı] Onshape Belgesi` olmalıdır
- İç bağlantılar mevcut sekmede açılmalı ve göreceli bir bağlantı kullanmalıdır: `[Link Metni](göreceli_bağlantı "Link Başlığı")`
  - İç bağlantılar için bağlantı başlıkları `"[Sayfa Adı] Sayfası"` biçiminde olmalıdır

<br>
