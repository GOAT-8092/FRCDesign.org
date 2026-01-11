# 1B: Güç Aktarımı

## Miller ve Rulmanlar
### Miller
Miller bir eksen boyunca döner güç ileterek, FRC'de en yaygın olan altı köşeli millerdir. Genellikle 1/2" ve 3/8" çaplarında (düzden düze ölçülür) olan bu altıgen miller bazen "yuvarlatılmış altıgen" veya "Thunderhex" olarak bilinen yuvarlatılmış köşelere sahip olabilir.

### Rulmanlar
Rulmanlar millerin plakalardan bağımsız dönmesine ve/veya şeylerin millerden bağımsız dönmesine izin verir. Standart altıgen miller 1/2" altıgen rulmanlar kullanır, yuvarlatılmış altıgen miller ise daha kolay montaj için yuvarlak rulmanlar kullanabilir.

<figure>
    <img src="../images/examples/bearing-and-shaft.webp" style="width:75%">
    <figcaption>1/2" yuvarlatılmış altıgen rulman (Sol) ve 1/2" yuvarlatılmış altıgen mil (Sağ) (Görsel Kaynak: WCP)</figcaption>
</figure>
### Örnek

!!! Example "Rulmanda Dönen Bir Mil Örneği"
    <figure>
        <img src="../images/examples/shaft-spinning.gif" style="width:100%">
        <figcaption>Rulmanlarda dönen bir mil</figcaption>
    </figure>

### Burçlar
Burçlar, rulmanların ucuz ve düşük sürtünmeli bir alternatifidir ve esas olarak yer tasarrufu sağlamak için omzu cıvatalar, altıgen miller ve yuvarlak boru gibi metal millerle kullanılır. Bronz veya asetal/delrin gibi kendinden yağlanan bir malzemeden yapılırlar ve genellikle pivotlar ve bağlantı mafsalları gibi nispeten düşük RPM'li uygulamalarda kullanılırlar.

<figure>
    <img src="../images/examples/bushing.webp" style="width:50%">
    <figcaption>Bir Bronz Burç (Görsel Kaynak: WCP)</figcaption>
</figure>


### Modelleme
Milleri modellemenin en kolay ve en parametrik yolu, aşağıdaki alıştırmalarda nasıl kullanacağınızı öğreneceğiniz [`Robot Shaft` Featurescript](https://cad.onshape.com/documents/9cffa92db8b62219498f89af/w/06b332ccabc9d2e0aa0abf88/e/2e6e4b559832eeff8391e933 "Robot Shaft Featurescript Onshape Document"){:target="_blank"} özelliğini kullanmaktır.

Rulmanlar için, istediğiniz rulmanı FRCDesignLib'den ekleyin.

<br>
