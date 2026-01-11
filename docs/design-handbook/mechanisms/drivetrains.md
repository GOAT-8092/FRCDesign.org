# Sürücü Sistemi Temelleri

Sürücü sistemi tasarımı rehberi.

**Çok Yakında**

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

# Sürücü Sistemi Temelleri


## Sürücü Sistemi Türleri

- Swerve - Tüm sürücü tekerleklerinin bağımsız olarak sürüldüğü ve yönlendirildiği 4 tekerlekli bir sürücü sistemi. Sürücü sistemi herhangi bir yönde hareket edebilir
<figure markdown="span">
![swerve](../../img/design-handbook/swerve.png){height=50% width=50%}
</figure>
- Kit of Part sürücü sistemi - Kit of parts ile gelen ve bükülmüş sac metalden yapılmış 6 tekerlek drop center (orta tekerlekler dış tekerleklerden daha alçak) sürücü tabanı.
<figure markdown="span">
![KOP](../../img/design-handbook/KOP.png){height=50% width=50%}
</figure>
- West Coast Drive (WCD) - Drop-center tekerlekli bir altı tekerlek sürücü tabanı, şanzımandan doğrudan sürülür. Geleneksel olarak, güç aktarımı zincir, bir şanzıman ve rijitlik için kutu profili ile sürülür. West coast sürücüleri için temel bir özellik, tekerleklerin kantilever olmasıdır.
<figure markdown="span">
![WCD](../../img/design-handbook/nickwcd.webp){height=50% width=50%}
</figure>

## Ana Sürücü Sistemi Seçimleri

<p style="font-size:1rem;">Rijitlik</p>

Tek bir FRC oyununda, robotlar çarpışmalardan büyük kuvvetlerle karşılaşır ve rijit bir çerçeve herhangi bir yapısal hasar riskini azaltmaya yardımcı olur. Sürücü sisteminizde, bir çapraz ray gibi rijitliği artıracak bir şey eklemek istersiniz. Bir süper yapı inşa ederken, aşağıdan yukarıya düşünmeniz gerekir ve bu, sürücü sisteminizin mümkün olduğunca rijit olmasıyla başlar.

<p style="font-size:1rem;">Çapraz üyeler yapınız için ne yapar?</p>
- Popüler inancın aksine, metal insanların düşündüğü kadar güçlü ve stabil değildir ve bracing üzerindeki sıkıştırıcı yükler gelmeye başladığında "paralelogram" yapmayı sever.

<figure markdown="span">
![parallel](../../img/design-handbook/parallel.png){height=150% width=150%}<figcaption> Bu resimde, kare çerçevenin sol tarafa bir yük geldiğinde paralelgrama dönüştüğünü görebilirsiniz. Tek bir FRC maçında, şasiniz çok sayıda kuvvete maruz kalır ve bu sürücü sisteminizin şeklini etkileyebilir. </figcaption>
</figure>

<p style="font-size:1rem;">Çapraz rayları nereye yerleştirmelisiniz?</p>

- Takımların yaptığı iki ana çapraz üye türü vardır:
    - İlk tür, swerve modüllerine mümkün olduğunca yakın iki dikey çapraz üyedir.
    <figure markdown="span">
    ![twoCross](../../img/design-handbook/twoCross.png){height=50% width=50%}
    </figure>
    - Artıları:
        - Şeyleri monte etmek daha kolay
        - Sert yapı, sürücü sisteminizi etkileyen sıkıştırıcı yüklerin daha az değişme şansı.
    - Eksileri:
        - Elektronik panellerinizin erişilebilirliğini ciddi şekilde sınırlar ve elektroniklerinizin yerleşimini etkiler.

    - İkinci tür, tek bir 2x2 Yatay Çapraz kiriştir.
    <figure markdown="span">
    ![citrusCirc](../../img/design-handbook/citrusCirc.png){height=50% width=50%}
    </figure>
    - Artıları:
        - Çok fazla elektronik panel alanı açar
        - Oraya tek bir 2x1 koymaktan daha güçlüdür, çünkü kesitsel alanınız nedeniyle ve yield veya başarısız olmadan önce daha yüksek yükleri idare edebilir.
        - Eylemsizlik momenti iki katındadır, çünkü genişlik iki katıdır, yani gücünde çok daha büyük bir artış vardır.
        - 2x2 kutu profili [shear-load](https://www.youtube.com/watch?v=C-FEVzI8oe8&t=109s&ab_channel=TheEfficientEngineer) daha büyük bir alana yayılır
        - 2x2'nin sertliği daha iyidir.
    - Eksileri:
        - Süper yapınızı oradan monte etmek daha zordur, ekstrude etmeniz gerekebilir.
            - Bu, karmaşık bükülmüş metal parçalarını tanıtmanız gerektiği anlamına gelebilir
        - Sizi bir montaj tarzına kilitleyerek ciddi şekilde kilitler.
<p style="font-size:1rem;">Hangi profil kalınlığını kullanmalısınız?</p>
- Çoğu sürücü sisteminde, insanlar 1/8 kalınlığında 2x1 Kutu profili kullanır.
    - Genel olarak, duvar kalınlığı ne kadar ince olursa, yırtılmaya ve ezilmeye o kadar yatkın olur. Ağır darbelerin olduğu maçlarda, sürücü sistemi profillerinizin bükülmesini istemezsiniz:
         - 1/8" duvar kalınlığı, darbeler olacağını bildiğiniz senaryolarda veya, nasıl fikstur edildiğine veya monte edildiğine göre stres konsantrasyonunun yüksek olması gerektiği alanlarda en iyisidir.

<p style="font-size:1rem;">Bellypanler ve rijitlik üzerindeki etkileri</p>
- Belly pan, sürücü sisteminizin alt tarafında elektronikleri monte etmek için bir plakadır, ancak aynı zamanda sürücü sisteminizin rijitliğini de etkiler, çünkü her şeyi bir araya getiren dev bir gusset gibi davranır
- Sürücü sisteminin altını span ederek ve çerçeve rayları/çapraz üyeler gibi ana yapısal öğelere bağlanarak, belly pan yükünü tüm yapıya eşit olarak dağıtabilir ve entegrasyon çerçevesin herhangi bir bükülmesini veya deformasyonunu önlemeye yardımcı olur.

<p style="font-size:1rem;">Bellypan'im hangi malzemeden olmalı?</p>
 - Bellypan kalınlığını artırarak ve malzemeyi değiştirerek, robotunuzun ağırlık merkezini ciddi şekilde değiştirebilirsiniz.
- Popüler Malzeme Türleri:
    - Çelik:
        - Artıları:
            - Düşük ağırlık merkezi
            - Yüksek güç
        - Eksileri:
            - Ağır ağırlık, ağırlık limitinin altında kalmak için robotunuzun diğer parçalarını hafifletmeniz gerekebilir anlamına gelir. (254 takımının 2022'deki robotuna bakın, 1/4" Çelik Bellypan kullandılar ve diğer tüm parçalarını hafifleterek telafi ettiler)
            - İşlenmesi zor
    - Alüminyum:
        - Artıları:
            - İşlenmesi kolay
            - Nispeten yüksek güç
            - Çelikten daha hafif
        - Eksileri:
            - Alüminyum pahalıdır.
    - Polikarbonat:
        - Artıları:
            - Hafif, yani robotunuzun diğer parçalarına daha fazla ağırlık ayırabilirsiniz.
            - Nispeten uygun maliyetli
            - Çok basit işlenir.
        - Eksileri:
            - Daha düşük rijitlik ve bükülebilir
            - Daha düşük ağırlık, ağırlık merkezinizin istediğinizden daha yüksek olabileceği anlamına gelir.
- Birçok takımın rijitliği korurken ağırlığı hafifletmek için yaptığı şey pocketed bir bellypan'dır ve bu, gereksiz yerlerde malzemeyi çıkarırken, elektroniklerin doğru konumlarda tutulması için delikleri koruyarak monte edilmelerine izin verir.
<figure markdown="span">
![bPan](../../img/design-handbook/bPan.png){height=50% width=50%}
</figure>

## Çerçeve Çevresi

- Oyun kılavuzuna uygun olarak, sürücü sistemi çerçeve çevreniz maksimum 120" olmalıdır.
    - Çerçeve Uzantısı:
        - Oyun kılavuzuna uygun olarak, maçınızın başında, robotunuzun hiçbir parçası çerçeveden çıkamaz. Daha fazla temizlik elde etmek için takımlar [Swerve-Corners](https://cad.onshape.com/documents/3969471095df924bad241f81/w/42f02d1579e8bcd9c0435d48/e/b1b02258ec73e6686b1e62fd) ve 1/4" plakalar kullanır ve çerçeve çevresini her tarafta 1/2" uzatır ve bu, plakaları profilinizin kenarlarına monte etmenizi sağlar.

<figure markdown="span">
![swerveCorner](../../img/design-handbook/swerveCorner.png){height=50% width=50%}<figcaption>Vurgulanan bölümde, kutu profil uzantınızdan daha fazla sticks out görebilirsiniz.</figcaption>
</figure>

## Tekerlek Tabanı Konumu
- Daha fazla stabilite sağlamak için, özellikle dönerken tekerleklerinizi olabildiğince uzakta istersiniz.

## Elektronik Montajı
- Bir bellypan tasarlerken, elektroniklerinizin mümkün olduğunca erişilebilir olduğundan emin olmanız gerekir. Bazı takımlar çapraz profillerinde devasa erişim delikleri delerler. Bunun için aklınızda tutmanız gereken bir şey, tellerin deliğin keskin kenarlarında strip olmasını önlemek için deliklerde 3D Yazdırılmış koruma guards/kauçuk grommets yazdırmanız gerekebilir.

<figure markdown="span">
![accessHoles](../../img/design-handbook/accessHoles.png){height=50% width=50%}
</figure>

<br> -->
