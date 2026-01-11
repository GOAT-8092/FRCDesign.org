# Mekanizma Örneklerine Katkıda Bulunma

[Mekanizma örnekleri](../mechanism-examples/index.md "Mekanizma Örnekleri Sayfası"){:target="\_blank"} sayfaları, dış katkıdan en çok fayda sağlayacak sayfalardır. Elbette diğer takımlardan örnekler ekleyebilirsiniz, ancak kendi mekanizmanızı eklemek ve tasarım ve performans hakkında arkasından gitmek ideal olacaktır. Başka bir takımdan bir örnek ekliyorsanız, onların girdilerini ve daha doğru bilgi almak için onlarla röportaj yapmaya çalışın.

**Mekanizma Örnekleri için Kriterler:**

- Bir yarışmada gerçekten inşa edilmiş ve kullanılmış olmalıdır
- Hem iyi hem de kötü parçaları göstermelidir. Ne için tasarlandı? Neden belirli kararlar verildi? İnşa etmek ve üretmek ne kadar kolaydı? Gerçekte nasıl performans gösterdi? Yeniden tasarlanırsa ne iyi gider ve ne değiştirilebilir?
- Tasarımın belirli parçaları hakkında detaylı bilgi verin, kullanılan malzemeler ve parçalar ve nedenleri, belirli mekanizmalar veya süreçler vb.
- CAD ve/veya gerçek robotun detaylı resimleri. Tercihen Onshape'de yapılan veya yüklenen halka açık CAD.
- Müsaitse ve uygulanırsa ekstra medya ve bağlantılar.

## Mekanizma Örnekleri Ekleme

[katkıda bulunma yöntemlerinde](methodsOfContributing.md "Katkı Kılavuzu Sayfası") açıklandığı gibi, iki yöntem vardır:

1. Ayrı bir platformda (örneğin Google Docs) katkıyı yazmak ve bir iç katkıda bulunanın web sitesine eklemesini sağlamak
2. GitHub'da fork yapmak ve bir pull request yapmak

İlk yöntem oldukça açıklayıcıdır, ancak GitHub'da fork yapmayı ve bir pull request yapmayı seçerseniz, bazı biçimlendirmeler gereklidir. GitHub'da ve VS Code'da çalışmaya başlamak için [katkıda bulunma yöntemleri](methodsOfContributing.md "Katkı Kılavuzu Sayfası") sayfasındaki katkı kılavuzunu izleyin.

## Bir Mekanizma Kategorisi Ekleme (İSTEĞE BAĞLI)

Bir mekanizma kategorisi eklemeniz gerekiyorsa, kategorideki mekanizma örnekleri için bir açılış sayfası ve [mekanizma örnekleri açılış sayfasına](../mechanism-examples/index.md "Mekanizma Örneği Dizin Sayfası") bir grid kartı eklemelisiniz.

### Klasörleri ve Dosyaları Ekleme

1. Yeni mekanizma kategorisinin adıyla `mechanism-examples` altında yeni bir klasör oluşturun. Tüm mekanizma örnek sayfaları ve kategorinin açılış sayfası bu klasörde olacaktır.

   !!! Not
   Mekanizmanın birden fazla türü varsa (örneğin asansörler ve intakeler gibi), oradaki açılış sayfalarıyla her biri ayrı klasörde birden fazla klasör oluşturabilirsiniz. Örneğin, `elevator` klasörü `cascade` ve `continuous` klasörlerini içerir, her ikisi de bir `index.md` açılış sayfası içerir.

2. Yeni kategorinin kök klasöründe `.meta.yml` adında yeni bir dosya oluşturun ve içine aşağıdaki kodu kopyalayın:

   ```yml
   social:
     cards_layout_dir: layouts
     cards_layout: mechanism_fundamentals_wide
   ```

   Bu, tüm kategori için sosyal kart için kullanacağınız resmin boyutunu ayarlar. `cards_layout` seçeneği için `mechanism_fundamentals_wide` veya `mechanism_fundamentals_tall` arasında seçim yapabilirsiniz.

   Resimler 1:1.545 veya 1.545:1 olmalıdır, herhangi bir boyut. Daha fazla bilgi [burada](mechanismContribution.md#adding-an-image-for-the-example "Resimleri ekleme bölümü") sağlanır.

3. Kategorinin açılış sayfalarını oluşturun, `index.md` adında. Her klasörde sadece bir tanesini yapabilirsiniz.

   Kategori açılış sayfası için bu şablonu kopyalayın ve bilgilerinizle doldurun:

   ```md
   ---
   title: sayfa-başlığı
   image: link-to-social-card-image
   ---

   # sayfa-başlığı

   açıklama

   <div class="grid cards" markdown>

   - <center markdown>[![](link-to-mechanism-image)](link-to-page)</center>

     ***

     description-about-unique-aspects-of-example

     [:octicons-arrow-right-24: page title](link-to-page)

   </div>

   <br>
   ```

   Drivebase örnekleri açılış sayfası için kod şöyledir:

   ```
   ---
   title: Drivebase Örnekleri
   image: docs/img/mechanism-examples/drivebase/swerve/2910_2023_dt.webp
   ---


   # Swerve Drivebases
   Drivebase, robotunuzun en önemli parçasıdır, her diğer alt sistem için bir yatak sağlar. Farklı drivebase'lerin örnekleri, elektronik düzeni, bellypan şekilleri ve montaj için yapısal cross üyeler için ilham sağlayabilir, bunların hepsi robot tasarlamanın zor ama kritik bir parçasıdır, çünkü erişilebilirlik ve bakım sağlanmalıdır, alt sistemler robotun üstüne yerleştirilirken.

   <div class="grid cards" markdown>

   -   <center markdown>[![](../../img/mechanism-examples/drivebase/swerve/2910_2023_dt.webp)](2910_2023_dt.md)</center>
   -   <center markdown>[![](../../img/mechanism-examples/drivebase/swerve/2910_2023_dt.webp)](2910_2023_dt.md)</center>

       ---

       Radyo ve breaker için erişilebilir kılan özel bir plaka, tellerin cross üyelerden geçmesine izin veren delikler ve grommets

       [:octicons-arrow-right-24: 2910 Charged Up Drivebase](2910_2023_dt.md)
       [:octicons-arrow-right-24: 2910 Charged Up Drivebase](2910_2023_dt.md)

   -   <center markdown>[![](../../img/mechanism-examples/drivebase/swerve/972_2024_dt.webp)](972_2024_dt.md)</center>
   -   <center markdown>[![](../../img/mechanism-examples/drivebase/swerve/972_2024_dt.webp)](972_2024_dt.md)</center>

       ---

       Merkezi 2x2 cross üye, bir brainpan ve narenciye bumper monteleme plakaları.

       [:octicons-arrow-right-24: 972 Brainpan Drivebase](972_2024_dt.md)
       [:octicons-arrow-right-24: 972 Brainpan Drivebase](972_2024_dt.md)

   </div>

   <br>
   ```

### Mekanizma Örnekleri Açılış Sayfasına Bir Grid Kartı Ekleme

Tüm grid kartları `<div class="grid cards" markdown>` div içindedir. Daha fazla bilgi için [mkdocs-material grid kartlar hakkında dokümlara](https://squidfunk.github.io/mkdocs-material/reference/grids/#using-card-grids "MKdocs Kart Dokümantasyonu"){:target="\_blank"} bakın.

Aşağıdaki kodu div içine yapıştırın ve tüm şablon bilgilerini kendi bilgilerinizle değiştirin.

```md
- <center markdown>[![](link-to-image)](link-to-category-page)</center>

  ***

  Örnek Açıklama

  [:octicons-arrow-right-24: category-name](link-to-category-page)
```

!!! Not
Her kart arasında kodda bir satır sonu bırakın, aksi takdirde kart içeriği birleşir.

Drivebase örnekleri grid kartı için kod şöyledir:

```md
- <center markdown>[![](../img/mechanism-examples/drivebase/swerve/2910_2023_dt.webp)](drivebase/swerve/index.md)</center>
- <center markdown>[![](../img/mechanism-examples/drivebase/swerve/2910_2023_dt.webp)](drivebase/swerve/index.md)</center>
  ***

  Swerve drivebase'ler elektronik düzen örnekleriyle

  [:octicons-arrow-right-24: Swerve Drivebases](drivebase/swerve/index.md)
  [:octicons-arrow-right-24: Swerve Drivebases](drivebase/swerve/index.md)
```

## Bir Mekanizma Örnek Sayfası Ekleme

Halihazırda var olan bir kategoriye bir mekanizma örnek sayfası eklemek için yapılması gereken birkaç şey vardır. Sayfa oluşturulmalı, kategori açılış sayfasında bir grid kartı oluşturulmalı ve örnek için standart bir resim oluşturulmalıdır.

### Sayfayı Oluşturma

Örneğiniz için kategori klasöründe yeni bir `.md` dosyası oluşturun.

İçine aşağıdaki şablonu kopyalayın ve Markdown biçimlendirmesini kullanarak bilgileri doldurun:

```
---
image: link-to-social-card-image
---

# mekanizma-örnek-adı

<figure markdown="span">
    [![alt-text](link-to-image){height=80% width=80%}](link-to-cad){target = "_blank"}
<figcaption>caption</figcaption>
</figure>

### Links
[CAD Link](link){target = "_blank"}

## Behind the Design

<br>
```

Aşağıda içerik yazılmamış 2910 Charged Up Drivebase sayfasının bir örneği vardır:

```
---
image: docs\img\mechanism-examples\drivebase\2910_2023_dt.webp
image: docs\img\mechanism-examples\drivebase\2910_2023_dt.webp
---

# 2910 Charged Up Drivebase

<figure markdown="span">
[![2910 Charged up Drivebase](../../img/mechanism-examples/drivebase/swerve/2910_2023_dt.webp){height=80% width=80%}](https://cad.onshape.com/documents/28a885d3b8ad7de567efebbd/w/33b7dd39d54ec1ab15f2e2aa/e/d78c591638c349b708e238e6){target = "_blank"}
[![2910 Charged up Drivebase](../../img/mechanism-examples/drivebase/swerve/2910_2023_dt.webp){height=80% width=80%}](https://cad.onshape.com/documents/28a885d3b8ad7de567efebbd/w/33b7dd39d54ec1ab15f2e2aa/e/d78c591638c349b708e238e6){target = "_blank"}
<figcaption>Swerve drivetrain featuring MK4I swerve modules, a pocketed bellypan, and a billet brass frame-rail for weight distribution.</figcaption>
</figure>

### Links
[CAD Link](https://cad.onshape.com/documents/28a885d3b8ad7de567efebbd/w/33b7dd39d54ec1ab15f2e2aa/e/d78c591638c349b708e238e6){target = "_blank"}

## Behind the Design

<br>
```

Sayfanız için kullandığınız resimleri `/docs/img/mechanism-examples/[category]/[example]/` ekleyin.

### Örnek İçin Bir Resim Ekleme

Kategorinin .meta.yml'sini varsayılan kart düzeni (uzun veya geniş) için kontrol edin. Bu, mekanizma örneği için kullanacağınız 1:1.545 resminin yönü olacaktır.

1:1.545, Onshape'in "baskı" işlevini kullanarak "tabloid" kağıt boyutu ile çıkarılan bir resmin en boy oranıdır. Oradan geniş veya uzun için manzara veya portre seçebilirsiniz.

!!! İpucu
Zaten sahip olduğunuz resimler için, GIMP ve bir hesap makinesi kullanarak bir resmi istenen en boy oranına getirmek için piksel ekleyerek kırpmak için kullanabilirsiniz.

## Site Gezintisine Sayfaları Ekleme

Eklenen tüm yeni sayfalar site gezintisine eklenmelidir.

Gerekirse daha fazla sayfa, kategori ve açılış sayfası eklemek için `mkdocs.yml dosyasında` sunulan standart biçimlendirmeyi izleyin:

```yml title="mkdocs.yml"
- Mechanism Examples:
    - mechanism-examples/index.md
    - Drivebases:
        - Swerve:
            - mechanism-examples/drivebase/swerve/index.md
            - 2910's Charged Up Drivebase: mechanism-examples/drivebase/swerve/2910_2023_dt.md
            - 1678's Crescendo Drivebase: mechanism-examples/drivebase/swerve/1678_2024_dt.md
            - 3005's Charged Up Drivebase: mechanism-examples/drivebase/swerve/3005_2023_dt.md
            - 6328's Crescendo Drivebase: mechanism-examples/drivebase/swerve/6328_2024_dt.md
            - 5460's Crescendo Drivebase: mechanism-examples/drivebase/swerve/5460_2023_dt.md
            - 972's Crescendo Drivebase: mechanism-examples/drivebase/swerve/972_2024_dt.md
        - Tank:
            - mechanism-examples/drivebase/tank/index.md
    - Intakes:
        - Pivoting Intakes:
            - mechanism-examples/intake/slapdown/index.md
            - 1678's Crescendo Intake: mechanism-examples/intake/slapdown/1678_2024_intake.md
            - 1778's Crescendo Intake: mechanism-examples/intake/slapdown/1778_2024_intake.md
            - 6423's Crescendo Intake: mechanism-examples/intake/slapdown/6423_2024_intake.md
            - 3847's Rapid React Intake: mechanism-examples/intake/slapdown/3847_2022_intake.md
            - 2910's IR @ Home Intake: mechanism-examples/intake/slapdown/2910_2021_intake.md
        - Linkage Intakes:
            - mechanism-examples/intake/linkage/index.md
            - 1678's Rapid React Intake: mechanism-examples/intake/linkage/1678_2022_intake.md
            - 6800's Rapid React Intake: mechanism-examples/intake/linkage/6800_2022_intake.md
            - 4089's Rapid React Intake: mechanism-examples/intake/linkage/4089_2022_intake.md
    - Game Piece Manipulation:
        - Shooters:
            - mechanism-examples/shooter/index.md
            - 1678's Rapid React Shooter: mechanism-examples/shooter/1678_2022_shooter.md
            - 6328's Crescendo Shooter: mechanism-examples/shooter/6328_2024_shooter.md
            - 2910's Rapid React Shooter: mechanism-examples/shooter/2910_2022_shooter.md
            - 6800's Rapid React Shooter: mechanism-examples/shooter/6800_2022_shooter.md
            - 2910's IR @ Home Shooter: mechanism-examples/shooter/2910_2021_shooter.md
        - Indexers:
            - mechanism-examples/indexer/index.md
        - End Effectors:
            - mechanism-examples/end-effector/index.md
    - Linear Extensions:
        - Continuous Elevators:
            - mechanism-examples/elevator/continuous/index.md
            - 1678's Charged Up Elevator: mechanism-examples/elevator/continuous/cable.md
            - 3847's Charged Up Elevator: mechanism-examples/elevator/continuous/belt.md
        - Cascade Elevators:
            - mechanism-examples/elevator/cascade/index.md
            - WCP Greyt COTS Elevator: mechanism-examples/elevator/cascade/wcp_greyt_elevator.md
            - 2 Stage Cascade Elevator: mechanism-examples/elevator/cascade/2_stage_elevator.md
            - 3 Stage Cascade Elevator: mechanism-examples/elevator/cascade/3_stage_elevator.md
        - Telescopes:
            - mechanism-examples/telescope/index.md
    - Rotating Mechanisms:
        - Pivots:
            - mechanism-examples/pivots/index.md
            - 6328 A-Frame Pivot: mechanism-examples/pivots/6328_2023_pivot.md
            - 2910 Dead Axle Pivot: mechanism-examples/pivots/2910_2023_pivot.md
            - 1690 Lantern Gear Pivot: mechanism-examples/pivots/1690_2024_pivot.md
            - 5460 Dead Axle Pivot: mechanism-examples/pivots/5460_2023_pivot.md
        - Turrets:
            - mechanism-examples/turret/index.md
```

Görebileceğiniz gibi, biçimlendirme şöyledir:

```yml
- Mechanism Examples:
    - mechanism-examples/index.md
    - Category 1:
        - link-to-category-landing-page
        - Mechanism 1: link-to-mech-1-page
        - Mechanism 2: link-to-mech-2-page
```

Katınız için teşekkürler!

<br>
