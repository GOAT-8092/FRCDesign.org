# Yapı

Sağlam ve çok yönlü robot yapıları oluşturma rehberi. Farklı malzemeleri, teknikleri ve COTS bileşenleri kapsar.

<!-- Add round tube, rectangular tube, thin vs thick wall tube -->

## Kutu Profil

**Çok Yakında**

### Profil Plugs

Profil plakaları, kutu profilin uçlarına giren metal Inserts'lerdir ve gusset kullanımı olmadan profilleri birbirine bağlamanıza izin verir. Profil plakalarını ezici bloklarla birleştirmek, profiller arasında basit ve güçlü bir bağlantı sağlar. Profil plakaları, tasarım sürecini ne kadar basitleştirdikleri nedeniyle modern asansör tasarımlarında büyük kullanım alanı bulur. Rulman bloklarının gussetlerle karışmasını konusunda endişelenmenize gerek kalmaması, tasarım karmaşıklığını büyük ölçüde azaltırken aynı zamanda parça sayısını ve robot maliyetini de azaltır. Profil plakalarını profile cıvatalarken genellikle mevcut olan 8 cıvatanın hepsini kullanmanıza gerek yoktur, çoğu kullanım durumu için 2-4 yeterlidir.

!!! Not
Profil plakaları 1/8" duvar kalınlığına sahip profillere sığacak şekilde yapılmıştır. Daha ince duvarlı profiller için, profil plakasının dışında (muhtemelen 3D yazdırılmış) bir plastik manşet kullanarak boşluğu güce kaybetmeden doldurabilirsiniz.

!!! Info "Önemli"
Profil plakaları kullanırken, profiller arasında güçlü bir bağlantı yapmak için profil ucuna göre iyi toleranslı delikler gereklidir.

<center markdown>![tube plug](/img/best-practices/tube-plug.webp){width=50%}</center>

### Ezici Bloklar

Ezici bloklar, modern FRC'de ince duvarlı kutu profilinin sık kullanılması nedeniyle yaygındır. Ezici blokların ana amacı, kuvvetlerin profilin ince duvarını burkulmasını önlemektir. Bu, profil üzerinde bir cıvatalayı aşırı sıkmakla çok kolay yapılır. Böylece, ezici bloklar ezici blok olmadan olduğundan daha sıkı cıvataları sıkmanızı sağlar. Bu bağlantıyı ve profili bir bütün olarak sertleştirir.

!!! Not
Ezici bloklar herhangi bir malzemeden yapılabilir, ancak ezici bloklar için 3D yazıcı ile yazdırmak bugüne kadar en basit üretim yöntemidir. Yazıcı toleranslarını hesaba kattığınızdan emin olun. Ezici bloklar çok gevşek olmamalıdır, ancak içine sokmak için zorlamak da istemezsiniz.

<center markdown>![simplest_crush](/img/best-practices/simplest-crush.webp){width=25%}</center>
Yukarıda ezici bloğun en basit formu: profilin içindeki boşluğu dolduran ve cıvataların geçmesi için bazı delikleri olan bir plastik parçası. Bir profilin ucundaki ezici blok için, profildeki deliklerle hizalamaya yardımcı olmak için bir flanş ekleyebilirsiniz. Ezici bloklar, monte edilmesi ve servis edilmesi zor olacağı için uzun profillerin ortasında kullanmak için ideal olmayabilir; bu yerlerde, cıvataların sıkılmasından kaynaklanan yükü yaymaya yardımcı olmak için profilin dışına ekstra 1/16" bir plaka ekleyebilirsiniz, işlevsel olarak büyük bir pul olarak hizmet eder. Ekstra güç için, 3D yazdırırken duvar sayısını 4-6'ya artırmayı düşünün.

<br>
