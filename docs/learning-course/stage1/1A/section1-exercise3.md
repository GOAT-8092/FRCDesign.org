# 1A: Onshape Temelleri - Bölüm 1
## Egzersiz 3: Daha Fazla Extrude

Bu egzersizde, dört dikdörtgeni simetrik olarak iki inç extrude edeceksiniz — ve onları borulara dönüştüreceksiniz.
Sadece bir extrude özelliği kullanın. Ne olur?

<figure>
  <img src="/img/learning-course/stage1a/exercise3-rectangles.webp" style="width:70%">
  <figcaption>Dört dikdörtgen ile başlangıç kurulumu.</figcaption>
</figure>

Unutmayın: extrude yaptıktan sonra Tube Converter'ı kullanın.

---
***Kutuları genişletmek için tıklayın!*** ([Web sitesi özellik rehberine](../../../website-feature-guide.md) bakın)
??? question "Biraz garip görünüyor mu? Denedikten sonra burayı tıklayın."

    Talimatları takip ettiyseniz ve tek bir extrude kullandıysanız, tüm dört dikdörtgen muhtemelen tek büyük bir blokta birleşti.
    Gerçek hayatta, istemediğiniz sürece parçaların bu şekilde birleşmesini istemezsiniz.

    > Onları **ayrı ayrı** extrude ederek **ayırmayı nasıl çözebilirsiniz?**

    Yeniden başlamanız gerekiyorsa, kötü borularınızı nasıl sileceğinizi gösteren hızlı bir video:

    <iframe width="100%" height="400" src="https://www.youtube.com/embed/2Jzb1Xr6NBE?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>

---

??? success "Extrude'unuzu düzelttiyseniz burayı tıklayın."

    Manuel olarak dört extrude yapmak zahmetlidir. Daha iyi bir yol var!

    - Eski extrude'larınızı silin.

    - [Gerekli kurs araçlarında](../../course-setup/required-course-tools/featurescripts.md){:target="_blank"} eklediğiniz `Extrude Individual` Featurescript'ini kullanın.
    - (Gerekirse `Alt+C` tuşlarına basın ve "extrude individual" araması yapın.)

    Bu araç, birden fazla sketch bölgesini tek bir adımda ayrı ayrı extrude etmenizi sağlar.

    Ayrıca, Extrude Individual içindeki "Symmetric" seçeneğine tıklarsanız, simetriyi zorlayabilirsiniz.

    <figure>
      <img src="/img/learning-course/stage1a/extrude-individual.webp" style="width:90%">
      <figcaption>Extrude Individual içinde "Symmetric" kullanma.</figcaption>
    </figure>

---

## Egzersiz 3.1: Sketch Temelleri

Son egzersizde, mevcut bir sketch'i extrude ettiniz. Şimdi sıra **sketch'i kendiniz oluşturmak**.

Sketch yaparken, kutu borularını temsil etmek için 2D'de dikdörtgenler kullanırız ve her şeyi yerine kilitlemek için **dimension'ları** ve **constraint'leri** kullanırız.

Onshape'de sketch temellerini pratiğini yapmak için aşağıdaki videoyu takip edin.

<br>

<figure>
  <iframe width="768" height="432" src="https://www.youtube.com/embed/ftbpbvuZklc?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
</figure>

<br>

!!! tip "Önemli Sketch Noktaları"

    - **Dimension'lar** mesafeleri kontrol eder (bir dikdörtgeni tam olarak 5 inç genişliğinde yapmak gibi).
    - **Constraint'ler** ilişkileri tanımlar (bir dikdörtgen kenarını diğerine kilitlemek gibi).
    - **Sarı noktalı çizgiler** otomatik constraint'leri gösterir — bunları kullanın!
    - **Origin** çapanızdır. Sketch'leri mümkün olduğunca origin'e bağlayın.
    - **Mavi kötü** — mavi bir sketch henüz tam olarak tanımlanmamış demektir. Her şey siyaha dönmelidir.
    - **Daha az iyidir** — tasarımınızı tam olarak kilitlemek için gereken en az dimension'ı kullanın.

---

### Ne Öğrendiniz

- Birden fazla boruyu ayrı ayrı nasıl extrude edeceksiniz
- Bir sketch'i nasıl oluşturacağınız ve kısıtlayacağınız
- Dikdörtgenleri nasıl düzgün yapacağınız
- Temel dimension'ları ve ilişkileri nasıl kullanacağınız
- Construction çizgileri kullanarak nasıl aynalayacağınız

---

## Egzersiz 3.2: Raylar Ekleme

<figure>
  <img src="/img/learning-course/stage1a/3-2-sketch.webp" style="width:100%">
  <figcaption>Bu sketch'i düzenleyin</figcaption>
</figure>


Şimdi bunu robota uygulayalım.

Egzersiz 3.2 part studio'sundaki Üst Boru Sketch'ini açın ve **birbirinden 8 inç uzaklıkta olan iki çapraz boru ekleyin**.

!!! Tip
    Sketch'i düzenlemek için feature tree'deki sketch'e çift tıklayın.

Yeni rayları kendiniz çizin. Sadece **toplamda bir yeni dimension** kullanın.

Görmemeniz gereken tek sayılar:

- 4.25" (modüller arasındaki boşluk)
- 1" (boru genişliği)
- 8" (çapraz raylar arasındaki mesafe)

<figure>
  <img src="/img/learning-course/stage1a/drivetrain-crossrail-sketch2.webp" style="width:90%">
  <figcaption>Final çapraz ray sketch kurulumu.</figcaption>
</figure>

---

### Çalışmanızı Kontrol Edin

??? info "Sketch'inizi bitirdikten sonra burayı tıklayın"

    Bunu sketch etmenin optimize edilmiş bir yolu:

    <iframe width="100%" height="400" src="https://www.youtube.com/embed/ktKuSFVV10U?controls=1&rel=0&showinfo=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>

    Yaklaşımınızı videoyla karşılaştırın.
    > Farklı olarak ne yaptınız?
    > Bir dahaki sefere böyle hatalardan nasıl kaçınırsınız?

<br>

Çalışmanızı kontrol etmeyi ve yaklaşımınızı gözden geçirmeyi bitirdikten sonra, bir sonraki egzersize geçin.

<br>
