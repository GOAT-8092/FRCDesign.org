# 2C: Slapdown Intake

## Assembly

Dead axle pivot gibi, bu alt sistem de statik bir parça ve hareketli bir parça içerir. Yine, bunları rijit (hareketsiz) assembly'lere ayırmak, sonra en üst seviyede birleştirmek istiyoruz.

### Base Assembly

Statik parçalar için bir assembly oluşturun, part studio'dan parçaları ve origin cube'ü yeşil işaret ile ekleyin ve bunları bir grup haline getirin. Origin cube'ü orijine sabitleyin. Part studio'dan kalan parçaları, MKCAD'den ve standart içerikten ekleyin, mümkün olduğunda replicate ve patterns kullanın.

<figure>
    <img src="/img/learning-course/stage2-slapdown/staticAssembly.webp" width="70%">
    <figcaption>Tamamlanmış Statik Assembly</figcaption>
</figure>

### Arm Assembly

Intake kolları için bir assembly oluşturun ve assembly'yi tamamlamak ve rijit hale getirmek için yukarıdakiyle aynı şeyi yapın. Rollerlar için, bunları [Configurable Rollers Document](https://cad.onshape.com/documents/b75886a5660c38eee7d50e47/w/58faeca16d5b2008a9485b5c/e/6274f59b451ed6222cd7523d "Configurable Rollers Onshape Document"){:target="_blank"} 'tan ekleyin.

<figure>
    <img src="/img/learning-course/stage2-slapdown/intakeArms.webp" width="70%">
    <figcaption>Tamamlanmış Intake Kolları Assembly</figcaption>
</figure>

### Top Level Assembly

Şimdi en üst seviye bir assembly oluşturun ve statik assembly'yi (orijine sabitleyin) ve intake arm assembly'yi ekleyin. Her iki assembly'deki origin cube'lardan gelen mate connectors arasında bir revolute mate oluşturun ve ona bir limit ekleyin. Bu slapdown intake assembly'yi tamamlar.

<figure>
    <img src="/img/learning-course/stage2-slapdown/intakeTopLevel.webp" width="70%">
    <figcaption>Tamamlanmış Top Level Intake Assembly</figcaption>
</figure>

<br>
