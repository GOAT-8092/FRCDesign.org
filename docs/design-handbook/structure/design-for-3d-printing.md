# 3D Yazıcı için Tasarım
Bu rehber, FRC'de kullanılmak üzere 3D yazıcı için teknikler ve örnekler sağlar.

## Giriş

3D yazıcı için parça taslamak, 3D yazıcıların çalışma şekline göre parçanızı nasıl optimize edeceğinizi anlamak anlamına gelir. Bu fikirleri anlamanız, harcanan malzemeyi azaltmanıza, daha güçlü parçalar yapmanıza ve yazdırma süresini azaltmanıza yardımcı olacaktır.

!!! Not
    3D yazıcıya yeniyseniz [3D Yazıcıya Giriş](../intro-to-3d-printing.md "3D Yazıcıya Giriş"){:target="_blank"} sayfasına bakın.

## FRC'de 3D Yazdırılmış Parçaların Çok yönlülüğü

3D yazdırılmış parçalar bir FRC robotunun her yerinde kullanılabilir. Kasnaklardan ve sensör montajlarına kadar braketlere ve yapısal parçalara kadar, 3D yazıcı neredeyse her şeyi oluşturmak için güçlü bir çözüm olabilir.

<figure>
  <img src="/img/design-handbook/design-for-3d-printing/3dp-604-robot.png" style="width:80%">
  <figcaption>604 Quixilver 2024 - 3D yazdırılmış parçaların geniş kullanımı <figcaption>
</figure>


## 3D Yazıcıyı İşlemenin Üzerine Ne Zaman Seçmelisiniz

FRC'de 3D yazıcı kullanmanın ilk adımı, en iyi ne zaman kullanılacağını anlamaktır, genel olarak en iyisi şu durumlardadır:

1. İhtiyaçlarınız için mevcut bir COTS parçası yoktur.
2. CNC frezeleme/size mevcut diğer süreçlerden daha hızlı veya daha ucuza işlevsel olarak eşdeğer bir çözüm yazdırabilirsiniz.
3. İhtiyaç duyulan geometri, sahip olduğunuz ekipmanlarda işlenmek için imkansızdır.
4. Kavramaları hızla prototiplemek veya test etmeniz gerekir, özellikle kamera açıları, oyun parçası sıkıştırması gibi boyutları ayarlarken.
5. Parçanın eşdeğer bir metal parça kadar güçlü olmasına gerekmez.

## Bu Rehberde Kapsanan Parça Türleri

1. **Aralıklar**: Hex milleri için mill aralıkları veya plakaları veya parçaları ayırmak için ofset blok aralıkları.
2. **Ezici Bloklar:** Cıvataları sıkma kuvvetinden profilleri ezmesini önlemek.
3. **Güç Aktarımı:** Özel kasnaklar, dişliler veya zincir dişlileri yazdırın.
4. **Özel Braketler:** Yapısal bileşenler veya motor braketleri oluşturun.
5. **Sensör Montajları:** Sensörleri, kameraları veya diğer bileşenleri robot şasisine hassas bir şekilde monte etmek için montajlar oluşturun.
6. **Elektronik için Kaplar:** Hassas elektronikleri (örneğin Orange Pi, Arduino) toz, enkaz ve darbeden korumak için özel muhafazalar tasarlayın.
7. **Aletler ve Kalıplar:** Robot montajına, kalibrasyonuna veya bakımına yardımcı olmak için özel aletler, kalıplar ve fikstürler oluşturun.

FRC'de 3D yazıcı için en basit kullanım durumlarından biri, hex milleri için özel aralıklar yapmaktır. MKCAD kullanarak farklı türde aralıklar hızla yapabilir ve uzunluğu özelleştirebilirsiniz. Bunlar çok düşük maliyetle çok kolay yazdırılır. İletişim kutusunda ek tolerans (Tolerance Adder) seçeneği görebilirsiniz. 3D yazıcılar genellikle çok hassas parçalar üretebilir, ancak termal genleşme, filament tutarsızlıkları, zayıf kalibrasyon ve diğer hata kaynakları gibi faktörler parçanın boyutlarının amaçlandan daha büyük veya daha küçük olmasına neden olabilir. Bunu ele almak için, parçaların iyi bir şekilde oturması için tolerans (iki parça arasındaki boşluk) ekleyebiliriz. Muhtemelen belirli yazıcınızın elde edebildiği en iyi toleransı bulmanız gerekecektir, ancak makul bir başlangıç toleransı genellikle yaklaşık 0.004"-0.020" (0.1mm-0.5mm) olacaktır, istenen oturum türüne (müdahale, yakın, boşluk) bağlı olarak. Birçok çevrimiçi 3D baskı sitesi, belirli bir yazıcı/filament kombinasyonu için minimum toleransı bulmak için test baskıları sunar.

<figure>
  <img src="/img/design-handbook/design-for-3d-printing/3dp-spacer-example.png" style="width:60%">
  <figcaption>MKCAD Yapılandırılabilir Aralık<figcaption>
</figure>


## Ezici Bloklar

Kutu profillerine cıvatalar eklerken, özellikle 1/16" profil, cıvatanın kuvveti profili ezebilir. Ezici bloklar, cıvataları sıkmaktan kaynaklanan kuvveti yaymaya ve profilin ezilmesini önlemeye yardımcı olur. MKCAD, çeşitli profil türleri ve kalınlıkları için ayarlarla ezici blokları hızla yapmak için yapılandırılabilir bir profil plakası jeneratörüne sahiptir.

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-tube-crush.png" style="width:97%">
    <figcaption>Profil plakası olmadan profil</figcaption>
  </figure>

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-tube-crush-block.png" style="width:100%">
    <figcaption>Profil plakası ile profil</figcaption>
  </figure>
</div>


### Ezici Blokları Yazdırma İpuçları
3D yazıcıların katman katman yazdırarak çalışma şekli nedeniyle, delikler yapım plakasına paralel olarak yazdırıldığında bozulabilir. Bunun nedeni, yerçekiminin yazdırılırken sıcak filament aşağı çekecek şekilde "ezilmiş" bir daire delik oluşturmasıdır. Bir çözüm desteklerle yazdırmaktır, ancak bu destekler özellikle daha uzun deliklerde çıkarılması genellikle zordur. Bu soruna basit bir çözüm, destek olmadan yazdırmaya izin vermek için gözyaşı geometrisi kullanmaktır. Bu, bir 3D baskıdaki "taşma" veya aşağıdaki katmanları tarafından en azından kısmen desteklenmeyen alanları ortadan kaldırarak çalışır. Bunu başarmak için, yazdırıldığında yazdırmanın hangi yüzünün yapım plakasına dokunacağını planlamanız gerekir.
<figure>
  <img src="/img/design-handbook/design-for-3d-printing/3dp-crush-block.png" style="width:60%">
  <figcaption> Gözyaşı geometrisi ile örnek ezici blok (dairenin üstünde 100 derece)
<figcaption>
</figure>
<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-regular-holes.png" style="width:100%">
    <figcaption>Yuvarlak delikler destek gerektirir</figcaption>
  </figure>

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-teardrop-holes.png" style="width:95%">
    <figcaption>Gözyaşı delikleri destek olmadan yazdırılabilir</figcaption>
  </figure>
</div>



## Güç Aktarımı
### Kasnaklar
Kasnaklar 3D yazdırma için harika bir seçenek olabilir. 3D yazıcı, herhangi bir sayıda diş yapmanıza ve kasnağın diğer geometrilere nasıl monte edeceğini özelleştirmenize izin verir.

<figure>
  <img src="/img/design-handbook/design-for-3d-printing/3dp-custom-pulley.png" style="width:60%">
  <figcaption> MKCAD Yapılandırılabilir HTD Kasnak
</figcaption>
</figure>

### Kasnakları Yazdırma İpuçları
**Infill:** Güç aktarım parçaları daha fazla duvar ve daha yüksek infill yüzdesi (parçanın içindeki yoğunluk) ile yazdırılması gerekebilir. Kullanım durumuna bağlı olarak %100 infill ile yazdırmak bile gerekebilir. Daha düşük infill kullanmak baskı süresini azaltır ve ağırlığı azaltır, ancak parçanın kırılma riskini artırabilir.
<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-fill-percentage.png" style="width:94%">
    <figcaption>%13 infill ve 2 duvar ile kasnak</figcaption>
  </figure>

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-pulley.png" style="width:97%">
    <figcaption>%100 infill ve 6 duvar ile daha güçlü kasnak</figcaption>
  </figure>
</div>

**Hex Milleri İçin Inserts:** Metal ile karşılaştırıldığında, plastik nispeten yumuşaktır ve zamanla aşınabilir. Hex millerinden (özellikle Thunderhex, yuvarlatılmış kenarları vardır) gelen yüksek miktarda tork, 3D yazdırılmış bir kasnağın altı deliklerini yuvarlak bir deliğe dönüştürebilir ve sonunda mil ve kasnak arasındaki güç aktarımını ortadan kaldırabilir. Bunu düzeltmenin bir yolu, hex millerin kuvvetlerini yazdırılmış parçaya, hex delikten uzaklaştırmaya yardımcı olan metal inserts kullanmaktır.

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-pulley-insert.png" style="width:50%">
    <figcaption>3D yazdırılmış kasnağın içinde Thritybot metal insert'i</figcaption>
  </figure>

### Dişliler

Dişliler kullanım durumlarına bağlı olarak 3D yazdırılabilir. Yüksek tork gereksinimleri olan genel uygulamalar için 3D yazdırılmış dişliler uygun değildir. Ancak pençeler veya ikincil mekanizmalar gibi şeyler 3D yazıcının ağırlık tasarrufu ve esnekliğinden faydalanabilir. Aşağıdaki örnekte, 3005 Robochargers, 2023'te uç etkileşimlerinde 3D yazdırılmış dişlileri harika kullandılar.

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-3005.png" style="width:60%">
    <figcaption>3005 Robochargers 2023 - 3D yazdırılmış yapı ve dişliler ile pençe</figcaption>
  </figure>

### Dişliler için İpuçları

**Yüz Genişliği:** Yüz genişliği, iki dişli arasında temas halinde olan yüzey miktarını ifade eder. Ayrıca dişlin ne "kalın" olduğu düşünülebilir. Daha büyük bir yüz genişliğine sahip olmak, dişli üzerindeki stresi azaltır ve kırılması daha az olası hale getirir.

**Diş Gücü:** Daha düşük bir diametral pitch (pitch çemberi uzunluğu başına daha az diş) kullanmak dişleri daha kalın yapar, bu da dişliyi daha güçlü hale getirir.
Yukarıdaki ilkelerin her ikisi de 2910 tarafından bu 2022 shooter hood örneğinde kullanıldı.
  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-2910-rack.png" style="width:60%">
    <figcaption>2910 shooter 2022'de büyük bir yüz genişliğine sahip 10 DP 3D yazdırılmış rack and pinion kullanıyor</figcaption>
  </figure>

3D yazdırılmış dişliler motor pinyonları veya sürü dişlileri gibi yüksek tork uygulamalarında dikkatle kullanılmalıdır, bu uygulamalarda 3D baskı kullanmak dişlilerin hızla aşınmasına neden olabilir.

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-pinion.png" style="width:60%">
    <figcaption>604, aşınmış dişleri olan 3D yazdırılmış bir pinyon dişlisini gösteriyor </figcaption>
  </figure>


### Zincir Dişlileri

Yukarıdaki birçok ilke zincir dişlileri için de geçerlidir. Zincir dişlisinin yükü yazdırılmış malzemenin gücünü aşmadığından emin olmak için dikkat exercise edilmelidir. Herhangi bir tork aktarımı olmadığı için, 3D yazdırılmış zincir dişlileri bazen zincir gerdiriciler için idler zincir dişlileri olarak yararlı olabilir, yine yük gereksinimlerine ve filament gücüne bağlı olarak.

## Özel Braketler ve Yapı

Garip şekilli geometri gerektiğinde 3D yazıcı istisnai iyi bir çözümdür. Örneğin, 5460'ın 2023'teki kolu, geleneksel işleme yöntemleriyle yapmak zor veya pahalı olacak geometri ile inşa edildi.


  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-5460-arm.png" style="width:60%">
    <figcaption>5460 Strike Zone 2023 - Karmaşık kol parçaları için 3d yazıcının geniş kullanımı </figcaption>
  </figure>

Ancak, çoğu yapısal parça için dikkat exercise edilmelidir. Şok yüklerine yatkın parçalar kırma veya parçalanma riskinde olacaktır.

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-block-failure.png" style="width:60%">
    <figcaption>604 3D yazdırılmış parça başarısızlığı örneği </figcaption>
  </figure>


### Özel Braketler için İpuçları
Özel braketler tasarlerken, parçanın robot üzerinde nasıl monte edileceğini düşünmek kritiktir. Parçaları kolayca servis edilebilir yapmak robotunuzu yarışma sırasında daha güvenilir hale getirir.
  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-2337-arm-rest.png" style="width:60%">
    <figcaption>2337 Enginerds 2023 - Kol dinlenme braketi </figcaption>
  </figure>

Yukarıdaki örnek, çok hassas bir kol dinlenme açısının ayarlanmasına izin verdiği için 3D yazıcı için mükemmel bir kullanım durumudur. Bu, programlamanın kolun her maçta aynı konumda başlamasını sağlamak için yararlıdır. Parçanın bölünmüş tasarımı, profilleri daha güvenli bir şekilde sıkabilmesi için çok faydalıdır, değiştirmesi daha kolay olmanın ek faydası ile. Parçayı bölerek, her parçanın yazdırılırken aşağı yönlendirilebilecek düz bir yüzeyi olacak, bu da gereken destek miktarını azaltır.


Bazen 3D baskılar tek başlarına yüksek kuvvet uygulamalarına dayanacak kadar güçlü olmayabilir. Bir seçenek, bir baskıyı cıvataların sıkabileceği metal plakalarla çevrelemektir. Bu, cıvataların yükünü dağıtır ve baskıyı birlikte sıkı tutar, kırılma şansını azaltır.

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-226-arm-clamp-bracket.png" style="width:60%">
    <figcaption>226 Hammerheads 2025 - Kol eklem mafsalı </figcaption>
  </figure>

**Benzersiz Bağlama Yöntemleri:** Bazen parçalar, parçayı monte etmeyi kolaylaştırmak için bağlantı elemanlarını tutabilir. Bu, bir oyun parçası merkezleme özelliği gibi cıvatalar/somunlar içermeyen bir yüzey istiyorsanız özellikle yararlıdır.


  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-6328-centering.png" style="width:50%">
    <figcaption>6328 Mechanical Advantage 2024 - Oyun parçası merkezleme </figcaption>
  </figure>

Yukarıdaki 3D baskısı, bir oyun parçasını merkezlemek için tasarlandı. Dikdörtgen kanallara yerleştirilen kare somunlar ile monte edilir ve cıvatalar dışarıdan çalıştırılır ve onu montaj plakasına tutar. Bu, oyun parçasının takılabileceği merkezleme yüzeyinde herhangi bir cıvata veya somun olmadığı için avantajlıdır.


  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-citrus-hood.png" style="width:60%">
    <figcaption>1678 Citrus Circuits 2021 - Ayarlanabilir hood </figcaption>
  </figure>
1678'den bu özellik, oyun parçasını ayarlanabilir shooter'larından geçirmeye yardımcı olur. 3D yazıcı bu seviye geometrik karmaşıklık için mükemmel bir çözümdür.

**Parça Yönelimi:** Yapım plakasındaki parça yönelimi gücü, destek ihtiyaçlarını ve baskı süresini önemli ölçüde etkiler. Baskılar genellikle yazıcının x-y düzleminde en güçlüdür, çünkü z yönünde katmanlar delamine olabilir (ayrılabilir). z yönündeki azaltılmış güç, katman arayüzünde gerçekleşir, çünkü bir önceki biriktirilmiş filament bir sonraki katman ekstrüde edilmeden önce soğur. Farklı sıcaklıklardaki polimerler, erime noktalarındakiler kadar etkili bir şekilde birleşmez, bu nedenle sonuçta katmanlar arasındaki yapışma daha zayıftır.

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-isotropic.png" style="width:60%">
    <figcaption>
      Sol tarafta SLA baskısı (projeksiyonla ışığıyla tedavi edilmiş reçine) vs bir FDM yazdırılmış parça (bir yol izleyen bir meme ile yazdırılmış)
      <a href="https://formlabs.com" target="_blank">https://formlabs.com</a>
    </figcaption>
  </figure>
Bu resim, solda katı bir parçayı vs bir FDM yazdırılmış parçayı gösteriyor. Sol parça "izotropik" yani tüm malzeme gücü tutarlı, sağdaki parça ise "anizotropik" yani yöne göre farklı özelliklere sahip. Katmandan katmana bağlantı baskının en zayıf alanıydı ve bu testte başarısız oldu.

**Malzeme Seçimi:** Malzeme seçimi, parçanızın performansında ve güvenilirliğinde büyük bir fark yaratabilir. Örneğin Bambu Lab'ın (bir 3D yazıcı şirketi) ürün yelpazesindeki filamentler arasında, PETG, daha yaygın 3D yazıcı filamenti PLA üzerinde darbe gücünde ve çekme gücünde önemli bir iyileştirme sunar. Polikarbonat, PLA'nın neredeyse **iki katı** çekme gücüne ve bükülme gücüne sahiptir (filament spesifikasyonlarına uygun olarak düzgün bir şekilde tavlandığında) ve neredeyse **%50 daha yüksek** darbe gücüne sahiptir (ancak yazdırmak çok daha zordur). Karbon fiber infüze filamentler benzer performans iyileştirmeleri sunar ve yüksek seviye CF filamentleri alüminyuma PLA'dan daha yakın spesifikasyonlara ulaşabilir. Ek olarak, bazı şok yüklerine veya darbelere yatkın uygulamalar için TPU çok uygulanabilir olabilir. Yüksek sertlik TPU çekme özellikle güçlü değildir, ancak PLA'nın neredeyse **6x** darbe gücüne sahiptir.

## Sensör Montajları
Sensörleri veya kameraları monte etmek için 3D yazıcı harika bir çözümdür, çünkü bu cihazlar genellikle belirli açılarda çok hassas bir şekilde konumlandırılması gerekir. 3D yazıcı, kamera açılarını belirli April Etiketlerini veya oyun öğelerini görmek için yinelemeyi ve optimize etmeyi çok kolaylaştırır. Aşağıdaki 6328'nin kamera montajı örneğinde, başka bir üretim yöntemiyle yapmak oldukça karmaşık olacak bir parça oluşturabildiler.

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-camera-mount.png" style="width:50%">
    <figcaption>6328 Mechanical Advantage 2024 Kamera montajı  </figcaption>
  </figure>

3D yazıcının mükemmel olduğu diğer alanlardan biri elektroniklere strain relief eklemektir. Aşağıdaki örnekte, parçanın üstünde bir zip tie'nin girebileceği kanallar vardır ve VRM'ye giren telleri bağlamak için kullanılır. Bu, tellerin terminallerinden çekilmesini önlemeye yardımcı olur. Aynı kavram, tellerin güvenceye alınması gereken herhangi bir parçaya uygulanabilir.

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-vrm-mount.png" style="width:95%">
    <figcaption>2056 OP Robotics 2024 Tel strain relief</figcaption>
  </figure>
  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-2056-VRM-mount.png" style="width:90%">
    <figcaption>Kullanımda baskı</figcaption>
  </figure>
</div>


### Sensörler ve Strain Relief için İpuçları


Oyun parçaları veya diğer robotlar tarafından vurulabilecek sensör montajları için, daha dayanıklı malzemeler, özellikle yüksek darbe gücüne sahip malzemeler düşünün. Darbe gücü, bir malzemenin ani bir kuvvete veya şoka maruz kaldığında kırılma veya parçalanma direncini ne kadar iyi ölçüsüdür. FRC'de, hem sahanın yapımında hem de yüksek darbeli robot parçalarında polikarbonatın önemli kullanımını görebilirsiniz. Bu, polikarbonatın yüksek darbe kuvvetine dayanma ve orijinal şekline dönme yeteneğinden dolayıdır. PC bazı 3D yazıcılarda yazdırılabilir, ancak genellikle çalışmak zordur. TPU (Termoplastik Polüretan) çok yüksek darbe direnci olan bir malzeme için harika bir seçim olabilen kauçuk benzeri bir malzemedir. Buna bir örnek, 6328 Mechanical Advantage'in 2024 kamera montajlarını TPU'dan yazdırarak onları daha darbe dirençli hale getirmesidir. Malzemenin hafif esnekliği, kamera montajlarının darbelere dayanmasına ve orijinal konumlarına geri dönmelerine izin verir ve sonunda daha zayıf malzemelerle oluşabilecek katastrofik parça başarısızlıklarını önler.

## Elektronik için Kaplar
Elektronik kapları, genellikle fanlar, güç panelleri, montaj delikleri vb. gibi şeyler için karmaşık parça tasarımlarına ve özelleştirmelere güvendikleri için 3D yazıcı için harika bir kullanım durumudur.

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-electronics-case.png" style="width:55%">
    <figcaption>Orange Pi 5 Kasa <a href="https://www.printables.com/model/1008300-orangepi-5-zinc-v-case" target="_blank">Printables.com</a>
    </figcaption>
  </figure>


### Elektronik Kaplar için İpuçları

Tel yönlendirme, havalandırma ve portlara veya LED'lere erişim için yeterli açıklık olduğundan emin olun. Bileşenleri güvenli montaj özellikleriyle güvenceye alın ve pit onarımları sırasında kolay kaldırma veya bakım için plan yapın.

**Parçalara Diş Takma:** Dişleri olan bir muhafaza veya diğer parçaların cıvatalarla birbirine bağlanabilmesi istenebilir. Ancak, bir cıvatan dişine takılması ve çıkarılmasının birkaç döngüsünden sonra yumuşak plastik dişler muhtemelen aşınır. Bir alternatif, heat stake insert kullanmaktır. Bu inserts, baskıdaki bir deliğe yerleştirilir ve lehimleme ütüsü veya özel bir ısıtıcı kullanılarak plastiğe eritilir. Plastik soğuduktan sonra insert'i tutar ve bir cıvatalarken dönmesini önler.


  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-heat-stake.png" style="width:60%">
    <figcaption>Heat stake insert montajı <a href="www.isonmoulding.com" target="_blank">isonmoulding.com </a> </figcaption>
  </figure>


## Aletler ve Kalıplar

3D yazıcı, yaygın işlemler için hassas kalıplar ve fikstürler yapmak için de kullanılabilir. Aşağıdaki örnekte, kalıp, bir profil plakası için delikleri tam olarak profilin ucundan 0.5" olacak şekilde yapmak için kullanılır.

  <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-tube-jig.png" style="width:55%">
    <figcaption>Profil plakası kalıbı </figcaption>
  </figure>

### Aletler ve Kalıplar için İpuçları

Yukarıdaki parçada metal delik kılavuzları kalıbın ömrünü uzatmak için kullanılır. Kalıp sadece plastik olsaydı, tekrar tekrar deliklere delik açmaktan hızla hasar görürdü.

Yararlı olabilecek diğer kalıplar, bir profilin ortasına delik açmak, bir musluğu tam olarak düz olması için hizalamak veya profilleri ve milleri kesmek için hassas bir mesareyi işaretlemek için kalıplardır.


## Son Notlar

**Delikler ve Toleranslar:** Tam CAD boyutlarına tasarlanmış delikler genellikle malzeme genleşmesi/soğuması nedeniyle daha küçük yazdırılır. Farklı delik toleransları ile test baskıları yaparak belirli yazıcınız ve malzeme için optimal toleransları bulabilirsiniz. (örneğin. nominal bir delik boyutu için .2" .18", .19", .20", .21", .22" vb. deliklere sahip bir test parçası yazdırabilirsiniz). Hedefinize en yakın delik boyutunu bulmak, CAD'de delik boyutu olarak ne kullanmanız gerektiğini size söyleyecektir.

**Taşmalar ve Destekler için Optimize Edin:** Taşma, bir parçada aşağıdan desteklenmeyen herhangi bir yerdir. Bazı yazıcılar destek malzemesi (baskı sırasında parçayı tutmak için kullanılan ekstra malzeme) olmadan yazıcı plakası düzleminden 30 derece gibi düşük açıları idare edebilir. Taşmaları azaltmak, destek üzerinde harcanan filament atığını azaltır, parçanın yüzey kalitesini ve doğruluğunu iyileştirir ve baskı süresini azaltabilir.

   <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-supports.png" style="width:60%">
    <figcaption> Taşmaları hesaba katarak tasarlama örneği </figcaption>
  </figure>

   Destek malzemesi (yeşil) ile tutulan bir taşması olan soldaki parça, sağda ekstra geometri eklenen parçaya göre **%23 daha fazla** filament kullanır. Ek olarak, sağdaki parça daha güçlü olacaktır, çünkü taşan özellik daha iyi desteklenmektedir.


**Filletler vs Chamferler**
Filletler parçalarınızı pürüzsüz yapmak ve bazı durumlarda daha hassas yapmak için harika bir yoldur. Tipik bir FDM 3D yazıcısı, yüksek hızda hareket eden bir araç başlığı içerir ve hızlı yön değişiklikleri (örneğin 90 derecelik bir köşe) tam olarak keskin olmayacak, bu da köşelerin boyutunda hafif sapmalara neden olacaktır. Birbirine oturan parçalar için sorunlu olabilir, ancak fillet ekleyerek keskin kenarı yumuşatmak kolayca çözülebilir.
Ancak, yazıcı plakasına dokunan parça yüzeyindeki filletler, yukarıda tartışılan aynı taşma sorunu nedeniyle parçanın burkulmasına neden olabilir. Yazıcının destek olmadan yazdırabileceği bir açıda filleti bir chamfer ile değiştirmek bu sorunu çözebilir.

## Ek Kaynaklar

1. [604 Robotics Scrappy Not Crappy Presentation](https://resources.604robotics.com/presentations/2024-fmc-scrappy-not-crappy)
3. [https://blog.rahix.de/design-for-3d-printing/](https://blog.rahix.de/design-for-3d-printing/)




