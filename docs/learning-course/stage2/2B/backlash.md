# 2B: Dingil Silisi Pivot

## Backlash

Özellikle pivotlar için, daha iyi kontrol için mümkün olduğunca rijit yapmak istediğiniz için, backlash'ı mümkün olduğunca azaltmak için adımlar atmanız gerekir.

| **Kaynak**        | **Detaylar**  | **Çözüm**  | Resim |
|-------------------|----------------------------|---------------------------------------------------------------------|-----|
| **Hex Arayüzleri**| Hex'den hex deliği arayüzlerindeki boşluklar backlash oluşturur. | Shim bant kullanarak boşlukları azaltın.  | <img src="/img/design-handbook/DFC/hightide%20shim%20tape%20placement.webp" width=40%>
| **Sprocket Clocking** | Düzginsiz hareketi önlemek için sprocket'lerin doğru hizalanmasını sağlayın.   | Her iki taraftaki düzensizlikleri hizalayın. |<img src="\img\learning-course\stage2-pivot\wcp sprocket clock.webp" width=40%><figcaption>Sprocket üzerindeki düzensizliğe dikkat edin</figcaption>
| **Montaj Slop** | Gevşek cıvata-delikli arayüzler slop getirebilir.  | Uygun cıvatalama ve güçlü spacerler kullanın. |
| **Redüksiyon Aşamaları**| Daha fazla redüksiyon aşaması backlash artırır. | Optimal performans için aşamaları 3 veya daha az tutun. "Aşamalar"dan biri sprocket redüksiyonudur|
| **Zincir Gerilmesi** | Zincirin zamanla gerilmesi backlash'a neden olur| Zincir gerilmesini periyodik olarak kontrol edin. Çok yüksek hassasiyet gerekiyorsa (shooterlar), bunun yerine bir sektör dişli kullanın|

Bu çözümlerle ilgili detaylar [kontrolden tasarlama hakkında tartışan tasarım el kitabı sayfasında](../../../design-handbook/design-writeups/DFC.md "Designing for Controllability Page"){:target="_blank"} ele alınmaktadır.


### Referans Tasarım

Backlash genellikle gerçek hayat toleransları sonucu ortaya çıktığı için CAD'de modellemek zordur. Referans tasarım gerçek hayatta yapılsaydı, dişli slop'unu azaltmak, hizalanmış sprocket'ler ve backlash'ı en aza indirmek için düzgün gerilmiş zincir için shim bandı kullanırdı.

<br>
