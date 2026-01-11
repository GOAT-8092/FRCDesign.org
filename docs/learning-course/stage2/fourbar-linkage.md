---
search:
  exclude: true
---

# 2x: Four-bar Linkage

Work In Progress

## Tasarım Teorisi

### Linkage'lar nedir / neden kullanırsınız

Four bar linkages, 2E'de tanıtılan slapdown dağıtım yöntemine bir alternatiftir {#TODO link}. Dikkatli bir şekilde tasarlanmış linkage'lar, alan kısıtlı tasarımlar veya intake roller'ları için zorunlu pozisyonları olan tasarımlar için daha fazla tasarım esnekliği sağlar. Layout eskizi ayarlayarak, ana intake plakanın son pozisyonları istendiği gibi çevrilebilir ve döndürülebilir. Slapdown intake sadece intake'ı döndürür, bu yüzden intake her zaman pivot noktasının üzerinde dikey olarak depolanır. Four-bar intake, intake'ı daha sıkı paketleyebilir, çünkü büyük bir intake'ı depolandığında robotun altına daha yakın çevirebilir.

### Pnömatik vs Motor Aktüasyon

Motorlar, her mekanizma için en yaklaşılabilir aktüasyon yöntemidir. Four bar intakelar, pnömatik silindirlerin kullanıldığı en yaygın yerlerden biridir ve bazı durumsal faydalar sunabilir. Pnömatik silindirler, karmaşıklığı tasarladığınız mekanizmanın mekanik tasarımından robotun elektronik alanına taşıyabilir. Bir tasarımda pnömatik kullanmaya karar vermeden önce, pnömatik sistem bileşenlerinin ağırlığını ve hacmini robotunuzun başka bir alanına yüklediğini aklınızda tutun.

### Linkage mekanik avantajı

TODO: mekanik avantaj için grafikler (merkezden kaçınma)

### Four Bar Linkage Oluşturma
Bu adım adım kılavuz, 9" foam topu intake etmek için bir four bar linkage oluşturmayı gösterir. Bir pnömatik silindir ile aktüe edilir.


<details>
  <summary>Nick Aarestad'dan Alternatif Video Eğitimi</summary>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/QsAC_seQHJY?si=apjY7oN6o2JKj5xE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</details>




<p>Four Bar Kılavuzu:</p>
<p>Adım 1.<br>
    Önce oyun parçasının intake'ten geçmesini istediğiniz akışı anlamalısınız (yeşil ok). Bumper geometrisini, oyun parçasının başlangıç pozisyonunu (ön bumper'a değiyor) ve oyun parçasının bitiş pozisyonunu çizin. Ayrıca oyun parçasının yolu boyunca birkaç ara pozisyonunu çizin.
    <center><img src="\img\learning-course\stage2-fourbar\step 1 reqs.webp" width="60%"></center>

Adım 2a (sol).<br>
Sonra intake roller'larınızın genişletilmiş ve geri çekilmiş pozisyonunu tanımlayın (sol resim). Roller'lar oyun parçasıyla teması ve istenen compression'ı korumalıdır. Bu durumda roller'lar bumper'lerden 7" uzaklıkta ve öndeki roller 7" yerden yüksek olacak şekilde boyutlandırılmıştır. Intake'ın geri çekilmiş durumu robotun çerçeve çevresi içinde olmalı ve mümkün olduğunca az yer kaplamalıdır.<br>

Ana intake plakası intake roller'larını tutar ve ayrıca four bar linkage linklerinin intake plakasına bağlanacağı montaj noktalarını tutar. Soldaki resimde linkage montaj noktaları üçgenlerle tanımlanır. Bu montaj noktaları, genişletilmiş ve geri çekilmiş durumlar arasında her bir yapı çizgisi üzerinde eşit kısıtlamalar kullanılarak aynı olduklarından emin olmak için kullanılır.<br>

Adım 2b (sağ).<br>

Intake roller'larının pozisyonları genellikle tam olarak tanımlanır, ancak diğer noktalar işlevsel bir linkage tasarlamak için gerektiği gibi hareket ettirilmelidir. Intake plakasındaki linkage montaj noktalarını ve şasiye linkage montaj noktalarını makul bir geometri elde edilene kadar elle hareket ettirin. Ardından, sağ resimde olduğu gibi, linkage'yi tam olarak tanımlamak için boyutları kullanın. Şasiye montaj noktaları boyutlandırılmalı ve bazı noktalar geometrik kısıtlamalar sonucunda tam olarak tanımlanacaktır.
<center><img src="\img\learning-course\stage2-fourbar\step 2a partial sketch.webp" width="45%">  <img src="\img\learning-course\stage2-fourbar\step 2b full sketch.webp" width="45%"></center>
Tam Olarak Tanımlanmış Layout Eskizi:<br>
<center><img src="\img\learning-course\stage2-fourbar\step 3 layout sketch.webp" width="60%"></center>
Adım 4. (sadece pnömatik ise)<br>
Bu örnekte, intake'ı içeri ve dışarı aktüe etmek için bir pnömatik silindir kullanılacaktır. Daha uzun düz çizgi silindirin genişletilmiş uzunluğudur ve daha kısa yapı çizgisi silindirin geri çekilmiş uzunluğudur. Bu linkage'yi düzenlemenin birçok başka yolu vardır, bunlar arasında üst kol yerine alt kol üzerine hareket edenler veya intake genişletildiğinde silindirin geri çekilmesine neden olanlar. Silindirin bağlanacağı link üzerindeki noktayı (5.5" boyutu) linkage'nin hem genişletilmiş hem de geri çekilmiş durumlarında tanımlayın. Linkage'nin arka montaj noktası tam olarak tanımlanacak ve linkage düzeni tamamlanmış olacaktır.
<center><img src="\img\learning-course\stage2-fourbar\step 3 pneumatic sketch.webp" width="60%"></center>
Adım 5. <br>
Şimdi uygun parametrik CAD uygulamasını kullanarak, intake ve linkage için plakaları eskizleyin ve extrude etmeye hazırsınız. Bunlar assembly'de gerçek olacakları yerde olmalıdır, part studio'nun merkez çizgisinde değil. Link'ler arasında sıfır çarpışma veya mükemmel uyum sağlamak için gelişkin eskizleme teknikleri kullanılabilir. İlk tasarımınız için bunu denemeyin. Bunun yerine, basit şekiller oluşturun, ardından assembly'de çarpışmaları kontrol edin ve her iki seyahat ucunda da çarpışma olmayana kadar plakaları gerektiği gibi ayarlayın. Bu plakalar diğer robotlarla ve saha ile ciddi çarpışmalar yapacaktır, her deliğin etrafında önemli marjlar (>0.5") ile 1/4" polikarbonat önerilir.
<center><img src="\img\learning-course\stage2-fourbar\step 5 extrude plates.webp" width="60%"></center>
Adım 6. <br>
Four bar linkages monte etmek oldukça karmaşık olabilir ve daha az hareketli subassembly'li daha basit bir assembly kadar temiz olmayacaktır. Bu söylenmişken, intake'ınızı monte ederken düzgün origin cube assembly pratiklerini kullandığınızdan emin olun. Bu resim tam monte edilmiş intake plakalarını ve ayrıca pnömatik silindiri gösterir. Açıklık için intake roller'ları gibi bazı diğer donanımları içerir, ancak iyi bir tasarım örneği olarak alınmamalıdır. Four bar layout eskizlerini assembly'ye ekleyin ve intake'ın beklediğiniz gibi tam olarak hareket ettiğinden emin olun. Resim, pnömatik silindirin tamamen geri çekildiği intake'ın geri çekilmiş durumunu gösterir ve plakalar layout eskiz ile mükemmel eşleşir. Bu durum böyle değilse, sorunu takip etmeli ve düzeltmelisiniz.
<center><img src="\img\learning-course\stage2-fourbar\step 6 assembly.webp" width="60%"></center>
[onshape link](https://cad.onshape.com/documents/9aeba443b3990c61c52d9613/w/fe0631a64edb24356a3dbe20/e/673191a338fd6c4480e9d624?renderMode=0&uiState=663e8f226d078f47b184758e)


<br>

<script>
var coll = document.getElementsByClassName("collapsible");
var i;

for (i = 0; i < coll.length; i++) {
  coll[i].addEventListener("click", function() {
    this.classList.toggle("active");
    var content = this.nextElementSibling;
    if (content.style.maxHeight){
      content.style.maxHeight = null;
    } else {
      content.style.maxHeight = content.scrollHeight + "px";
    }
  });
}
</script>
