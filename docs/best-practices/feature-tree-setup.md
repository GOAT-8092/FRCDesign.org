---
title: Feature Tree En İyi Uygulamaları
description: Her mekanizma belgesindeki part studio feature ağaçları için en iyi uygulamalar.
---

# Part Studio En İyi Uygulamaları


### Part Studio'ya Ne Dahil Edilmeli

Part studio, **takımınızın üretmesi gereken tüm parçaları içermelidir**. Bu, tamamen özel plakaları, boyuna kesilmiş milleri, değiştirilmiş COTS parçalarını vb. içerebilir. Değiştirilmemiş COTS parçaları doğrudan ilgili assembly'ye içe aktarılmalıdır - part studio içinde hiçbir değişiklik gereklidir.

Ayrıca **aynı parçaları çoğaltmaktan ve tube converter gibi yoğun featurescripts'leri aşırı kullanmaktan kaçının**. Bu uygulamalar part studio yükleme sürelerinizi yüksek yapabilir ve navigasyonu ve değişiklikleri çok gecikmeli hale getirebilir. Part studio'da her parçadan sadece birini oluşturmak, assembly yaparken sadece çoğaltabileceğiniz anlamına gelirken, part studio performansınız büyük ölçüde iyileştirilecektir.

!!! İpucu
    Referans için COTS parçalarını türetmek yerine, genellikle sketchlerinize basit ölçümler ekleyebilirsiniz (türetilmiş bir dişli yerine bir pitch circle gibi); bu hem şimdi hem de genel olarak daha hızlıdır, çünkü yükleme sürelerini azaltır. Diğer alt sistemlerinizden parçaları türetebilirsiniz (örneğin çerçeveyi ve drivetrain part studio'nuzdaki basitleştirilmiş modülleri intake part studio'nuzda) ve kolay referans için onları closed composite yapabilirsiniz, ancak bunu minimumda tutun.

### Feature Tree Organizasyonu

Her part studio feature ağacı, ilgili ana layout sketch'lerden çekilen bir derive komutuyla başlamalıdır. Bu üzerine inşa edeceğiniz şeydir.

**Özellikleri, parçaları ve sekmeleri sıralayın ve adlandırın ve klasörleri kullanın** CAD'inizi robot üzerinde çalışan diğer insanlar için daha anlaşılır hale getirmek için. Onshape'in en büyük faydalarından biri işbirliği yapma yeteneğidir, ancak adsız ve sıralanmamış belgeler bu noktayı tamamen ortadan kaldırır. Gerçek zamanlı sıralama ve adlandırma ayrıca geri dönüp şeyleri değiştirmeyi (yapmanız gerekecektir) kolaylaştırabilir. Bazı takımlar organizasyonu ve assembly için yardımcı olmak için bir parça adlandırma sistemi bile kullanır.

<!-- !!! İpucu
    Parçaları manuel olarak yeniden adlandırabilir veya bunu otomatik olarak yapmak için çeşitli [featurescripts](https://www.frcdesign.org/resources/featurescripts/?h=feat#onshape) kullanabilirsiniz.  -->

İyi organize edilmiş bir part studio'nun bir örneğini burada görün:

<center><img src="/img/best-practices/organized-part-studio.webp" style="border:5px solid #ADADAD"></center>

### Akıllı Originlerin Önemi
CAD'deki diğer birçok iyi uygulama gibi, akıllı origin'ler gelecekteki senin hayatını kolaylaştırabilir. Akıllı origin'ler, tasarımcıların modellerinde sağlam simetri eksenleri ve referanslar için varsayılan geometriyi (Front/Right/Top Düzlemleri, Origin Noktası) kullanmalarına izin verir.

FRC CAD için, tüm studio'larda ve assembly'lerde ana layout sketch ile aynı origin'i kullanmanın amacı iki katlıdır:

1. Origin her zaman başvurabileceğiniz tutarlı bir merkezi nokta olacaktır. Bu ayrıca şeylerin parametrik kalmasına yardımcı olur.
2. Robot CAD ve robot yazılım origin noktasını birleştirmek için. CAD'de ve kodda aynı origin'e sahip olarak, robot sorunsuz bir şekilde [AdvantageScope](https://github.com/Mechanical-Advantage/AdvantageScope "AdvantageScope Deposu"){:target="_blank"} aktarılabilir ve kamera dönüşümleri daha kolay ölçülebilir.

!!! Not
    Tanımlar takımdan takıma değişebilir, ancak bir FRC robotunun origin'i genellikle ***drivebase'nin merkezi, zemin seviyesinde*** olarak tanımlanır.

Buna yardımcı olmanın bir yolu [Origin Cube Featurescript](https://cad.onshape.com/documents/321c197a842fc5f1a29e6621/w/fc3cdd5ca7edcd93e02f13cc/e/df3afdbec8d1356c2af15e4b?renderMode=0&uiState=6637caa6ccbcaa36badca03a "Origin Cube Featurescript Belgesi"){:target="_blank"} kullanmaktır, bu daha fazla [assembly en iyi uygulamaları sayfasında](assembly-setup.md "Assembly En İyi Uygulamaları Sayfası") açıklanmıştır. Origin cube kullanıyorsanız, origin cube'u tüm part studio'larda ilk özellik yapın.


<br>
