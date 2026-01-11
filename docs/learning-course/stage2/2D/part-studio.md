# 2D: Kaskat Asansör

## Part Studio
1. `Origin Cube` özelliğini ekleyin ve bunları ayrı bir part studio'da yaptıysanız ana layout eskizlerini türetin.
2. Boruları oluşturmak için extrude individual kullanın (sadece kopyalar oluşturmayın; bu, bir taraftaki sadece aşamaların altlarını anlamına gelir).
3. Ekstrüzyonları borulara dönüştürün.

    ??? Tip "Ekstrüzyonları Borulara Dönüştürme"
        Boru dönüştürücü bunu yapmanın en kolay yoludur, daha önce gösterildiği gibi, ancak delik deseni şeyleri bozabilir ve asansörün boyutları değişirse oldukça kolay hizalanamaz. En parametrik yol boruları manuel olarak shelling, ardından delik deseni oluşturmak için karışık bir eskiz ve lineer desenler kullanmaktır. Bu şekilde, delik desenine tasarım amacı ekleyebilirsiniz, böylece boyutlar değiştiğinde hizalanmaz.

        Parametrik delik desenleri oluşturmak için, borunun uzunluğunu ölçmek için CADSHARP'dan [**Measure Value**](https://cad.onshape.com/documents/77baa8153589a7fc5f289829/w/cffd0f2a7077380d5378a885/e/d3174bf5315e6aafcb889367?renderMode=0&uiState=652ee7d25129162fc0afad5f "Measure Value Featurescript Onshape Document"){:target="_blank"} featurescript'ini kullanmaya başlayabilirsiniz. İlk deliğinizin borunun üstünde oluşturun, ardından borunun uzunluğu boyunca 0.5" mesafede ve instance count'u `((#frame_side_tube/inch)*2)-1` olarak ayarlanmış bir özellik deseni veya eskiz deseni oluşturun. Bu yöntem delik sayısını borunun uzunluğuna parametrik tutar.

4. Yapıyı tamamlamak için boruları dönüştürün ve kopyalayın.

    !!! Tip
        Bu noktada, tasarım lideri olarak, mate connectors, subassembly'ler ve en üst seviye assembly oluşturabilir ve asansörü diğer insanlara verebilir ve iş akışını paralel hale getirebilirsiniz.

5. Benzersiz crushblock'ları modelleyin

    !!! Info
        Crushblock'lar ve boru tıpası günümüzde çoğu superstructure ve asansör için yaygın olarak kullanılır. Bunların ne olduğunu ve neden yararlı olduklarını [yapı hakkında tasarım el kitabı sayfasında](../../../design-handbook/structure/structure.md "Structure Handbook Page"){:target="_blank"} bulun.

    <figure markdown="span">
        <img src="/img/learning-course/stage2-elevator/tubesAndCrushblocks.webp" style="width:75%">
        <figcaption> Tamamlanmış asansör boruları </figcaption>
    </figure>

1. Rigging (halat) nerede istediğinize karar verin ve onu bir yol, profil ve sweep ile modelleyin.
2. Birinci aşama borusunda yerinde olmak için [TTB zincir tarasını](https://www.thethriftybot.com/products/elevator-25h-chain-drive-kit "TTB Chain Comb Product Page"){:target="_blank"} türetin. Bu, zinciri borulardan ne kadar uzaklaştıracağınızı bilmak içindir.
3. Zincir transmisyonunu ve çapraz üyeyi, sprocket'ler için rulman delikleri dahil olmak üzere eskizleyin.
4. Çapraz üye için plakaları ve boruyu oluşturun. Rigging için kelepçe çapraz üyeye monte edilecek, ancak aynı zamanda taban aşamasının rijitliği için de vardır.
5. Çapraz üyede yerinde olmak için [TTB kablo kelepçesini](https://www.thethriftybot.com/products/elevator-dyneema-pulley-kit "TTB Cable Clamp Product Page"){:target="_blank"} türetin ve onun için montaj deliklerini oluşturun, ve boruya tamamen cıvatalıyorsanız bir crushblock oluşturun.
6. Çapraz üyedeki boru tapaları için delikler ekleyin.
7. Zinciri, herhangi bir özel spacer ve mili dahil olmak üzere zincir transmisyonunu oluşturun
8. Dişli kutusunu oluşturmak için bazı maxplanetary parçalarını türetin. Her iki maxplanetary için spacer'lar ve montaj oluşturun. Kolayca erişilebilir ve değiştirilebilir olduklarından emin olun
9. MAXplanetary millerini desteklemek için asansörün altına plakalar ekleyin.
10. İsteğe bağlı olarak, carriage için cıvata şeritlerini ve bir ratchet plakasını türetin ve rigging'in bağlanacağı mili oluşturun.
11. Taban borusunun ortasında, origin cube tarafından sahip olunan bir referans mate oluşturun, daha sonra subassembly'leri birbirine mate etmek için kullanılacak.

<figure markdown="span">
    <img src="/img/learning-course/stage2-elevator/elevatorPartStudio.webp" style="width:75%">
    <figcaption> Tamamlanmış asansör part studio </figcaption>
</figure>

<br>
