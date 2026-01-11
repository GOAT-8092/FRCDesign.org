# 1A: Onshape Temelleri - Bölüm 1
## Egzersiz 5: Bir Kutu Süperyapısı Oluşturma
### Giriş

Bir sürücü sisteminin üstüne ekstra montaj için daha fazla alt bölüm parçası, örneğin bir shooter veya bir kol, kutu borusundan yapılmış çerçeveler eklenebilir.

<figure style="margin-bottom: 2rem;">
  <img src="/img/learning-course/stage1a/exercise-5-973-example.webp" style="width:60%; border:5px solid #ADADAD">
  <figcaption>973'ün 2022 Süperyapısı</figcaption>
</figure>


Bu egzersizde, daha önce oluşturduğunuz sürücü sistemine basit bir kutu borusu çerçevesi ekleyeceğiz.

<figure>
  <img src="/img/learning-course/stage1a/exercise5-frame.webp" style="width:80%">
  <figcaption>Final Kutu Boru Çerçevesi</figcaption>
</figure>

---

### Layout Sketch ve Sürücü Sistemi

1. Bunu düzgün bir şekilde planlamak için, bir yan layout sketch oluşturmalıyız (önceden Egzersiz 5'te kullanılan).
2. [Gerekli kurs araçlarında](../../course-setup/required-course-tools/featurescripts.md){:target="_blank"} eklediğiniz **origin cube feature script'ini** ekleyerek başlayın. `Alt + C` kullanarak şeyleri arayabileceğinizi unutmayın!
3. Yeni bir sketch oluşturun, `right plane`'i seçin ve bu sketch'i kopyalamaya başlayın. Onu mükemmel bir şekilde kopyalamak için ihtiyacınız olan constraint'leri kendiniz çözin.


    <figure>
      <img src="/img/learning-course/stage1a/exercise5-frame-sketch.webp" style="width:100%">
      <figcaption>Kutu süperyapı sketch'i</figcaption>
    </figure>

    !!! Info "Origin Yerleşimi"
        Tekerlekler borunun köşelerindeki 1.75 inçlik bloklardır. Bu durumda, yan layout sketch'de origin nereye yerleştirilmiştir? Sizce oraya neden yerleştirilmiştir? Gerçek hayatta robotu yandan hayal edin.

4. Yan layout sketch bittikten sonra, son egzersizden hatırladıklarınıza göre part studio'nuzda swerve sürücü sistemi çerçevesini oluşturun. (Mate connector'ı seçmeyi unutmayın!)

    !!! Tip
        Zorlanırsanız, denedikten sonra önceki videoya bakın

    !!! Info "Tasarım Niyeti"
        Bu sürücü sistemini bir kare yapalım. Gereksiz dimension kullanmaktan kaçınmak için üst sketch'inize nasıl yaklaşacağınız? Sadece swerve boşluğunuzu, çapraz borularınız arasındaki mesafeyi (8 inç) ve boru ofsetinizi tanımlamanız gerekir.

    ??? Hint
        Hangi uzunluk zaten tanımlanmış/kısıtlanmış? Equal constraint'ı kullanabilir misiniz?



### Çerçeveyi Modelleme
Şimdiye kadar, sketch'ler varsayılan düzlemlerde ve mate connector'larda oluşturuldu. Çapraz boruların üstündeki çerçeve için kutu borusunu modellemek için, boruları oluşturacak sketch'in çapraz borunun yüzünde oluşturulmalıdır, çünkü borunun orada olmasını istiyorsunuz, çapraz boru pozisyonunu değiştirse bile.

!!! Tip "Tasarım Niyeti"
    Buna "tasarım niyeti" ile modelleme denir. Bir şeyi modellemenin birçok farklı yolu vardır, ancak bir parçanın veya genel tasarımın niyetine göre belirli yolları seçebilirsiniz. Bu ayrıca yaratıcı bloklardan kaçınmanıza ve tasarım değiştiğinde CAD'inizin hata oluşturmasını engellemeye yardımcı olabilir.

<figure>
  <img src="/img/learning-course/stage1a/side profile.webp" style="width:80%">
  <figcaption>Kutu süperyapı sketch'i</figcaption>
</figure>

Bu sketch tekniğinin bir demosunu aşağıda izleyin.
<figure>
  <iframe width="768" height="432" src="https://www.youtube.com/embed/_b2Gf8IiEEA?controls=1&rel=0&showinfo=0&vq=hd1080" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</figure>

Şimdi bir demosunu gördüğünüze göre, çapraz borunun yüzünde bir sketch oluşturarak ve layout sketch'ten `use` aracını kullanarak yeni sketch'e çizgileri yansıtarak **kutu borusu yapısını tamamlamayı deneyin**.

### Gereksinimler
- Kutu çerçevesi, sketch'te ve extrude'da toplam 0 yeni dimension kullanılarak yapılmalıdır
- Tube converter'ı 1/16" kalınlığında duvarlar kullanacak şekilde düzenleyin ve "centered on tube" seçeneğini "auto offset" olarak değiştirin

!!! Warning "Boru Ofsetleri"
    Sürücü sistemleri ve tipik kullanım için borunun kenarı ile delik arasındaki mesafe farklıdır. Düzenli kutu borularınız için "centered on tube" kullanırsanız delik yerleşiminiz doğru olmayacaktır. Sadece sürücü sistemi raylarınız için "Centered on tube" kullanın!

---

### Bitirme

Bitirdiğinizde, **5 dakikalık bir mola verin**.

Geri döndüğünüzde, **bulduğunuz hataları iyileştirmeyi veya düzeltmeyi deneyin**. Bitirdiğinizde, iş akışınızı çözümle karşılaştırın. **Farklı bir şey yapmanıza ne gibi bir düşünce süreci neden oldu?**


<center markdown>[Çözüm Belgesi](https://cad.onshape.com/documents/5f1057b0e7579ff9dd5811fe/w/4c6a1a1d9747b8ea76b238a3/e/b89eed09a1d075135ee83667){.md-button .md-button--primary target="_blank"}</center>

Özelliklerinizi nasıl yeniden adlandıracağınızı öğrenmek için aşağıdaki kısa videoyu takip edin, ardından part studio'nuzdaki sketch'leri ve özellikleri yeniden adlandırın. İleriye doğru, **her zaman sketch'lerimizi ve özelliklerimizi adlandırmak istiyoruz**.

<figure>
  <iframe width="768" height="432" src="https://www.youtube.com/embed/ELdwPyFnm4Y?controls=1&rel=0&showinfo=0&vq=hd1080" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</figure>

<br>

Özelliklerinizi yeniden adlandırmayı bitirdikten sonra, bir sonraki egzersize geçin.

<br>
