---
title: Layout Sketch En İyi Uygulamaları
description: Ana layout sketch'ler oluştururken takip edilmesi gereken en iyi uygulamalar.
---

# Layout Sketch En İyi Uygulamaları

Ana layout sketch, her mekanizmanın ana boyutlarını, alan öğesi etkileşimlerini ve robot boyut kısıtlamalarını yakalayan sketchler serisidir. Daha sonra, ana layout sketch'ler her mekanizmanın part studio'suna eklenir ve bireysel bileşenler ithal layout sketch etrafında modellenir. Bu, üstten aşağı tasarım yaklaşımıyla çok daha kolay entegrasyon sağlar.

| **Her Zaman Dahil Edin**                                                          | **Bazen Dahil Edin**                               | **Asla Dahil Etmeyin**                                           |
|:----------------------------------------------------------------------------|:----------------------------------------------------|:------------------------------------------------------------|
| Drivebase boyutları                                                        | Dişliler                                               | Plakaların şekli gibi belirli detayler                   |
| Prototipe dayalı end-effector tekerlek konumları                       | Kayışlar                                               | Gussetler                                                     |
| Alan öğeleri ve uzatma sınırları                                         | Zincir                                               | Montaj delikleri                                              |
| Mekanizma hareket yolları                                                      | Motor konumları                                     | &nbsp;                                                      |
| Gamepiece yolu                                                              | &nbsp;                                              | &nbsp;                                                      |

Bu kapsamlı bir liste değildir ve şeyler takımdan takıma ve mimariden mimariye değişebilir. Gerekirse detay kolayca eklenip çıkarılabilir.

Robotun geometrisini yönlendiren tüm önemli ölçümler layout sketch'ler part studio'sunda vardır. Hepsi kolayca görülebilir ve birlikte değiştirilebilir, üst düzey robot assembly'sinde şeyleri sığdırmaya çalışmak için her alt sistemi geçmek zorunda kalmak yerine.

<figure>
<img src="/img/best-practices/1778-2024-MS-Part-Studio.webp" style="border:5px solid #ADADAD"></center>
<figcaption>1778 Chill Out'un 2024 Robotu Ana Layout Sketch'leri</figcaption>
</figure>

Ana layout sketch'ler her zaman drivetrain'iniz, bumper'ler, initial konfigürasyon ve uzatma sınırları ile başlar. Alan öğeleri daha sonra sketch edilir. Robotun çok fazla yazılım veya mekanik karmaşıklık olmadan parçaları puanlayabileceğinden emin olmak için bumper'lara karşı sert hizalama kullanabilirsiniz.

!!! İpucu
    Kickoff'tan hemen sonra, drivetrain, uzatma sınırları ve alan öğelerinin layout sketch'leri ile bir part studio oluşturabilirsiniz. Bu, kopyalanabilir ve birkaç farklı robot mimarisinin geometrilerini test etmek için kullanılabilir, sonra arasında karar vermek için.

Robotunuzun alan öğeleri ve gamepieces ile etkileşimi için özel olarak tasarlanmalıdır. Ana layout sketch'ler için, bu, her alt sistemin her boyutunu kasıtlı hale getirmek anlamına gelir, ister alan öğelerine, ister uzatma sınırlarına veya birbirlerine dayalı olsun.

!!! Örnek
    Bir asansörün uzunluğu, taşınan manipülatörün başlangıç ve bitiş pozisyonları tarafından yönlendirilir, çünkü bu pozisyonlar alan öğeleriyle nasıl etkileştiğine dayanır.

!!! İpucu
    Dönen bir alt sistemin hareket aralığını temsil eden inşaat daireleri oluşturabilir ve aralarında boşluk olduğundan emin olmak için bir alt sistemi daireden belirli bir mesafeye boyutlandırabilirsiniz.

Etkili layout sketch yapmak, organize kalmanızı gerektirir. Bu şunları ifade eder:

- Ana layout sketch part studio içinde genellikle alt sistem başına birden fazla sketch. Her şeyi ayrı tutun!
- Sketch'leri buna göre adlandırın
- Ayrıca sketch'lerinizi [farklı renklere](https://www.youtube.com/watch?v=ZG_gVeGdI5c "Onshape'de Sketch'lere Renk Ekleme Video Öğreticisi"){:target="_blank"} getirebilirsiniz, böylece aralarında fark edebilirsiniz
- Her hareketli alt sistemin tüm olası durumlarını sketch edin

<figure>
<img src="/img/learning-course/stage1d/exampleMasterSketch.webp" width="70%" style="border:5px solid #ADADAD"></center>
<figcaption>3647'nin 2024 Robotu Ana Layout Sketch'leri</figcaption>
</figure>

Layout sketch yapmak, alışkanlık gelmesi için biraz pratik gerektirebilen bir sanattır. Aşama 3 tam layout sketch'leri öğrenmekte ve pratik yapmada size yardımcı olacaktır, ancak emin değilseniz [bu öğretici](https://www.youtube.com/watch?v=Bd_XzBw5V_U "2023 David Bot Ana Layout Sketch Canlı Yayını"){:target="_blank"} başlamanıza yardımcı olabilir.

Bir örneğin sunumu: [8177 Vector 2023 Robotu](https://docs.google.com/presentation/d/1IwjXvcAZFVcEUFSZZDHlTYlLA_5PbI3wPJzbfAOTz8Y/edit?usp=sharing "8177 2023 Robotu Ana Layout Sketch Sunumu"){:target="_blank"}

<br>
