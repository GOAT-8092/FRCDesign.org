---
title: En İyi Uygulamalar
description: Onshape'da mekanizma belgelerinizi organize ederken takip edilmesi gereken en iyi uygulamalar.
---

# Alt Belge Kurulumu

Her alt sistem belgesinin en az bir part studio'su ve bir assembly'si olmalıdır.

Aşama 2A Temel Shooter, hareketli parçası olmayan basit bir alt sistemdir. Bu sadece bir part studio ve bir rijit assembly içerir.

<center markdown>[Aşama 2A - Temel Shooter](https://cad.onshape.com/documents/8f093edaad44b5702e92ddd9/w/fefbb7a7af099fc237c1513a/e/84d7075719d34c35b3be9410 "Aşama 2A Temel Shooter Onshape Belgesi"){:target="_blank" .md-button .md-button--primary}</center>

<center><img src="/img/best-practices/shooterAssembly.webp" style="border:5px solid #ADADAD"></center>

### Birden Fazla Serbestlik Derecesine Sahip Alt Sistemler

Birden fazla serbestlik derecesine sahip alt sistemleri birden fazla rijit assembly'ye ayırmak isteyebilirsiniz. Alt sistemin her ayrı hareketli parçasının bir 'rijit' assembly'si olmalıdır (hiçbir parça için serbestlik derecesine izin verilmez), üst düzey alt sistem assembly'si sadece aralarındaki hareketi tanımlar.

!!! Not
    Bir rijit assembly, eklendiğinde, hesaplanan hiçbir mate olmadan katı bir gövde olarak ele alınır. Üst düzey assembly'lerde yükleme süresini büyük ölçüde azaltır. Parametrik mate'ler için origin cube'u bu sisteme nasıl entegre edeceğinizi [assembly en iyi uygulamalarında](assembly-setup.md) öğreneceksiniz.

Örneğin, bir asansör belgesini her aşama için bir part studio ve ilgili rijit assembly'ye ayırabilirsiniz. Üst düzey asansör assembly'si böylece her aşama alt assembly'sini ve slider mate'leri içerecektir.

Aşama 2C Slapdown Intake, statik bir bölümü ve dönen bir bölümü olan bir alt sistemdir. İşlevsel olarak, bu bir part studio, dişli kutuları ve pivot için statik bir assembly, kollar ve silindirler için rijit bir assembly ve iki alt assembly'yi birleştiren üst düzey bir assembly içerir.

<center markdown>[Aşama 2C - Slapdown Intake](https://cad.onshape.com/documents/17302d787e092ce11015f7ee/w/f7cf5c02c7655f0328a3a74a/e/f1456325e0175c4c081008c2 "Aşama 2C Slapdown Intake Onshape Belgesi"){:target="_blank" .md-button .md-button--primary}</center>

<center><img src="/img/best-practices/subassembly.webp" style="border:5px solid #ADADAD"></center>

Aşama 2D Cascade Asansör, statik bir bölümü ve lineer kayan iki alt assembly'yi olan bir alt sistemdir. Bu bir part studio, statik bir çerçeve/dişli kutusu assembly'si, ilk aşama ve carriage için assembly'ler ve slider mate'lerle 3 alt assembly'yi birleştiren üst düzey bir assembly içerir.

<center markdown>[Aşama 2D - Cascade Asansör](https://cad.onshape.com/documents/da5aef9e6bf6e869f4a51a45/w/5a0f4a3426876db0ba214277/e/f8fd8133abcb12800eacb5d1 "Aşama 2D - Cascade Asansör Onshape Belgesi"){:target="_blank" .md-button .md-button--primary}</center>

<center><img src="/img/best-practices/elevatorAssembly.webp" style="border:5px solid #ADADAD"></center>

<br>
