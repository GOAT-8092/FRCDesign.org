# 1D: Tasarım Metodolojisi - Basit Swerve Şasisi

## Üsten Aşağı Tasarım Metodolojisi

CAD'de bir model tasarlarken, kullanılabilecek iki üst düzey strateji vardır: üsten aşağı ve aşağıdan yukarıya. Üsten aşağı tasarım, tasarımı dikte etmek için üst düzey, düşük detaylı sketchler kullanır ve ardından detayları ve bileşenleri bu çerçeve içinde iyileştirir. Buna karşılık, aşağıdan yukarıya tasarım, bireysel bileşenleri veya parçaları ayrı ayrı oluşturmayı ve ardından nihai ürünü oluşturmak için bunları birleştirmeyi içerir.

Üsten aşağı tasarım, daha iyi sistem entegrasyonu, tutarlılık ve daha parametrik olma sağlayan bütüncül bir yaklaşım sunar. Aşağıdan yukarıya tasarım, bireysel parçaları tasarlarda esneklik ve bağımsızlık sunar. FRC robot tasarımında, sistem entegrasyonu genellikle en zorlayıcı aspect olduğu için üsten aşağı yaklaşım tercih edilir. Üsten aşağı, robot mimarisinin parça tasarımını dikte etmesini sağlar.

### Ana Düzen Çizimi

Bunu başarmak için, ***ana düzen çizimi*** kullanılır. Bazen bunlara "master" sketchler de denir. Ana düzen çizimi, her mekanizmanın ana boyutlarını, saha öğesi etkileşimlerini ve robot boyut kısıtlamalarını yakalayan bir dizi sketchtir. Ardından, ana düzen sketch(leri) her mekanizmanın part studio'una eklenir ve bireysel bileşenler daha sonra içe aktarılan düzen çizimi etrafında modellenir. Düzen çizimleri hakkında daha fazla bilgi [Layout Sketch Best Practices](../../../best-practices/mastersketch-setup.md "Layout Sketch Best Practices Page"){:target="_blank"} sayfasında bulunabilir.

???+ Example "Örnek Ana Düzen Çizimi"
    <figure>
    <img src="../images/example-master-sketch.webp" style="width:60%">
    <figcaption>Robot ana düzen çizimlerine örnek. Her mekanizmanın önemli detayları yakalayan bir dizi düzen çizimi vardır. (Fotoğraf Kaynağı: FRC 3647)</figcaption>
    </figure>


### Origin Yerleşimi ve Origin Cube

Düzen çizimi üsten aşağı tasarımını tam olarak kullanmak için, tüm part studio'lar için birleştirilmiş bir origin seçmeliyiz. Tüm part studio'lar ve montajlar için ana düzen çizimi ile aynı origin'i kullanmanın iki amacı vardır:

1. Origin her zaman referans verebileceğiniz tutarlı bir merkez nokta olacaktır. Bu da işlerin parametrik kalmasına yardımcı olur.
2. Robot CAD'ini ve robot yazılımı origin noktasını birleştirmek için. CAD ve kodda aynı origin'e sahip olarak, robot sorunsuz bir şekilde [AdvantageScope](https://github.com/Mechanical-Advantage/AdvantageScope "AdvantageScope Repository"){:target="_blank"}'a aktarılabilir ve kamera dönüşümleri daha kolay ölçülebilir.

!!! Note
    Tanımlar takımdan takıma değişebilse de, bir FRC robotunun origini genellikle ***şasinin merkezi, zemin seviyesinde*** olarak tanımlanır.

Bunu başarmak için, 1C boyunca kullandığınız [`Origin Cube` Featurescript](https://cad.onshape.com/documents/321c197a842fc5f1a29e6621/w/fc3cdd5ca7edcd93e02f13cc/e/df3afdbec8d1356c2af15e4b?renderMode=0&uiState=6637caa6ccbcaa36badca03a "Origin Cube Featurescript Document"){:target="_blank"}'ini kullanırız. Bu, origin'de şeffaf 2" bir küp üretir ve önceki aşamada zaten kullanılan birçok kullanışlı sabit ve fonksiyon sağlar.

Origin Cube, montaj mating için daha sonra çok yararlı olacak, ancak şimdilik hatırlamanız gereken tek şey **Origin Cube'un tüm part studio'lardaki ilk özellik olmalıdır**. Origin Cube hakkında daha fazla bilgiyi [assembly best practices page](../../../best-practices/assembly-setup.md "Assembly Best Practices Page"){:target="_blank"} sayfasından okuyabilirsiniz.

<br>
