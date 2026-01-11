# 2C: Slapdown Intake

## Pivot

### Diş Oranı

Pivot, 2 aşamalı MAXplanetary dişli kutusu üzerinde tek bir Kraken motor ile güçlendirilir. MAXplanetary'deki 4:1 aşamaları (16:1) ve 12:48 sprocket redüksiyonu pivot için toplam 42:1 genel redüksiyon yapar.

Bir kol hesaplayıcı kullanarak kendi mekanizmanızda bu kadar redüksiyon isteyip istemediğinizi değerlendirebilirsiniz, ancak çoğu intake için 30:1 ile 42:1 arası iyi olmalıdır.

### Pivot Tasarımı

MAXplanetary, dönüşü uzun bir çapraz mile transfer etmek için 1:1 kayış/kasnak kullanır. Tüm özel kasnaklar, onların soyulmasını önlemek için COTS metal insertler için cepler vardır. Bu çapraz milin her iki ucunda sprocket'ler vardır, zincir kola bağlı sprocket'lere yukarı çıkar. Bu kurulum, intake'ın her iki tarafının eşit olarak yukarı ve aşağı hareket etmesini sağlar, böylece intake üzerinde garip bükülme kuvvetleri yoktur.

### Backlash ve Sensör Geri Bildirimi

Sistemdeki backlash'ı azaltmak için, 1:1 kayış/kasnak tam merkezden merkeze mesafededir ve zincirler inline tensioner'larla gerilir. Kolların çıkışındaki büyük sprocket'ler de zincirle daha fazla diş teması için iyidir.

Intake pozisyonunu kontrol etmek için, mutlak bir kodlayıcıya gerek yoktur. Depolandığında ve hardstop'a karşıyken konumu sıfırlayabilir veya robot açıkken zeminde dinlenmesini sağlayabilir ve belirli bir aşağı pozisyona götürmek için göreli kodlayıcıyı kullanabilirsiniz.

<figure>
    <img src="\img\learning-course\stage2-slapdown\pivot.webp" alt="Power Example" width="60%" style="border:5px solid #ADADAD">
    <figcaption> Referans Tasarım Intake Pivot'u</figcaption>
</figure>

<br>
