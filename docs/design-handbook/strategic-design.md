# Stratejik Tasarım

Stratejik tasarım temellerin kutsal kasesidir. (öğrenciler ve mentörlerden oluşan sağlam bir destek yapısı ile) herhangi bir takımın performansını önemli ölçüde yükseltebilir. Stratejik tasarım; takımınızın hangi robotu yapacağına karar vermek için gereken tüm faktörler, robotu tamamlamak için başarılı bir yapım sezonu programı oluşturmak ve yarışmalarda iyi bir şekilde uygulamak hakkındadır. Öncelikler ve ödünleşimler hakkındadır. Yetenekleriniz dahilinde bir robot tasarlamak ve oyunu oynamak hakkındadır.

**Çok Yakında**

<br>

<!--

Bu sayfa henüz bitmedi ve nihayetinde stratejik tasarım için tam bir rehber olacak, ancak şimdilik, içerik için harici kaynaklar dahil edilmiştir ve bağlanmıştır. Stratejik tasarımın birçok farklı unsuru vardır ve bu sayfada bunlar bir yapım sezonunda yapacağınız sırayla formatlanmıştır.

## Genel Stratejik Tasarım Kaynakları

https://www.youtube.com/live/ENJu0In8YV8
https://www.chiefdelphi.com/t/karthik-effective-first-strategies-2024-championship-conference/461067

https://www.citruscircuits.org/uploads/6/9/3/4/6934550/strategic_design.pdf - Genel Stratejik Tasarım Sunumu (1678 Citrus Circuits)

### Hedef Belirleme

https://www.youtube.com/watch?v=TyBWSDEIuXI - Hedef Belirleme (Mike Corsetto, 1678)

## Yapım Sezonu

https://www.youtube.com/watch?v=RhfuKh0JkVc&list=PL2masFy2jbzZGhpn1gGgjQ8xQmzcICKDl&index=3&pp=iAQB - Kickoff'tan Konsepte (2910 Jack in the Bot)

## Yapım Sezonunun İlk Haftası

https://docs.google.com/presentation/d/1IXEhOXcLP8JVHVKsQoxPzVU4_HUCeys4mnsD7fESQDk/ - Strateji analizi ve robot konseptleme (Nick Coussens 8096)
https://www.chiefdelphi.com/t/progression-of-cad/440533/2 - Yapım sezonunun ilk haftası (Andrew Torrance, 254)


### Oyun Analizi

https://www.youtube.com/watch?v=T8jixiVZDhQ - Oyun Analizi (Mike Corsetto, 1678)

https://www.youtube.com/watch?v=IDsPkpojPqQ&list=PL2masFy2jbzZGhpn1gGgjQ8xQmzcICKDl&index=2 - "Modern" FRC Oyunları, Strateji, Tasarım (2910 Jack in the Bot)

https://www.youtube.com/watch?v=OIWYjbQcudo ve https://docs.google.com/presentation/d/1ds0-b_hzbc6l7c-GeNb7hqMawF7ZjPcb2eSuLVgDkA0/ - 2022 Meta Evrimi (Spectrum 3847)

https://docs.google.com/presentation/d/e/2PACX-1vQgnQDo5wF8g1wZtlIzFYa3bvkPVU2jD60h9_UDFZTh3leDYgjO3k7AUpnHIFnpYRYEgP_eX_JNe8ew/pub?start=false&loop=false&delayms=3000&slide=id.p - FRC Oyunlarına Genel Bakış (3847 Spectrum)

### Genel Mekanizma Temelleri

https://www.youtube.com/watch?v=JTZ31lpMkfA - FRC Robotlarına Genel Bakış

### Basit Tasarım

https://youtu.be/Y9B0Khob0Xk (Karthik, 2056)

https://youtu.be/JyPHwNx_KXM (Adam Heard, 254/973)

Her robotun mimarisi bir beyaz tahtaya haritalanabilir. Ancak çoğu takım bu gerçek seviyede yarışmaz (330 ve 2056 gibi birkaç takım dışında). Daha düşük tavanlara hedefleyin, ancak bunları gerçekten maksimize edin (bu basically daha az kaynak noktası belirlemenin sorun olmadığı anlamına gelir, ancak teorik kapasitenin %100'ünde çalışmalısınız. Yüksek tavanları ve daha düşük teorik kapasiteyi olan bir şeyi hedeflerseniz daha kötü performans göstereceksiniz.)

Offseason için robotlarınızı yapım sezonu ile karşılaştıramazsınız. Yarım yıl süre içinde iyi performans alabildiğiniz şeyler, 10 haftalık bir yapım sezonunda yapılan bir şeyle asla karşılaştırılamaz

Daha fazla DOF çok karmaşıktır ve gerekirse kötü değildir. El değiştirme için DOF around tasarım yaparken kendinize sormanız gereken iyi sorular, eylemlerin sırada gerçekleşmesi gerekip gerekmediğidir. Bu, iyi yapmak için uygulanması gereken bir koordinasyon seviyesi yaratır...bu bir beyaz tahtada kolay görünebilir, ancak aslında mücadele etmek çok kolaydır. Ek olarak, kontrollerin ne kadar hassas olması gerekir? Skor yapmak için çok spesifik bir açı gerekirse, bunu bozabilecek çok sayıda karışık değişken vardır (backlash, motor aşınması, zincir/kayış gerilmesi, dişli/kasnak/zincir aşınması, vb.). Döner eklemeler kontrol etmek çok zor olabilir (daha fazla matematik ve daha fazla matematik = kötü). Doğrusal çok daha kolaydır, bu gerçekten sadece yukarı / aşağı

Botunuzu bakımı çok kolay yapın. Heard, pitlerde botu ham parçalardan yeniden monte edebilmeniz gerektiğini söylüyor (bunu gerçekten yapmayın, gerçekten yapmamanızı söylüyor) ve maça gidebilir ve her şey doğru yüksekliklerde skor yapmalıdır. Ek olarak, pitlerde neye erişmeniz gerekir? Yerlerde erişim deliklerine ihtiyacınız var mı? Sisteminizi nasıl ayarlıyorsunuz? Pitlerde pratik sahası, sahte goller, kod indirme, parça değiştirme, tüm montajları ayarlama gibi harici şeylere ihtiyacınız var mı?

Kickoff'larda, oyun parçalarına ulaşmak, oyun parçasını almak, skor alanına ulaşmak, nişan almak ve skor yapmak için ne kadar süreceğini tahmin edebilirsiniz. (döngüler olarak bilinir). Tahminler için iyi bir metrik geçmiş yılların keşif verilerine, video izlemeye bakmaktır...hafızanızı kullanmamak çok önemlidir! Geçmiş yıllara bakıyorsanız, şeyleri hızlandırmak çok makuldür (Krakens ve Falcons smurf CIMS = robot daha hızlı). FRC'deki çoğu mekanizma muhtemelen daha önce yapılmıştır ve benzer kaynak / stillere sahip takımlara bakabilir ve benzer bir oyunla ne yaptıklarını görebilirsiniz. (bu, yetenekleriniz dahilinde tasarıma geri döner)

Erken iterasyon yapmak çok önemlidir-> kendi prototiplerinizi, ri3d, diğer takımların prototiplerini, döngü veri analizi / vod incelemelerini kullanın. Ne iterasyon yapacağınızı belirlemek için çok iyi bir strateji, kendinizden uzaklaşmak ve bu prototipin düşündüğünüzden daha kolay / daha zor mu olduğu kendinize sormalısınız. Ve bununla, bu döngü süresi tahminlerinizi ne olacağından daha hızlı veya daha yavaş yapar mı? (prototipler test hazırlığı gibi olmalıdır... neyin iyileştirilebileceğine gerçekten dalmalısınız, asla iyileşmezse 5 2x1 parçayı bir araya getirip buna prototip diyemezsiniz.)

Şimdi sezonun ilerleyen dönemlerinde, daha önce bahsedilen %100 teorik kapasiyeye ulaştıktan SONRA, daha karmaşık şeyler yapabilirsiniz. Örneğin 973, 2019'da seviye 1 tırmanıcı yaptı, ancak şampiyona için çatal tırmanıcı yaptı. Bu karara kendilerine şu soruyu sorarak ulaştılar: Mekanizmanın fırsat maliyeti nedir? Bot bu mekanizmadan ne kadar faydalanacak? Bunu uygulamak için çok şeyi değiştirmem gerekiyor mu? "frc'de bir şeyi ihtiyacınız olduğu zaman kadar iyi yapmak ve her şeyi gerçekten ihtiyaç duyduğunuz zaman saklamak için bir avantaj vardır

https://www.youtube.com/watch?v=j-wOaF65cTU (Mike Corsetto, 1678)

DOF'leri Kullanarak Basitliği Tanımlama: https://www.chiefdelphi.com/t/how-to-build-simple/441721/14

### Gereksinimler ve Öncelik Listeleri

### Mimari Karar

https://www.igniteminds.us/post/blocks-sketches-prototyping-in-cad

## Yarışma Sezonu

https://www.youtube.com/watch?v=huB3j6bCxmc&list=PL2masFy2jbzZGhpn1gGgjQ8xQmzcICKDl&index=4&pp=iAQB

<br>
-->
