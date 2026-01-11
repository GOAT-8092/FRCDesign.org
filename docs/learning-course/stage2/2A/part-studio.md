# 2A: Basic Shooter

<center markdown>[Shooter Reference Document](https://cad.onshape.com/documents/8f093edaad44b5702e92ddd9/w/fefbb7a7af099fc237c1513a/e/ad76a30633d5b293d92d8217 "Shooter Reference Onshape Document"){:target="_blank" .md-button .md-button--primary }</center>

## Part Studio

!!! Tip
    Rollback barını kullanarak referans shooter part studio'yu sürecin her adımında görüntüleyebilirsiniz.

### Yapı

1. Shooter plakalarının monte edeceği referans drivetrain çapraz borularını modelleyin ve bunları kapalı bir kompozit parça yapın. Bunlar topun plakalar arasında seyahat etmesi için alan bırakacak şekilde 8 inç aralıkta olacaklar.
2. Ana plakanızı çapraz raylerin içine modelleyin, önce montaj donanım deliklerini eskizleyin, feeder tekerleklerini büyük top yolu daire çevresini takip eden eğilmiş polikarbonu tutan standoffs'ları dahil ederek, sonra güç aktarımını (motorlar, kayış merkezden merkeze çizgileri, diş step circles), ve son olarak plaka ana hatlarını eskizleyin. Büyük bir dişli kutusu eskizlemeye benzer, değil mi? Diğer parçalar için parametrik referans için extrude edin ve ayna olduğundan emin olun.
3. Shooter'ın önünü drivetrain'e monte etmek için kullanılan ek 1x1 boruyu modelleyin. Bu, yüksek hızlarda olası flywheel titreşimlerine rağmen rijit kalmasına yardımcı olur.

### Güç Aktarımı

4. `Belt & Chain Gen` ve `Shaft Generator` featurescript'lerini kullanarak güç aktarım bileşenlerini modelleyin.
5. Çoğu kasnak MKCAD'nin yapılandırılabilir HTD kasnak parçası kullanılarak assembly'e eklenecektir (hepsi 3D yazdırılabilir), ancak feeder tekerlekleri için Kraken x60 pinion kasnağı bir SplineXS 3D-yazdırılmış parça adaptörü kullanacaktır. MKCAD'yi kullanarak taban kasnağı part studio'ya derive edin ve [bu dokümandan](https://cad.onshape.com/documents/1b85e3f2d6e09d4be8bb81ba/v/531d064ba727d665df487f4a/e/e64fbaae49bd0a01559aa66c?renderMode=0&uiState=668f43004852b8565ff6390e "SplineXS 3D Print Adapter"){:target="_blank"} SplineXS 3dp adaptörünü derive edin. Kasnakta adaptör ile bir boolean subtract işlemi gerçekleştirin, kesimi oluşturmak için, adaptör parçasını tutmak için keep tools kontrol edin. Ana plakada doğru yerlere dönüştürüldüklerinden emin olun.

### Bitirme Adımları
6. Delgelerle bağlamak için delikleri olan polikarbon desteğini modelleyin.
7. Limelight 3 için 3D-yazdırılmış kamera montajını ve kamera montaj spacer'lerini modelleyin

<figure>
    <img src="/img/learning-course/stage2-shooter/Shooter Part Studio.webp" width="50%">
    <figcaption>Tamamlanmış Part Studio</figcaption>
</figure>

<br>
