---
title: Katkıda Bulunma Yöntemleri
description: Web sitesine halka açık olarak katkıda bulunma kılavuzu, IDE kurmayı ve düzenleme için yerel önizlemeyi içerir.
---

# Katkıda Bulunma Yöntemleri

## Halka Açık Katkı

Herkes markdown bilgisi veya github olmadan web sitesi için içerik oluşturabilir, ancak diğer katkıda bulunanların iş yükünü azaltmak için her ikisini de öğrenmeyi tercih ederiz.

[Discord sunucusunda](https://discord.gg/qdx7pdZKx4 "FRC Design Discord Sunucusu"){:target="_blank"}, ["website-discussion" kanalına](https://discord.com/channels/1120162219502608426/1233961750639018104 "#website-discussion Discord Kanalı"){:target="_blank"} gidin ve bu şablonu doldurarak katkıda bulunmak istediğiniz şeyi yapabileceğinizi sorun:

    Sorun/içerik:
    Çözüm veya içeriğin uygulanması hakkında notlar:
    Ne zaman bitirmeyi planlıyorsunuz?:
    Alternatif bir platform kullanıyor musunuz veya Github'ta fork yapıyor musunuz?:

Bu, zamanınızı boşuna harcamamanız veya zaten birinin üzerinde çalışmaya başladığı bir şey olmaması içindir.

Çalışmaya başlamak için onay alırsanız, bir iç katkıda bulunan ["public-website-contribution" forum kanalında](https://discord.com/channels/1120162219502608426/1233993910817259663 "#public-website-contribution Discord Forum Kanalı"){:target="_blank"} yeni bir gönderi oluşturacak veya içerik veya sorun zaten ele alınmaya başlanmışsa çalışmak üzere mevcut bir gönderiye yönlendirecektir.

Çalışmaya başladığınızda, şunlardan birini seçebilirsiniz:

1. Github'ta depoyu forklayın ve work'in kabul edilmesi için pull request gönderin (daha programlama bilginiz varsa)
2. Google Docs veya Notion gibi alternatif bir platformda çalışın ve bittiğinde bir iç katkıda bulunanın web sitesine port etmesine izin verin

## Katkıda Bulunmak için Github ve VS Code Kurma

### Önkoşulları Yükleyin
İşletim sisteminiz için doğru sürümleri indirdiğinizden emin olun (Windows, Mac veya Linux).

Windows yükleyicileri neredeyse her zaman 64-bit sürüm olmalıdır, bir ayrım varsa.

- En son [Git Bash](https://git-scm.com/downloads "Git Bash İndirme"){:target="_blank"} sürümü
    - İşletim sisteminiz için talimatları izleyin
    - Kurulum için tüm varsayılan seçenekleri kullanın
- [Python 3.10.6](https://www.python.org/downloads/release/python-3106/ "Python 3.10.6 İndirme"){:target="_blank"}
    - Yükleyici açıldığında, alttaki "Python 3.10'u PATH'e ekle" yi seçin ve "Şimdi Yükle" ye tıklayın
    - Windows kullanıcıları için, sonunda PATH uzunluğu sınırlamasını devre dışı bırakma seçeneğiniz vardır; bu diğer projeler için yardımcı olabilir ancak web sitesine katkıda bulunmak için gerekli değildir
- [VSCode](https://code.visualstudio.com/ "VSCode"){:target="_blank"}
    - İşletim sisteminiz için kararlı derlemeyi indirin
    - İsterseniz masaüstü simgesi oluşturma dışında tüm varsayılan seçenekleri kullanarak kurulum yapın
- [GitHub Desktop](https://desktop.github.com/ "Github Desktop") (İsteğe bağlı - VSCode'daki git arayüzünü de kullanabilirsiniz)
    - Yükledikten sonra, "GitHub.com'da Oturum Aç" ı seçin
    - Oturum açın veya yeni bir GitHub hesabı oluşturun, ardından "Masaüstünü Yetkilendir" e tıklayın
        - Kaydolmayı seçerseniz, kaydın sonunda bir captcha ile hesabınızı doğrulamanız ve e-postalı bir kod gerekir
        - Captcha başarısız olursa, müdahale eden bir gizlilik uzantısını devre dışı bırakmayı deneyin
        - Hesabınızın geri kalanını ayarlayın (GitHub eğitim için kaydolmayı seçebilirsiniz ancak bu gerekli değildir, ücretsiz sürüm iyidir)
        - Sizi yetkilendirme sayfasına götürmezse, GitHub Desktop uygulamasına geri dönün, "İptal" e basın, ardından tekrar "GitHub.com'da Oturum Aç" ı seçin
    - Tarayıcınızın GitHub Desktop'ı açmasına izin verin
    - "Bitir" e tıklayın


### Yazmak İçin Adımlar

**Halka Açık Katkıda Bulunanlar İçin:**

1. [Depo web sitesine](https://github.com/davidsdesignserver/FRCDesign.org "FRC Design Github Deposu"){:target="_blank"} gidin
2. Sağ üstte "Fork" a tıklayın, ardından bir sonraki ekranda "Fork Oluştur" a tıklayın
3. GitHub Desktop'ı açın ve "İnternet'ten bir depo klonla..." seçeneğini seçin veya en sol üstte ```dosya -> deponu klonla...``` seçeneğine gidin
4. "GitHub.com" altında, fork edilmiş ```[kullanıcı adı]/FRCDesign.org``` depoyu seçin ve "Klonla" ya tıklayın
5. Depoyu klonladıktan sonra (bilgisayarınıza bir kopyasını indirir), nasıl kullanmayı planladığınızı soracaktır. "Ana projeye katkıda bulunmak için" seçeneğini seçin ve "Devam Et" e tıklayın

**İç Katkıda Bulunanlar İçin (ana depoya eklenenler):**

1. GitHub Desktop'ı açın ve "İnternet'ten bir depo klonla..." seçeneğini seçin veya en sol üstte ```dosya -> deponu klonla...``` seçeneğine gidin
2. "GitHub.com" altında, ```davidsdesignserver/FRCDesign.org``` deposunu seçin ve "Klonla" ya tıklayın
3. Depoyu klonladıktan sonra (bilgisayarınıza bir kopyasını indirir), nasıl kullanmayı planladığınızı soracaktır. "Ana projeye katkıda bulunmak için" seçeneğini seçin ve "Devam Et" e tıklayın

**Yazmak ve Pull Request Katkıda Bulunma Nasıl Yapılır**

1. GitHub Desktop'ın üstündeki "Mevcut dal" açılır menüsüne giderek, "Yeni dal" a basarak, adlandırarak ve "Dal oluştur" a tıklayarak yeni bir dal oluşturun.
    - Genellikle değişiklikleri dallerde (main değil) yapmalısınız, ardından değişikliklerin "pulled" ve ana dal ile birleştirilmesi için "pull request" denilen şeyi yapmalısınız
    - Dalı yaptığınız değişikliklerle ilgili bir şey olarak adlandırın, örneğin "contributors-guide" veya "3A-cleanup". Pull request'ten sonra dalı silmeyi beklemelisiniz, bu yüzden değişikliklerinize yeterince özgün tutun
    - Yeni bir dal oluşturduktan sonra sonra gösteren butona tıklayarak dalı yayınlayın
2. VS Code'u açmak için "Visual Studio Code'da Aç" a tıklayın.
3. "Bu klasördeki dosyaların yazarlarına güveniyor musunuz?" diyen bir açılır pencere alırsanız, ana klasör 'GitHub'ın tüm dosyalarına güven onay kutusunu işaretleyin (gelecekte depoları klonlarken başka açılır pencereler olmaz) ve "Evet, yazarlara güveniyorum" a tıklayın.
4. İlk kez çalıştırıyorsanız VS Code'u nasıl isterseniz ayarlayın (temalar, uzantılar).
    - "Code Spell Checker" uzantısı önerilir
    - ```dosya``` menüsünde otomatik kaydı etkinleştirin
5. Bir dizi değişiklik yapın.

    !!! ipucu
        Tüm web sitesi dosyaları ve klasörleri ```docs``` klasöründedir, web sitesinin kenar çubuğu için dizini içeren ```mkdocs.yml``` dosyası hariç

6. Değişikliklerinizi buluta kaydetmek istediğiniz durdurmak için iyi bir noktaya ulaştığınızda, değişikliklerinin dala kaydedildiği bir "commit" yapmak istersiniz, ardından commit'leri buluta yüklemek için "push" yapmanız gerekir, aksi takdirde yerel olarak kalırlar. Bunu VS Code veya GitHub Desktop aracılığıyla yapabilirsiniz, ancak tüm sürüm kontrol eylemlerini orada merkezi olarak tutmak için GitHub Desktop üzerinden geçeceğiz.
7. GitHub Desktop'ı açın ve kenar çubuğundaki "Değişiklikler" in seçildiğinden emin olun. Kenar çubuğunda seçilen tüm değişiklikler commit'e eklenecektir (değişiklikler commit için "hazırlanır"). Commit için bir özet açıklaması yazın (açıklama isteğe bağlı) ve "Commit to [dal]" a basın.
8. Yaptığınız commit'leri buluta itmek için butona tıklayın (ya yukarıda ya da ekranın ortasında).

    !!! ipucu
        "Fetch origin" butonunu tıklamak, başkaları tarafından yapılıp buluta itilen geçerli dala herhangi bir commit'i getirir

9. Kodunuzu orijinal deponun ana dali ile güncel tutmak için, ekranın üstündeki "dal" menüsünü açın ve "main'den güncelle" ye tıklayın. Main'den dalınıza bazı commit'ler çekilirse, dalınızı bulutta tekrar güncelleyebilirsiniz.

    !!! ipucu
        Dalınızı main'den sık sık güncelleyin! Yapmazsanız, değişiklikleriniz ve başkasının main'e yaptığı değişiklikler arasında büyük çakışmaları çözmeniz gerekebilir. Çakışmalarla karşılaşırsanız, GitHub Desktop'taki istemleri izleyerek çakışmaları VS Code'da açın ve orada çözün. Tüm çakışmalar çözüldüğünde, birleştirmeyi tamamlamak için GitHub Desktop'a geri dönün.

10. Değişikliklerinizi ana web sitesine eklemeyi talep etmek için yeterince memnun kaldığınızda ve tüm değişiklikleri commit ettiyseniz, güncellemeleri kontrol ettiyseniz ve tüm commit'leri push ettiyseniz, GitHub Desktop'ın ortasındaki menü aracılığıyla bir pull request oluşturun. Bu sizi web sitesine götürür, burada yaptığınız değişiklikleri ve web sitesine çekmek istediğinizi açıklayabilirsiniz ve düzelteceği bir sorunu atayabilirsiniz. Bir iç katkıda bulunan pull request'inizi gönderdikten sonra gözden geçirecek ve ya ana dal ile birleştirecek ve onaylayacak veya birleştirilebilmesi için düzeltilmesi gereken şeyler hakkında yorum yapacaktır.

Katkı adımlarını özetlemek için, dal oluşturma ve yayınlama, değişiklik yapma ve commit'ler, main'den güncelleme, commit'leri push'leme ve bir pull request oluşturma kombinasyonunu yapın.


### Web Sitesinin Yerel Önizlemesini Nasıl Alırsınız
Düzenlerken sitede canlı bir önizleme olması için yerel olarak barındırılan bir web sitesi sürümünü alabilirsiniz.

1. VS Code'da depoyu açın (hangi dal olduğu önemli değil)
2. Alt panel yoksa ```Ctrl + J``` kısayoluyla açın
3. Alt panelin sağ üst köşesindeki + yanındaki açılır menüye tıklayın ve "Git Bash" e tıklayın
4. Sanal ortam oluşturmak için ```py -m venv venv``` komutunu çalıştırın (İLK KEZ)
5. Gerekli tüm python paketlerini yüklemek için ```./installdependencies.sh``` komutunu çalıştırın (İLK KEZ)
6. Sunucuyu başlatmak için ```./runlocal.sh``` komutunu çalıştırın
7. Her şey yolunda giderse "Serving on" şeklinde bir şey söyleyecektir, örneğin ```http://127.0.0.1:8000```

Düzenlemek için VS Code'u her açtığınızda ```./runlocal.sh``` komutunu Git Bash'te çalıştırdığınızdan emin olun.

!!! İpucu
    Alt paneldeki terminali tıkladıktan sonra, Ctrl + C kullanarak yerel web sitesi barındırmayı sonlandırabilirsiniz.

!!! Not
    GitHub Desktop kullanarak dalları değiştirdiğinizde, yerel önizleme herhangi bir sorun olmadan takip edecektir

