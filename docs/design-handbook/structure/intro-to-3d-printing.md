# 3D Yazıcıya Giriş

3D yazıcıya ve FRC robotlarındaki kullanım durumlarına genel bakış.

## FRC için 3D Yazıcının Gücü

1. **Robot bileşenlerinin hızlı iterasyonunu ve prototiplemesini sağlar.**
   3D yazıcı, fiziksel prototiplerin hızlı üretilmesine izin verir. Onları test edebilir, kusurları bulabilir ve tasarımları hızla iyileştirebilirsiniz. Bu tasarım döngüsünü hızlandırır ve bu FRC için kritiktir.

2. **Benzersiz zorluklar için özel, uzman parçaların oluşturulmasını kolaylaştırır.**
   FRC Robotları genellikle benzersiz 3D geometrilere ihtiyaç duyar. 3D yazıcı, diğer üretim yöntemleriyle genellikle mümkün olmayan geometriyi sağlar.

3. **Hafif ama güçlü tasarımlara bir yol sunar.**
   3D yazıcı, parçanın içinde "infill" adı verilen karmaşık iç yapılar oluşturarak genel malzeme kullanımını ve ağırlığı azaltmanızı sağlar. Bu, gereken yerlerde gücü korurken veya artırarak yapılabilir ve daha hafif mekanizma tasarımlarını sağlar.

4. **Özel parçalar için uygun maliyetli bir üretim çözümü sunar.**
   3D yazıcı, özel parçalar yapmak için uygun maliyetli bir yol olabilir. 1 kg / 2.2 lbs temel yazıcı malzemesi (filament) 20 USD'nin altında alabilirsiniz.

## 3D Yazıcının Temel Kavramları

### 3D Yazıcı Nedir?

Çıkarmalı üretim (örneğin CNC frezeleme) ilk formdan malzeme çıkararak son parçayı ortaya çıkarır. 3D yazıcı veya eklemeli üretim, nesneleri katman katman inşa eder.

   <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-process.png" style="width:60%">
    <figcaption>3D yazıcı işlemi </figcaption>
  </figure>

### 3D Yazıcı İş Akışına Genel Bakış

1. **Tasarımdan (CAD) Dışa Aktarma** Tasarımınız oluşturulduktan sonra, 3D yazıcı yazılımı üzerinden işlemeniz gerekir, bu yüzden onu CAD yazıcınızdan dışa aktarmanız gerekir.

2. **Dilimleme** Dilimleme yazılımı modeli yatay katmanlara "dilimler". Sonra G-code oluşturur: yazıcıya her katmanı nasıl yazdıracağını söyleyen talimatlar, meme hareketlerini, sıcaklıkları ve hızları içerir. Parça infill, malzeme, destekler vb. gibi şeyleri yapılandırdığınız yer burasıdır.
3. **Yazdırma** G-code 3D yazıcıya yüklenir ve malzemeyi katman katman hassas bir şekilde biriktir, nesneyi aşağıdan yukarıya doğru tamamlanana kadar inşa eder.
4. **Son İşleme** Yazdırdıktan sonra, bazı parçaların daha fazla işleme ihtiyacı olabilir. Son işleme, destek yapılarının çıkarılmasını, zımparalanmasını, boyanmasını veya birden fazla yazdırılmış bileşenin montajını içerebilir.

## 3D Yazıcı Türleri

Birçok 3D yazıcı teknolojisi vardır, ancak Fused Deposition Modeling (FDM) en yaygın ve erişilebilir olandır. Yaygın FDM yazıcıları Prusa, Bambu Lab, Creality, Stratasys ve Markforged gibi şirketler tarafından üretilir.

   <figure>
    <img src="/img/design-handbook/design-for-3d-printing/3dp-bambu-a1.png" style="width:60%">
    <figcaption>Bambu A1 <a href="http://Bambulab.com" target="_blank">Bambulab.com </a></figcaption>
  </figure>

### Fused Deposition Modeling (FDM)

FDM yazıcıları filamenti ekstrüdere besler, eritir ve ısıtılmış bir memeden geçirir. Eritilmiş plastik ince çizgiler halinde yapım plakasına biriktirilir, ilk katmanı oluşturur. Yazıcı kafası yukarı hareket eder ve bir sonraki katman soğuduğunda tutunur. Bu nesne tamamlanana kadar tekrarlanır.

1. **Avantajları (Uygun Fiyat, Malzeme Çeşitliliği, Kullanım Kolaylığı)** FDM yazıcıları genellikle uygun fiyatlıdır ve eğitim için harikadır. Birçok termoplastikle yazdırırlar ve nispeten basit çalıştırılırlar.
2.  **Dezavantajları (Katman Çizgileri, Anizotropi)** FDM baskılar genellikle görülebilir katman çizgileri gösterir. Parçalar anizotropik olabilir, bu da kuvvetin farklı yönlerde uygulanmasına bağlı olarak gücün değiştiği anlamına gelir. FDM parçaları genellikle X ve Y eksenleri boyunca en güçlüdür ve yazıcının Z ekseni (yazıcı plakasına normal) boyunca daha zayıftır.

### Diğer Yazıcı Türleri

1. **Stereolitografi (SLA):** Sıvı reçineyi katman katman tedavi etmek için bir UV lazer kullanır. Yüksek detay ve pürüzsüz yüzeyler ile bilinir, ancak reçineye bağlı olarak parçalar kırılgan olabilir.
2. **Digital Light Processing (DLP):** SLA'ya benzer, ancak daha hızlı baskılar için tüm reçine katmanlarını bir seferde tedavi etmek için bir projektör kullanır. Tipik olarak daha pahalı bir teknolojidir.
3. **Selective Laser Sintering (SLS):** Toz malzemeyi (örneğin naylon) katman katman birleştirmek için bir lazer kullanır. Desteksiz güçlü, işlevsel parçalar üretir.

### Dilimleme Yazılımı

Dilimleme yazılımı 3D modelinizi 3D yazıcınıza bağlar. Tasarımınızı yazıcı talimatlarına çevirir.

1. **Slicer Nedir?** Bir slicer, 3D modeli (STL veya OBJ) alır ve onu ince katmanlara dönüştürür. Her katman için, takım yollarını, ekstrüzyonu, sıcaklıkları ve hızları belirler. Yazıcının eylemlerini yönlendiren bir dil olan G-code'u üretir.
2. **Popüler Slicer'lar** Bazı yazıcılar belirli slicer'lar gerektirir, ancak diğerleri bir dizi slicer ile uyumludur. Yaygın slicer'lar Bambu Studio, Prusa Slicer, Orca Slicer ve Cura'dır.
3. **Slicer Kurulumu** 3D modelleri dilimlemenin birçok inceliği vardır ve bu rehberde kapsanmamaktadır. Daha fazla öğrenmek için ekteki kaynaklara bakın.
4. **Dilimlemeyi Önizleme** Çoğu slicer'ın bir önizleme modu vardır. Bu, yazıcının parçanızı katman katman nasıl inşa ettiğini tam olarak gösterir. Bu, baskıdan önce sorunları (desteklenmeyen çıkıntılar veya ince duvarlar gibi) tespit etmek için hayati bir araçtır ve zaman ve malzemeden tasarruf sağlar.
5. **İçe Aktarmak İçin Dosya Formatları (STL, STEP)**
    1. **STL (Stereolitografi):** Bir 3D modelini bağlantılı üçgenler olarak temsil eder, bir "mesh" formatı. Heykeller, karakterler, serbest tasarım gibi çok karmaşık modeller için iyidir ve neredeyse her slicer ile çalışır. Ancak, birim bilgisi **içermez**, bu yüzden dışa aktarma ve içe aktarma sırasında birimlerin eşleştiğinden dikkatli olmalısınız. Düşük kalitede dışa aktarıldığında, delikler veya kritik boyutlar gibi şeylerin doğruluğunu etkileyen tesselasyon eserleri olabilir.
    2. **STEP:** Başka bir popüler formatdır, renk ve doku saklayabilir, temel FDM baskısı için STL'den daha az yaygındır. Binlerce küçük üçgen yerine özellik verileri ile çalışır. Birim verisi içerir, bu yüzden slicer'da dönüşüm gerekmez.

### Malzemeler (FDM için Filamentler)

Filament türü, 3D yazdırılmış parçanızın özelliklerini önemli ölçüde etkiler. Farklı filament özellikleri tablosu için eke bakın. 3D yazıcıya yeniyseniz, PLA ile başlamak en kolay olacak ve PETG, makul maliyetle güç ve dayanıklılık dengesi için harika bir sonraki adımdır.

1. **Yaygın Malzemeler**
    1. **PLA (Polilaktik Asit):** Yazdırması kolay, prototip için iyidir, düşük ısı direnci.
    2. **PETG (Polietilen Tereftalat Glikol):** Güçlü, dayanıklı, işlevsel parçalar için iyidir.
    3. **ABS (Akrilonitril Bütadien Stiren):** Güçlü, ısı dirençli, ancak yazdırmak daha zor.
2. **Gelişmiş Malzemeler**
   Bunlar yazdırmak daha zordur ve gerçekten ihtiyacınız olduğunda saklanması en iyisidir:
    1. **TPU (Esnek):** Esnek, kauçuk benzeri parçalar yapar. Farklı durometer malzeme satın almak veya parça kalınlığını/infill değiştirmek parçanın ne kadar esnek olduğunu değiştirir.
    2. **Naylon PA-6 (Poliamid):** Mühendislik sınıfı malzeme. Güç ve dayanıklılık için iyidir. Daha yüksek seviye yazıcılarla yazdırmak nispeten kolaydır.
    3. **Karbon Fiber Takviyeli Filamentler:** Yukarıdaki malzemelerin çoğuna filament karbon fiber parçaları eklenebilir. Bu, genellikle daha yüksek maliyetle artırılmış sertlik ve güç sunar.
    !!! Uyarı
        Doğranmış fiber filamentler zımparalamak, delik açmak veya handled tehlikeli olabilir, çünkü havaya veya cilde mikroskobik karbon çubuklar salabilir.

    4. **Sürekli Karbon Fiber:** Markforged'in belirli teklifleri gibi bazı 3D yazıcılar, gömülü sürekli karbon fiber ipliklerle yazdırabilir. Bu, alüminyumla eşleşen veya onu aşan parça gücü sunabilir.
    5. **PC (Polikarbonat):** Son derece güçlü, darbe dirençli ve yüksek ısı toleransı.
    6. **Daha Niş Filamentler:** PPS, PPA, ASA, Tullomer, PEEK, Ultem - Bu filamentlerin bazıları farklı kullanım durumları için faydalı olabilecek gerçekten benzersiz özelliklere sahiptir.
3. **Malzeme Saklama ve İşleme** Filamentler havadan nemi emer (higroskopik). Bu, stringing, kabarcıklanma ve hatta daha zayıf parçalar gibi baskı sorunlarına neden olabilir. Filamentleri kuru, kapalı kaplarda, ideal olarak kurutucu ile saklayın. Filament satıcısının filament kurutma talimatlarını okuyun.



