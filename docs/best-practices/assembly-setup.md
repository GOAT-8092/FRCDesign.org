---
title: Assembly En İyi Uygulamaları
description: Parçaları assembly'lere eklemek ve organize etmek için en iyi uygulamalar.
---

# Assembly En İyi Uygulamaları

Parçalarınızı zaten adlandırdığınızı ve belgenin geri kalanında işinizi organize ettiğinizi varsayarsak, düzgün organize edilmiş bir assembly oluşturmak çok basittir.

### Origin Cube
`Origin Cube` Featurescript'i, part studio'nun origin'ine 2 inç şeffaf bir küp ekler. Küpün origin'inde bir mate connector vardır. Bu parça asla değişmeyeceği ve her zaman part studio'nun origin'inde kalacağı için, onu kullanarak parçaları origin'e gruplandırmak ve fasten etmek, başka bir parçaya sabitlenmiş veya eklenmiş bir mate connector kullanmaktan her zaman daha **sağlam ve parametriktir**, çünkü bu parça değişebilir veya silinebilir.

<center markdown>[Origin Cube Featurescript](https://cad.onshape.com/documents/321c197a842fc5f1a29e6621/w/fc3cdd5ca7edcd93e02f13cc/e/df3afdbec8d1356c2af15e4b?renderMode=0&uiState=6637caa6ccbcaa36badca03a "Origin Cube Featurescript Onshape Belgesi"){:target="_blank" .md-button .md-button--primary}</center>

<br>


<figure>
<img src="\img\best-practices\originCubeFeature.webp" width="60%">
<figcaption>Origin Cube özelliğini ekleme</figcaption>
</figure>

!!! İpucu
    Origin cube, cıvata deliği boyutları, heat set insert deliği boyutları vb gibi kullanışlı sabitler ve işlevleri içe aktarma seçeneğine sahiptir.

### Parçaları Ekleme Süreci

[Alt Belge Kurulumunda](sub-document-setup.md#subsystems-with-multiple-degrees-of-freedom "Alt Belge Kurulumu Sayfası") açıklandığı gibi, hiçbir serbestlik derecesine sahip olmayan alt sistemlerin sadece bir assembly'si olacak, birden fazla hareketli parçası olan alt sistemler ise birden fazla rijit assembly'ye ayrılacaktır. Parçaları ekleme ve assembly'leri bitirme süreci her iki durum için de benzerdir.

1. Part studio'nuzda origin cube'u oluşturun
2. İlgili parçaları ve origin cube'u rijit bir alt assembly için yeni bir assembly belgesine ekleyin
3. Tüm parçalarda "grup" aracını kullanın
4. Origin mate connector'ünü origin'e fasten edin
5. Yinelenen parçaları çoğaltın ve fasten edin
6. Standart donanım ve COTS bileşenlerini ekleyin
7. Örnekleri klasörlere sıralayın (örneğin borular, swerve modülleri, spacerler)

!!! İpucu
    Part studio'ya daha fazla parça ekledikçe, bunları yeşil onay işaretiyle assembly'ye tek tek ekleyebilir, ilk gruba çift tıklayabilir ve parçayı mating'ten kaçınmak için gruba ekleyebilirsiniz. Bu, yeni parçanın her zaman part studio'da tasarlandığı yerde kalacağı anlamına gelir.

Alt sistemin birden fazla hareketli parçası varsa (örneğin over-the-bumper intake veya asansör), her serbestlik derecesi için ana layout sketch üzerinde bir mate connector oluşturun. Bu bir pivot noktası veya slider mate'in başlangıç noktası olabilir (asansör durumunda). Her mate connector'ü origin cube'a ait yapın.

Geçerli ise, diğer tüm rijit alt assembly'ler için 2-7 adımlarını tekrarlayın. Bu, her alt assembly'nin rijit olmasına, origin cube'un origin'e fasten edilmesine ve tüm parçaların part studio'dakiyle aynı yerde olmasına neden olacaktır. Her alt assembly ayrıca origin cube'a ait olan mate connector'leri içerecektir.

Şimdi üst düzey bir alt sistem assembly'si oluşturun ve her alt assembly'yi içine ekleyin. Statik alt assembly'nin origin cube'unu origin'e fasten edin ve diğer mate connector'leri kullanarak diğer alt assembly'leri birbirine mate edin.

??? Örnek "Aşama 2C - Slapdown Intake"
    Aşama 2C Slapdown Intake, statik bir bölümü ve dönen bir bölümü olan bir alt sistemdir. Pivot için ekstra bir mate connector eklenir, ana layout sketch üzerinde, origin cube'a ait

    <center markdown>[Aşama 2C - Slapdown Intake](https://cad.onshape.com/documents/17302d787e092ce11015f7ee/w/f7cf5c02c7655f0328a3a74a/e/f1456325e0175c4c081008c2 "Aşama 2C Slapdown Intake Onshape Belgesi"){:target="_blank" .md-button .md-button--primary}</center>

    <center><img src="/img/best-practices/slapdown-intake-example/slapdown-intake-mate-connector.webp" style="border:5px solid #ADADAD"></center>

    Bu mate connector her iki alt assembly'de de vardır.
    <center><img src="/img/best-practices/slapdown-intake-example/slapdown-intake-static-connectors.webp" style="border:5px solid #ADADAD"></center>

    <center><img src="/img/best-practices/slapdown-intake-example/slapdown-intake-arm-connectors.webp" style="border:5px solid #ADADAD"></center>

    Statik assembly origin'e fasten edilir ve kol assembly, origin cube'un her iki örneğine ait pivot mate connector'ini kullanarak döner.
    <center><img src="/img/best-practices/slapdown-intake-example/slapdown-intake-top-level.webp" style="border:5px solid #ADADAD"></center>


??? Örnek "Aşama 2D - Cascade Asansör"
    Aşama 2D Cascade Asansör, statik bir bölümü ve lineer olarak kayan iki alt assembly'yi olan bir alt sistemdir. Bu bir part studio, statik bir çerçeve/dişli kutusu assembly'si, ilk aşama ve carriage için assembly'ler ve slider mate'lerle 3 alt assembly'yi birleştiren üst düzey bir assembly içerir.

    <center markdown>[Aşama 2D - Cascade Asansör](https://cad.onshape.com/documents/da5aef9e6bf6e869f4a51a45/w/5a0f4a3426876db0ba214277/e/f8fd8133abcb12800eacb5d1 "Aşama 2D - Cascade Asansör Onshape Belgesi"){:target="_blank" .md-button .md-button--primary}</center>

    <center><img src="/img/best-practices/elevatorAssembly.webp" style="border:5px solid #ADADAD"></center>


??? Örnek "3647 Millennium Falcons 2024 Intake"
    <center><img src="/img/best-practices/0200-A.webp"><figcaption>Üst Düzey Assembly: 0200-A-Intake. Sadece iki mate olduğunu unutmayın. Döner, ilgili origin cube'lere ekli olan iki intake pivot mate connector arasındadır.</figcaption></center>

    <center><img src="/img/best-practices/0210-A.webp"><figcaption>Stationer Bileşenler Assembly: 0210-A-Intake Base. Bileşenler group mated ve origin cube origin'e fasten edilmiştir.</figcaption></center>

    <center><img src="/img/best-practices/0210-PS.webp"><figcaption>Stationer Bileşenler PS: 0210-A-Intake Base. Turuncu ana layout sketch'ten türetilmiş intake pivot mate connector'yi unutmayın. </figcaption></center>

    <center><img src="/img/best-practices/0220-A.webp"><figcaption>Hareketli Bileşenler Assembly: 0220-A-Intake Arm. Bileşenler group mated ve origin cube origin'e fasten edilmiştir.</figcaption></center>

    <center><img src="/img/best-practices/0220-PS.webp"><figcaption>Hareketli Bileşenler PS: 0220-Intake Arm. Turuncu ana layout sketch'ten türetilmiş intake pivot mate connector'yi unutmayın.</figcaption></center>


### Basitleştirilmiş Modeller

Assembly'nizde primitifleri en aza indirdiğinizden emin olun. Primitifler, bir nesnenin ne kadar karmaşık olduğunu ve Onshape'in ne kadar zor render edeceğini ölçen bir ölçüdür. Ne kadar çok primitif varsa, assembly'niz o kadar gecikmeli olacaktır.

Mümkün olan her yerde [FRCDesignLib](../../course-setup/required-course-tools/part-library.md "FRCDesignApp Ekleme Öğretici Sayfası"){:target="_blank"} basitleştirilmiş modüllerini kullanarak primitifleri en aza indirin: elektronik, swerve modülleri, motorlar vb.

??? Video "Primitifleri En Aza İndir"
    <video controls="true" allowfullscreen="true" poster="/img/best-practices/minimizePrimitives.webp">
      <source src="/img/best-practices/minimizePrimitives.webm" type="video/webm">
    </video>

### Diğer Küçük Şeyler

- FRCDesignLib'den COTS parçalarını içe aktarın
- Donanım eklemek için **replicate aracını** kullanın!
- Kullandığınız mate sayısını en aza indirin; bu çözme süresini düşürür
- Klasörlerle organize kalın

İyi organize edilmiş bir assembly'yi burada görün:

<center><img src="/img/best-practices/assembly.webp"></center>

<br>
