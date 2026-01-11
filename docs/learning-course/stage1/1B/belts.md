# 1B Güç Aktarımı

## Kayış ve Kasnak Temelleri

Zamanlama kayışı ve kasnak sürücüleri, dönen miller arasında hareket ve gücü iletmek için esnek kayışlar ve kasnaklar kullanan mekanik sistemlerdir. Sistem iki ana bileşenden oluşur: kauçuk gibi bir malzemeden yapılmış esnek bir döngü olan kayış ve kayışın sarıldığı oluklu tekerlekler olan kasnaklar. Bir kasnak dönerken, kayışı sürer ve bu da diğer kasnağı sürerek hareketi ve gücü bir mildden diğerine aktarır.


<figure>
  <img src="../images/belt\belt-and-pulley.webp" style="width:50%">
  <figpcation>Bir kayış ve kasnak aktarma orgüsü. (Görsel Kaynak: <a href="https://www.reca.lc/belts" target="_blank">ReCalc</a>)</figcaption>
</figure>

Girişten çıkışa tork ve hızı değiştirmek için, farklı boyutlarda kasnaklar kullanılmalıdır. Kayış aktarma organları için mekanik avantaj, dişlilere benzer şekilde, çıkış kasnağındaki diş sayısının giriş kasnağındaki diş sayısına oranı temelinde oluşturulur. Dişlilerin aksine, kasnakların aynı yönde döneceğini unutmayın.

### Kayış Türleri

Dişliler gibi, kayışların da bir pitch'i (adımı) vardır. Pitch, kayıştaki her diş arasındaki mesafe olarak tanımlanır. FRC'de bu genellikle 5 mm'dir. Kayışın *pitch uzunluğu* ise pitch'in (5 mm) diş sayısı ile çarpılmasıdır. Kayışlar her zaman tam sayı diş sayısına sahip olur, bu nedenle pitch uzunluğu 5mm'in bir katı olur.

Örneğin, 80 dişli bir kayış 400 mm uzunluğunda olacaktır.
<!-- Bir kasnağın çap çapını hesaplamak için aşağıdaki denklem kullanılabilir:
<center>**`PD = Pitch * (# of Teeth) / 3.14`**</center> -->

Kayışlar çeşitli genişliklerde de gelir. FRC'de genellikle 9 mm veya 15 mm genişliğinde kayışlar kullanırsınız.

### Kayış Aktarma Organlarını Modelleme

Kayışları modellemek için iki featurescript'e ihtiyacınız olacak: [`Origin Cube` Featurescript](https://cad.onshape.com/documents/321c197a842fc5f1a29e6621/w/fc3cdd5ca7edcd93e02f13cc/e/2b321cb91b74224b9c14b433 "Origin Cube Featurescript Onshape Document"){:target="_blank"} ve [`Belt & Chain Gen` Featurescript](https://cad.onshape.com/documents/53c0b14cad92676c14e04e97/w/1271c254ccb0a79563210195/e/7394c4a86d8d6c35c9a12041 "Belt & Chain Gen Featurescript Onshape Document"){:target="_blank"}. `Belt & Chain Gen` Featurescript'inin kayışı oluşturabilmesi için, en az iki kasnağın veya zincir dişlisinin çap çapını ve doğru merkezden merkeze mesafesine ihtiyacı vardır, her ikisi de `Origin Cube` featurescript'indeki fonksiyonları kullanacaktır.

!!! Note
    Origin Cube ayrıca robot ve mekanizma assembly'leri için ek işlevlere sahiptir ve bunlar sonraki aşamalarda tartışılacaktır. Bu uygulamaları [assembly best practices page](../../../best-practices/assembly-setup.md "Assembly Best Practices Page") sayfasından inceleyebilirsiniz. Origin Cube özelliği fonksiyonların kullanılabilir olması için bundan böyle tüm part studio'larda **ilk özellik olmalıdır**.

1. <code>Origin Cube</code> Featurescript'ini kullanarak <code>Origin Cube</code> özelliğini ekleyin. 1B alıştırmaları özellik tarafından oluşturulan küpü gerektirmediği için işaretini kaldıracağız.
  <figure>
    <img src="../images/belt/origin-cube.webp" style="width:100%">
    <figcaption>Origin Cube Özellik Seçenekleri</figcaption>
  </figure>

2. Layout sketch'inizde, kasnak çap çaplarını temsil eden iki daire çizin. <code>#PulleyPD_5mm(# of teeth)</code> fonksiyonunu kullanarak daireleri dimension yapın.

    - `#PulleyPD_5mm(n)`: `n` dişli 5 mm pitch kasnağın çap çapını hesaplar.
    - Örnek: `#PulleyPD_5mm(18)` 18 dişli 5mm pitch kasnağın çap çapını döndürür.

    !!! Tip
        Bu genellikle layout sketch'inizde yapılır, çünkü kayışlarla bağlanan miller arasındaki mesafeler, en yakın kayış boyutu için merkezden merkeze mesafeye göre belirlenir.


3. Kasnakları bağlamak için merkez çizgisini çizin ve hedef c-c mesafenizi ayarlayın. Bu örnekte, hedef c-c mesafemiz 5". Tüm sketch varlıklarının construction olduğunu doğrulayın. İsteğe bağlı olarak daireleri tangent çizgilerle bağlayın. Sketch'i onaylayın.
  <figure>
    <video width="1920" controls>
      <source src="../images/belt/belt-cad-1.webm" type="video/webm">
      Tarayıcınız video etiketini desteklemiyor.
    </video>
  </figure>

4. Kayışın 3D modelini oluşturmak için <code>Belt & Chain Gen</code> Featurescript'ini kullanın. Referans düzlemi mate connector, kayışın merkez çizgisinin konumunu ayarlar. Seçili mate connector'ı değiştirerek kayışın konumunu ayarlayabilirsiniz. Ayrıca kayış dişleri oluşturmayı seçebilirsiniz, ancak bu yeniden oluşturma süresini önemli ölçüde artırır ve önerilmez.
  <figure>
    <video width="1920" controls>
      <source src="../images/belt/belt-cad-2.webm" type="video/webm">
      Tarayıcınız video etiketini desteklemiyor.
    </video>
  </figure>

5. <code>Belt & Chain Gen</code> Featurescript'i en yakın tam sayı kayış boyutunu ve pitch uzunluğunu döndürecektir. Sadece 5T artışlarında kayış stokladığınızı varsayarsak, bir sonraki en yakın kayış boyutu 80T'dir.
  <figure>
    <img src="../images/belt/belt-cad-3.webp" style="width:100%">
    <figcaption></figcaption>
  </figure>

6. 80T kayışı için tam bir c-c mesafesi elde etmek üzere c-c dimension'ını <code>#BeltCTC_5mm()</code> fonksiyonunu kullanacak şekilde değiştirin. <code>Show Expressions</code> kutusunu işaretlemek, kayış pitch'ini, kasnak diş sayılarını ve kayış diş sayısını görmenizi sağlar.

    - `#BeltCTC_5mm(n1, n2, n3)`: `n2` diş sayısına sahip kasnağı ve `n3` diş sayısına sahip kasnağı bağlayan `n1` dişli 5 mm pitch kayışın c-c mesafesini hesaplar.
    - Örnek: `#BeltCTC_5mm(80,18,36)` 18T kasnağı 36T kasnağına bağlayan 80T 5 mm pitch kayış için merkez mesafesini döndürür.

    <figure>
      <video width="1920" controls>
        <source src="../images/belt/belt-cad-4.webm" type="video/webm">
        Tarayıcınız video etiketini desteklemiyor.
      </video>
    </figure>

    ???+ Note "Tasarım Niyetini Yakalama"

        Bu iki Featurescript'in ortaya çıkmasından önce, tasarımcılar c-c mesafelerini hesaplamak için [ReCalc](https://www.reca.lc/belts "ReCalc Design Calculator"){:target="_blank"} gibi çevrimiçi hesap makinelerini kullanmak zorundaydı. Ancak, bu yöntem tasarım niyetini yakalamaz, çünkü hesaplanan bir değeri layout sketch'e kopyalama-yapıştırmaya dayanır.

        <figure markdown="span">
          <img src="../images/belt/design-intent-1.webp" style="width:75%">
          <figcaption>Tasarım niyeti üst sketch'te yakalanmış ama alt sketch'te yakalanmamış.</figcaption>
        </figure>

7. <code>Belt & Chain Gen</code> özelliği otomatik olarak güncellenir ve kayış diş sayısının doğru olduğunu (80T) ve pitch uzunluğunun 5 mm'in bir katı olduğunu, yani kayış diş sayısının tam olduğunu ve yuvarlanmadığını görebiliriz.
  <figure>
    <img src="../images/belt/belt-cad-5.webp" style="width:100%">
  </figure>




<br>
