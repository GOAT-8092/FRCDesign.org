# 2A: Basic Shooter

## Spin Control


### Spin

Tek bir flywheel shooter kullanırken, küresel oyun parçaları shooter'ın bir tarafının statik doğası nedeniyle spin kazanabilir. 2022'de, aşırı spin sorunluydu çünkü oyun parçasının golden sekip çıkmasına neden oldu. Bunu ele almak için, zıt yönde dönen backrollers tanıtıldı. Bazı spinler atış stabilitesini artırabilir - örneğin 2017 gibi oyunlarda, dik bir yay trajektörü avantajlıydı - ancak 2022'de atış doğruluğunu olumsuz etkilememek için dikkatli bir şekilde yönetilmesi gerekiyordu.

<center>
<video width="600" controls>
<source src="\img\learning-course\stage2-shooter\bounceout.webm" type="video/webm">
Tarayıcınız video etiketini desteklemiyor.
</video>
<center> *Çok fazla spinden kaynaklanan sektirme. Kaynak: FRC Takımı 7492* </center>
</center>

### Back Rollers

Sürtünmeyi azaltmak, topu döndürmek için kaybedilen enerjiyi en aza indirerek atışa daha fazla enerji transfer etmeye yardımcı olur. Bu, hood üzerinde düşük sürtünmeli malzemeler kullanarak veya back rollers dahil ederek başarılabilir, bu da sürtünmeyi daha da azaltır ve atış verimliliğini artırır.

<figure><center>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/1b8spBWIAT4?si=daEZUNFTRv_rsYMn" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    <figcaption> Bu yüksek hızlı shooter videosu, hood desteği üzerindeki sürtünmeyi azaltmak için PTFE bant kullanır ve bu da bazı spinleri azaltır. Bu, çıkış hızını saatte 2 mil artırdı. </figcaption>
</center></figure>


Back rollers topa enerji transferini üç ana yolla artırır:

1. Oyun parçasına verilen spin miktarını azaltır, daha fazla enerjiyi ileri harekete dönüştürür ve atış hızını artırır.
2. Her iki tarafın da güçlendirilmesini sağlayarak sürüklemeyi azaltır, daha fazla compression ve daha etkili enerji transferi sağlar.
3. Temas noktalarını artırarak, oyun parçasına genel enerji transferini iyileştirir.

Back rollers shooter'a zıt yönde dönmelidir. Bu, back roller'lara ek motor(lar) ekleyerek veya dişliler ve kayışlar kullanarak ana flywheel'i back roller'lara bağlayarak başarılabilir. İki tarafı mekanik olarak birleştirmek yazılım kontrolünü basitleştirebilir. Back roller'ların hızını değiştirerek, oyun parçasına verilen spin miktarını kontrol edebilirsiniz.

<figure>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/QZKDnRvLhrA?si=9ZoKnbHI4jayoux0&amp;start=5" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    <figcaption>Topun shooter yolu boyunca seyahat ederken nasıl döndüğünü gözlemleyin. Back rollers varlığına rağmen, bazı spin hala belirgindir. </figcaption>
</figure>

<br>
