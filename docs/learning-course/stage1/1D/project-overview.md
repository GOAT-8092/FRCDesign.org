# 1D: Tasarım Metodolojisi - Basit Swerve Şasisi

## Proje Genel Bakış

Bu aşamada, bir swerve şasisi tasarlayacaksınız. Bir şasi, tüm diğer mekanizmalarımızın etrafında tasarlandığı ve tutturulduğu mobil platformdur. Güvenilir COTS swerve'in ortaya çıkışı ile, swerve şasisi tasarımı önemli ölçüde kolaylaşmıştır ve FRC'de en yaygın kullanılan rekabetçi şasi haline gelmiştir.

Bir swerve şasisi dört *swerve modülünden* oluşur. Her modülün iki motoru vardır: biri tekerleği döndürmek için ve diğeri onu yönlendirmek için. Bu, robotun rotasyonundan bağımsız olarak herhangi bir yönde hareket etmesini sağlar. Bu projede, [SDS MK4i modüllerini](https://www.swervedrivespecialties.com/products/mk4i-swerve-module "SDS MK4i Product Page"){:target="_blank"} kullanacağız. Birçok başka COTS seçeneği mevcuttur, her birinin kendi avantajları ve ticari ödünleşimleri vardır.

<!-- You can learn more about drivetrains on the [Design Handbook](/design-handbook/mechanisms/drivetrain/) page. -->

<figure>
    <img src="../images/drivetrain-assembly.webp" style="width:80%">
    <figcaption>1D Aşaması swerve şasisi projesi.</figcaption>
</figure>

Önceki egzersizlerde olduğu gibi, tamamlanmış proje referans için mevcuttur. Yardıma ihtiyacınız varsa, lütfen [Discord'da](https://discord.gg/qdx7pdZKx4 "DDS Discord Invite"){:target="_blank"} sormaktan çekinmeyin!

<center markdown>[1D Şasi Referansı](https://cad.onshape.com/documents/6c6044229091a87cf359270b/w/ed9648f0c04c639a2561615a/e/67a7ed0c6038787281325a51 "1D Drivebase Reference Onshape Document"){:target="_blank" .md-button .md-button--primary }</center>

### Şasi Çerçevesi

1A Aşamasında tanıtıldığı gibi, robot yapıları genellikle alüminyum kutu tüplerinden inşa edilir. Şasi de bir istisna değildir. Çoğu takım, kutu tüplerini standart 0.5" aralıklı 0.196" çaplı delik deseniyle tasarlamayı tercih eder. Bu, modülerlik sağlar ve köşebentler gibi birçok COTS bileşeninin kolay entegrasyonuna izin verir.

Kutu tüp ekstrüzyonları çoğu metal tedarikçiden satın alınabilir, ancak [WCP](https://wcproducts.com/collections/systems-structure/products/punched-tubing){:target="_blank"}, [TTB](https://www.thethriftybot.com/products/thrifty-box-extrusion){:target="_blank"} ve [REV](https://www.revrobotics.com/MAXTube/){:target="_blank"} gibi birçok FRC satıcısı önceden kesilmiş delik desenlerine sahip kutu tüpleri satar ve bu da üretim süresini ve ekipman gereksinimlerini önemli ölçüde azaltabilir.

<br>
