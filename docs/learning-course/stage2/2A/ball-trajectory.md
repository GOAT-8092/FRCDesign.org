# 2A: Basic Shooter

## Ball Trajectory

Bir top shooter'da, trajektori öncelikle oyun parçasının çıkış açısı ve çıkış hızı tarafından belirlenir, bu da topu ne kadar sert fırlattığınız ve shooter'ı nereye yönlendirdiğiniz anlamına gelir.

<!-- Rigidity is crucial for maintaining trajectory consistency. Any wobbling or flexing in the shooter structure can negatively impact accuracy, as even slight movements can alter the exit angle or velocity, leading to unpredictable shot behavior. -->

<figure>
    <img src="/img/learning-course/stage2-shooter/shot-trajectory.gif" style="width:70%; border:5px solid #ADADAD; border-radius: 2%">
    <figcaption>Takım 1678'nin 2022 shooter top trajektörisi.</figcaption>
</figure>

### Referans Tasarım

2020 için, sahadaki başlangıç çizgisi atış pozisyonunuzu ve açınızı tahmin etmek için bir referans noktası olarak hizmet edebilir. Golün skoring alanı, pozisyondaki küçük varyasyonları karşılayacak kadar affedici olduğu için hassas hizalamayı daha az kritik hale getirir. Bir atış mesafesi hesaplayıcı kullanarak, optimal atış parametrelerini tahmin edebilirsiniz.

### Trajektori Hesaplayıcı

Açı ve hızdaki ayarların atışınızı nasıl etkilediğini görmek için [bu 2020 trajektori hesaplayıcısını](https://www.desmos.com/calculator/euvciqv3tr "Desmos 2020 Trajcetory Calculator"){:target="_blank"} keşfedin. Bazı pozisyonel varyasyonlarla tutarlı skora izin veren bir açı ve hız kombinasyonunu belirleyebilir misiniz?
!!! Calculator
    <center><iframe src="https://www.desmos.com/calculator/5fil8alfmd?embed" width="500" height="500" style="border: 1px solid #ccc; border-radius: 2%" frameborder=0></iframe></center>

<br>
