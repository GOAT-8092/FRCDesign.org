# 2D: Kaskat Asansör

## Elevatorlar
Asansörler FRC'de sıkça ortaya çıkar ve mekanizmaları kompakt bir doğrusal şekilde hareket ettirmek için kullanılır. Bu genellikle bir mekanizma ile daha yüksek yerlere ulaşmak, çerçeve çevrenizden uzaklaşmak veya hatta bir saha unsuruna tırmanmak içindir. Asansörler genellikle "Rigging" edildikleri şekilde sınıflandırılır. Asansör "Rigging", motorun her aşamaya hareket iletilmesine izin veren şeydir. FRC asansörleri genellikle "Cascade" veya "Continuous" olarak rigging edilir.

<br>
<figure><img align="left"  src="\img\learning-course\stage2-elevator\2468elevator.gif" width="55%" style="border:5px solid #ADADAD"><img align="right" src="\img\learning-course\stage2-elevator\4414elevator.gif" width="39%" style="border:5px solid #ADADAD"></figure>
<center><figcaption>2468'nin Kaskat Asansörü ve 4414'in Sürekli Asansörü</figcaption></center>
<br>

Aşağıdaki match videolarını izleyerek [kaskat-rigging'li asansörlü 2468'nin 2023 Robotunu](https://www.youtube.com/watch?v=RAFjZgB_72w "2468 2023 Match Footage Video"){target=void} ve [sürekli-rigging'li asansörlü 4414'in 2023 Robotunu](https://youtu.be/PKPuqpe1Wlg "4414 2023 Match Footage Video"){target=void} aksiyon halinde görün.

### COTS Bileşenlerini Kullanma

Tipik olarak tasarlanan asansörler, satın alınması veya imal edilmesi gereken çok sayıda özel metal parça gerektirdiğinden, daha düşük kapasiteli bir takımın kapsamı dışında olabilir, ancak birinin nasıl çalıştığını bildiğinizde ve bir tane tasarladığınızda, minimal imalat kapabilitesi ve gerekli süre ile bir tane yapabilirsiniz. Bu proje, sürekli-rigging'li asansör yerine kaskat-rigging'li bir asansörün tasarımını tartışacaktır, çünkü COTS parçaların kullanılabilirliği ve kaskat-rigging'li bir asansör için gereken minimal imalat.

### Kaskat Asansör
Kaskat asansörler, aşamaların hareket etme biçimiyle karakterizedir. Kaskat rigging'li bir sistemde, her asansör aşaması ebeveyn aşamasından aynı mesafede hareket eder.

<figure markdown="span">
    ![cascade](/img/learning-course/stage2-elevator/cascade.gif)
    <figcaption>Kaskat Hareketi</figcaption>
</figure>

### Karşılaştırma

| **Kategori** | **Kaskat Rigging** | **Sürekli Rigging**|
|----------|----------|----------|
| Aşama Sayısı | 3'ten fazla aşamalı kaskat asansörler yapmak mümkündür, ancak rigging'i tasarlamak özellikle genişlik kısıtlıysa zorlaşır. | Ek aşamalar eklemek nispeten basittir |
| Aşama Sırası | Tüm aşamalar aynı anda birlikte hareket ettiği için, sürekli rigging'e kıyasla orta uzatma aralığında ağırlık merkeziniz daha yüksek olacaktır| Aşamalar, aşamalar arasındaki sürtünme ve her aşamayı hareket ettirmek için kuvvete dayalı olarak yukarı hareket eder. Düzgün yapılırsa, iç aşamalar önce hareket etmelidir.|
| COTS | Kablo rigging için birçok seçenek mevcuttur. | Kablo rigging için kadar çok seçenek yoktur|
| Dişli Kutusu (Aynı uç efektör hızı ve kuvveti verildiğinde) | Tırmanma gibi durumlar için ara aşamaları kullanabilir, ki bunlar son aşamadan daha fazla kuvvete sahiptir (Bkz. [2056'nın 2018 robotu](https://www.youtube.com/watch?v=47A83OfzYDw "2056's 2018 robot Behind the Bumpers Video"){target=void}) | Daha az redüksiyon gerektirir, ancak farklı yüksek hız ve yüksek kuvvet modlarına sahip olmak için shifting dişli kutusu gerektirir |
| Geçiş | Rigging'in konumunu değiştirerek elde edilebilir | Rigging'in konumunu değiştirerek elde edilebilir. Ara aşama pozisyonları, aşama hareket sırasının ne kadar iyi ayarlandığına bağlı olarak belirsiz olabilir. |

<br>
