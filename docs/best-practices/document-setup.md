---
title: Belge Kurulumu
description: FRC robotu için belge kurulumu için en iyi uygulamalar.
---

# Belge Kurulumu

Genel olarak, bir FRC robotu tek bir belge içinde tamamen oluşturulmak için çok karmaşıktır ve çok fazla parçaya sahiptir. Bunu yapmak mümkündür, ancak kötü yükleme sürelerine ve muhtemelen zayıf organizasyona neden olacaktır.

Bu zorlukları hafifletmek için, genellikle FRC robotlarını birkaç belgeye ayırırız, her biri bireysel bir sürüm numarasıyla:

- Ana layout sketch'i içeren bir "Kavram" belgesi. Bu, Crayon CAD (robotunuz archetype'inin basit bir modeli) ile birlikte, robot için genel mimariyi ve geometriyi belirler.
- Her alt sistem için part studio'ları, alt assembly'leri ve üst düzey assembly'yi içeren birkaç "Alt Sistem" belgesi, örneğin bir Intake.
- Üst düzey tam robot assembly'sini içeren bir "Ana Robot" belgesi. Bu assembly, her alt sistem belgesinin üst düzey assembly'sinden oluşur.

Bu belgeleri birbirine bağlamak için birkaç temel Onshape özelliğini kullanırız:

- **Derive** özelliği: Ana layout sketch'i kavram belgesinden alt sistem belgesine getirir, böylece onun üzerinde parçalarınızı tasarlayabilirsiniz.
- **Import**: Alt assembly'ler her alt sistem belgesinden içe aktarılır, böylece ana robot belgesinde assembly edilebilirler.

Tam dosya yapısını gösteren bir diyagram aşağıdadır:

<center><img src="/img/best-practices/docsetup2.webp"></center>

<center> *Mavi: Derive, Kırmızı: Import* </center>

!!! Not
    Bazen "ana robot" belgesi "kavram" belgesi ile birleştirilir. Bu durumda hiçbir şey gerçekten değişmez, dosya yapısı sadece bir tür döngü haline gelir ve bir belge daha az vardır.

Bu belge yapısının bir örneğini burada görebilirsiniz. Çerçeve ve ana belgelerin birleşimini unutmayın.

<center><img src="/img/best-practices/docsetup3.webp" style="border:5px solid #ADADAD"></center>

<center><img src="/img/best-practices/docsetup4.webp" style="border:5px solid #ADADAD"></center>

Belge yapısı taşa oyulmuş değildir; takımınızın üstten aşağı tasarım hedefini yerine getirmesine yardımcı olduğu ve mekanizmaların sürümlerini ayırmak için ayrı belgeler kullandığı sürece, ana layout sketch'lerinizi istediğiniz yere koyabilirsiniz (ana belge, kavram belgesi veya drivetrain belgesi).

<br>
