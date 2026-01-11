# 1E: Alt Sistem İş Akışı - Drivebase Detaylandırma

## Elektronik Montajı

Robotun kablo bağlamasını ve daha sonra kablo bağlamasını incelemeyi kolaylaştırmak için, her elektrikli bileşenin etrafında yeterli boşluk bırakılmalıdır. Çeşitli kontrol sistemi parçaları için en iyi konumu belirlemek için elektronik takım arkadaşlarınızla çalışmalısınız. Takımlar genellikle yer varsa elektroniklerini bellypan'a monte etmeye çalışırlar.

!!! Örnek
    <figure>
        <img src="../images/elec/elec-example.webp" style="width:80%">
        <figcaption>Bellypan üzerinde çeşitli elektronik bileşenlerin örnek yerleşimi. (Fotoğraf: FRC 3647)</figcaption>
    </figure>

### Elektronik Bileşenler

Aşağıda FRC robotlarında bulunan tipik elektrik bileşenlerinin bir listesi ve önerilen montaj konumu sunulmuştur. Yine, montaj konumları robotunuzun geri kalanına büyük ölçüde bağımlıdır, her zaman en iyisinin ne olduğunu karar vermek için elektronik takımınızla koordinasyon içinde olduğunuzdan emin olun.


!!! not "FRC Elektronik Bileşenleri"
    | **Bileşen** | **İşlev** | **Önerilen Konum** | **Görsel** |
    |---|---|---|---|
    | REV Power Distribution Hub (PDH) veya  CTRE Power Distribution Panel (PDP) | Gücü diğer tüm bileşenlere dağıtır | Bellypan | ![PDH](../images/elec-components/pdh.webp) |
    | Ana Şalter | Robotu açmak/kapatmak için kullanılır ve elektronikleri aşırı yüksek akım çekilen olaylardan korur | PDH ve Batarya'ya yakın ve kolayca erişilebilen bir yer | ![Ana Şalter](../images/elec-components/mbreak.webp) |
    | RoboRIO | Tüm robot işlemleri için merkezi kontrolcü | Bellypan | ![RoboRIO](../images/elec-components/rio.webp) |
    | Entegre motor kontrolörü (örn: Falcon 500, Kraken X60) | Entegre motoru güçlendirir ve kontrol eder | Elektrik montajı gerekmiyor | ![Entegre motor kontrolörü](../images/elec-components/kx60.webp) |
    | Ayrık motor kontrolörü (örn: Spark Max, Talon SRX) | Bazı motorları (örn: NEO, CIM) güçlendirmek ve kontrol etmek için gereklidir | Kontrol edilen motorun yakınında veya bellypan üzerinde | ![Ayrık motor kontrolörü](../images/elec-components/smax.webp) |
    | Robot Radyosu | Robotun sahadaki veya sürücü istasyonundaki kablosuz bağlantılar kurmasına izin verir | Vivid Hosting'in [radyo montaj yönergelerini](https://frc-radio.vivid-hosting.net/getting-started/usage/mounting-your-radio "Vivid Hosting Radyo Montaj Yönergeleri"){:target="_blank"} takip edin. | ![Robot Radyosu](../images/elec-components/vh109.webp) |
    | Robot Sinyal Işığı (RSL) | Robotun açık olup olmadığını ve etkinleştirildiğini/devre dışı bırakıldığını gösterir | Kolayca görülebilir bir yerde | ![Robot Sinyal Işığı](../images/elec-components/rsl.webp) |
    | Atalet Ölçüm Birimi (IMU) | Robot başlangıcını ve ivmesini belirlemek için kullanılır | Merkeze yakın olmak en iyi uygulamadır (Bellypan üzerinde veya RoboRIO'ya takmak için VHB bant) | ![Atalet Ölçüm Birimi](../images/elec-components/imu.webp) |
    | Voltaj Regülatör Modülü | Özel devreler için kullanılabilir | Bellypan | ![Voltaj Regülatör Modülü](../images/elec-components/vrm.webp) |
    | Pnömatik Hub | Pnömatik bileşenleri kontrol eder | Bellypan | ![Pnömatik Hub](../images/elec-components/pcm.webp) |

<br>
