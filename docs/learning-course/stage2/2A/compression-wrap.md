# 2A: Basic Shooter

## Compression & Wrap

### Compression

Compression'ın amacı, enerjiyi flywheel'den oyun parçasına verimli bir şekilde aktarmaktır. Oyun parçası ne kadar yumuşak olursa, etkili enerji transferi için o kadar fazla compression'a ihtiyaç vardır. Yetersiz compression kaymaya neden olur, zayıf enerji transferine yol açarken, aşırı compression güç gereksinimlerini artırır ve verimliliği düşürür. Doğru dengeyi bulmak için prototipleme gereklidir. Sert oyun parçaları olan oyunlar için, örneğin 2017'de, compression bir foam destek kullanılarak da elde edilebilir.

### Wrap

Wrap, oyun parçasının flywheel ile temas ettiği süreyi ifade eder. Daha uzun bir wrap süresi daha tutarlı enerji transferi sağlar. Altında yatan fizik için, [Impulse (Wikipedia)](https://en.wikipedia.org/wiki/Impulse_(physics) "Impulse Wikiepdia Page"){:target="_blank"} sayfasına bakın.

???+ Video "Yeterli Compression/İletişim Zamanı Yok"
    <figure>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/5OoCSAgqm3s?si=ougTDRU_EV1QIwa3" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    </figure>
    <figcaption>Bu, yeterli compression'a sahip değilseniz nasıl görünebileceğidir. Shooter'ın atışın gerçekte ne kadar uzağa gittiğine göre ne kadar gürültülü olduğunu görün (Uyarı: Yüksek Ses / Küfür)

???+ Video "İyi İletişim Zamanı ve Compression"
    <figure>
    <iframe width="320" height="560" src="https://www.youtube.com/embed/9DEJG6eoeaQ?rel=0" frameborder="0" allowfullscreen></iframe>
    </figure>
    <figcaption>Bu, tam aynı robotla iyi iletişim süresine ve compression'a sahip olduğunuzda nasıl göründüğüdür. (Uyarı: Yüksek Ses)</figcaption>

[Stealth wheels](https://www.andymark.com/products/stealth-wheels-options "Stealth Wheel Product Page"){:target="_blank"}, Solid roller wheels, ([WCP Solid Roller Wheels](https://wcproducts.com/products/solid-roller-wheels "WCP Solid Rubber Wheel Product Page"){:target="_blank"}), ve Colson wheels sıkça seçilir çünkü compression eksiklikleri ve yumuşak yapışkan silikon yüzeyleri vardır. Bunların hepsi build season sırasında prototip yapmak için iyi seçeneklerdir.


### Referans Tasarım

Örnek tasarım 4 inç çapında roller tekerlekler kullanır. Çap, yeterli temas süresi sağlarken, paketlemek için yeterince küçüktür.


### Feeder

Oyun parçalarını flywheel'e beslemek için genellikle bir tekerlek veya kayış seti kullanılır. Tasarım oyuna ve belirli besleme stratejisine bağlıdır. Örneğin, 2020 oyununda, power cell'in yapışkan doğası nedeniyle feeder'ın her iki tarafını güçlendirmek avantajlıdır. Örnekte, oyun parçalarını shooter'a yönlendirmek için tek bir compliant wheel kullanılır.


<br>

<div class="grid cards" markdown>

-   <center><img src="\img\learning-course\stage2-shooter\2910shooter.gif" width="100%" style="border:5px solid #ADADAD; border-radius: 2%"></center>

-   <center><img src="\img\learning-course\stage2-shooter\1690shooter.gif" width="88%" style="border:5px solid #ADADAD; border-radius: 2%"></center>

</div>

<figure>
<figcaption>2910'un ve 1690'un robotuna oyun parçalarının nasıl beslendiğini gözlemleyin.</figcaption>
</figure>
<br>
