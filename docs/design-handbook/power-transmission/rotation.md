# Döner Hareket Aktarımı

Döner güç aktarım bileşenleri rehberi. Dişliler, kayışlar ve zincir içerir.

**Çok Yakında**

<br>

<!-- <style>

td, th , table{
   border: none!important;
}

td{
  text-align: left !important;
  vertical-align: middle !important;
}

table tr:hover{
    background-color: transparent !important;
}

</style>

<p style="font-size:1rem;">Kayışlar</p>

- Kayışlar hafiftir ve yüksek hızlı mekanizmaları çok iyi sürer.
- FRC'de, en yaygın kayış tipi HTD5'tir ve GT2 ikinci en yaygın olanıdır.

<figure markdown="span">
![Kayış](../../img/design-handbook/belt.png){height=50% width=50%}
</figure>
<figcaption> GT2 ve HTD5 arasındaki fark diş profildir, çünkü GT2 diş profili dişlerin birbirinden 3mm aralıklı olduğu, HTD5 dişleri ise birbirinden 5mm aralıklıdır.
</figcaption>
Kayış tasarlerken, ReCalc'in [belt-calculator](https://www.reca.lc/belts) gibi bir hesap makinesi kullanarak doğru kayış merkezden merkeze mesafesini bulmanız gerekir, aksi takdirde kayışlarınız çok gergin olabilir veya çok fazla gevşek olabilir.


<p style="font-size:1rem;">Zincir</p>
- Zincirler ağır hizmette kullanılır ve yüksek torku idare eder, ancak kayışların aksine gerilmeleri gerekir.
- 3 Ana Tip:
    - 25:
        - 25 zinciri nispeten hafif olsa da, 35 veya 25h zincirinden çok daha az dayanıklıdır, bu da bir pivot üzerindeki şok yükleri düşünürken bir endişe kaynağıdır.
    - 25H:
        - 25H Zinciri, sertleştirilmiş #25 anlamına gelir, bu da zincir üzerindeki plakaların daha kalın olduğu anlamına gelir. Bu, tüm 25 zincir donanımı ile uyumlu kalmadan 25 zincirinden biraz daha güçlü olduğu anlamına gelir.
    - 35:
        - 35 Zincir en güçlü zincirdir ve bunu kırmak biraz zordur. En iyi kullanım durumu ağır pivotlardır.
<figure markdown="span">
![zincir](../../img/design-handbook/chain.png){height=50% width=50%}
</figure>

<p style="font-size:1rem;">Backlash Nedir:</p>
- Backlash, dişlilerin veya dişlerin dişleri arasında bir boşluk olduğunda, bu da onların tamamen tam olarak gerçekleşmeden önce hafifçe hareket etmelerine izin verir. Bu, hareket sırasında bir gecikme ile sonuçlanır ve konumlandırma hataları tanıtır, sistemlerinizin tekrarlanabilirliğini etkiler ve sistemin yanıt süresi biraz daha yavaş olduğu için son derece sorunludur.

- Backlash'i nasıl ortadan kaldırırsınız:
    - Sisteminizdeki backlash'i en aza indirmek için, zincirlerinizin düzgün şekilde gerildiğinden emin olmanız veya son redüksiyon olarak bir kayış kurulumu kullanmanız gerekir. Şanzımanları monte ettiğinizde [shim tape](https://www.mcmaster.com/products/shims/shim-tape-6/) uygulayın. FRC'de, hex millerinin hepsi tam olarak aynı boyutta değildir ve bu dişli ve mil arasinda gevşekliğe neden olur ve şanzımanlarda bu gevşeklik birikir. 4414'ün tüm konum kontrolü alt sistemlerini şimlemesinin yolu, gerçek dişlinin genişliğinin yaklaşık 1.5 katı şeritler kesmek ve ardından milin toleransına bağlı olarak bandı 1-2 yüzeysel uygulamaktır.
<p style="font-size:1rem;">Zincir Nasıl Gerilir:</p>

  - Turnbuckle:
      - Turnbuckle, iki bağlantıya bağlamak için kullanılan bir cihazdır ve zinciri bir arada germek için zinciri germek için kullanılır.
<figure markdown="span">
![turnbuckle](../../img/design-handbook/turnbuckle.png){height=50% width=50%}
</figure>

  - Idler Sistemi:
      - İdlerler, proper zincir germe olduğunu sağlamak için bir yöntemdir ve temel olarak zinciri içeri veya dışarı iterek gevşeklik miktarını azaltır.

<figure markdown="span">
![idler](../../img/design-handbook/idler.png){height=50% width=50%}
</figure>


<p style="font-size:1rem;">Dişliler:</p>
- Hareket ve güç aktarabilen dişli tekerlekler. Yönleri tersine çevirmek, şanzımanlar oluşturmak ve çok daha fazla uygulama için yaygın olarak kullanılır.

- Dişli Türleri:
    - Spur Gears:
        - 3 ana tip 10 DP, 20 DP, 32 DP'dir.
        - 10 DP:
        - Dişli çubuk ve taretleri sürmek için kullanılır
      - 20 DP:
        - Geniş dişli çeşitliliği nedeniyle şanzımanlarda çok kullanılır.
      - 32 DP:
        - Daha küçük boyutu nedeniyle daha küçük alanlarda kullanılır.
<figure markdown="span">
![32DP](../../img/design-handbook/32DP.png){height=50% width=50%}
</figure>
  - Herringbone
    - Ayrıca çift helisel dişli olarak bilinir, dişler bir V şekli oluşturur ve yüksek tork aktarırken pürüzsüz ve sessiz çalışma sağlamak için kullanılır. Yüzey alanını ve dişler arasındaki teması artırarak buna oldukça yüksek bir yük koyabilirsiniz. Bu dişliler genellikle 3 boyutlu yazdırılır.

||||
|:-:|:-:|:-:|
|<figure>![125 Herringbone Pivot](../../img/design-handbook/125pivot.webp){height=100% width=100%}</figure>|<figure markdown="span">![Herringbone](../../img/design-handbook/herringbone.png){height=50% width=50%}</figure>|


  - Bevel Gears
    - Bevel dişlileri COTS Max90 Şanzıman ile popüler hale getirilmiştir ve paralel olmayan miller arasında hareket aktarmak için harikadır. Yüksek bir yükü idare edemezler ve esas olarak paketleme için kullanılırlar.
<figure markdown="span">
![Bevel](../../img/design-handbook/bevel.png){height=50% width=50%}
</figure>
<p style="font-size:1rem;">Rack and Pinion:</p>
- Rack and pinion, daha büyük bir dişlinin daha küçük bir dişli tarafından sürüldüğü bir sistemdir ve 2022'de 1678 gibi kaputlu shooter'lar için çok kullanılır. Daha yüksek bir kontrol derecesi elde edersiniz, ancak bu sistem büyük bir yükü idare edemez.

<figure markdown="span">
  ![GIF Örneği](../../img/design-handbook/rackPinion.gif)
</figure>



<p style="font-size:1rem;">Vinç:</p>
  - Vinç, halat veya kabloları sarmak veya germek için kullanılan mekanik bir cihazdır ve tipik olarak halatın sarıldığı bir davul veya makara ve davulu döndürmek için kullanılan bir kol veya motor içerir ve geleneksel olarak teleskopik kollarda ve diğer tırmanıcılarda kullanılır.
<figure markdown="span">
![vinç](../../img/design-handbook/winch.png){height=75% width=75%}
</figure>

<p style="font-size:1rem;">Lineer Aktüatör:</p>
  - Lineer aktüatörler hassas doğrusal hareket için iyidir. Bir vida mil kullanarak döner hareketi doğrusal harekete dönüştürerek çalışırlar ve çok yüksek bir kontrol ve hassasiyet derecesi elde edersiniz.
<figure markdown="span">
![vinç](../../img/design-handbook/linearAct.png){height=75% width=75%}
</figure>

<br> -->
