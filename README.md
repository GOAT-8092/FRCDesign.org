# Katkıda Bulunma Yöntemleri

## Herkese Açık Katkı
Herkes markdown bilgisi veya github olmadan web sitesi için içerik oluşturabilir, ancak diğer katkıda bulunanların iş yükünü azaltmak için her ikisini de öğrenmeniz tercih edilir

[Discord sunucusunda](https://discord.gg/qdx7pdZKx4), ["website-feedback" kanalına](https://discord.com/channels/1120162219502608426/1233961750639018104) gidin ve bu şablonu doldurarak katkıda bulunmak istediğiniz şeyi sorabilirsiniz:

    Soru/içerik:
    Çözüm veya içeriğin uygulanması hakkında notlar:
    Ne zaman bitirmeyi planlıyorsunuz?:
    Github'ta çatallama mı yoksa alternatif bir platform mu kullanıyorsunuz?:

Bu, zamanınızı boşa harcamamanız içindir - web sitesine eklenmeyecek bir şey üzerinde çalışmaya başlamayın veya başka biri zaten çalışmaya başlamış bir şey üzerinde çalışmayın.

Çalışmaya başlamak için onay alırsanız, bir iç katkıda bulunan ["public-website-contribution" forum kanalında](https://discord.com/channels/1120162219502608426/1233993910817259663) yeni bir gönderi oluşturacaktır veya içerik veya sorun zaten ele alınmaya başlanmışsa mevcut bir gönderiyle çalışmanızı yönlendirecektir.

Çalışmanıza başladığınızda şunlardan birini seçebilirsiniz:

1. Github'ta depoyu çatallayın (fork) ve çalışmanızın kabul edilmesi için çekme istekleri (pull request) gönderin (daha fazla programlama bilgisiyseniz)
2. Google Docs veya Notion gibi alternatif bir platformda çalışın ve bittiğinde bir iç katkıda bulunanın web sitesine aktarmasını sağlayın

## Katkıda Bulunmak İçin Github ve VS Code Kurulumu
### Ön Koşulları Yükleyin
İşletim sisteminiz için doğru sürümleri indirdiğinizden emin olun (Windows, Mac veya Linux).

Windows yükleyicileri neredeyse her zaman bir ayrım varsa 64-bit sürüm olmalıdır.

- [Git Bash](https://git-scm.com/downloads)'in en son sürümü
    - İşletim sisteminiz için talimatları izleyin
    - Kurulum için tüm varsayılan seçenekleri kullanın
- [Python 3.10.6](https://www.python.org/downloads/release/python-3106/)
    - Yükleyici açıldığında, alt kısmında "Add Python 3.10 to PATH" seçeneğini işaretlediğinizden emin olun ve "Install Now" düğmesine tıklayın
    - Windows kullanıcıları için, sonunda PATH uzunluk sınırını devre dışı bırakma seçeneğiniz vardır; bu diğer projeler için yardımcı olabilir ama web sitesine katkıda bulunmak için gerekli değildir
- [VSCode](https://code.visualstudio.com/)
    - İşletim sisteminiz için kararlı yapıyı indirin
    - İsterseniz masaüstü simgesi oluşturmak hariç tüm varsayılan seçenekleri kullanın
- [GitHub Desktop](https://desktop.github.com/)
    - Yükledikten sonra "Sign in to GitHub.com" seçeneğini tıklayın
    - GitHub hesabınızla oturum açın veya yeni bir hesap kaydedin, ardından "Authorize Desktop" düğmesine tıklayın
        - Kaydolmayı seçerseniz, kayıt sonunda bir captcha ve e-postayla gönderilen bir kodla hesabınızı doğrulamanız gerekir
        - Captcha başarısız olursa, müdahale eden bir gizlilik uzantısını devre dışı bırakmayı deneyin
        - Hesabınızın geri kalanını ayarlayın (GitHub education için kaydolmayı seçebilirsiniz ancak bu gerekli değildir, ücretsiz sürüm uygundur)
        - Kaydolduktan sonra sizi yetkilendirme sayfasına götürmezse, GitHub Desktop uygulamasına geri dönün, "Cancel" düğmesine basın, ardından tekrar "Sign in to GitHub.com" seçeneğini tıklayın
    - Tarayıcınızın GitHub Desktop'ı açmasına izin verin
    - "Finish" düğmesine tıklayın


### Yazım Katkılarına Başlama Adımları

**Herkese Açık Katkıda Bulunanlar İçin:**

1. [Depo web sitesine](https://github.com/davidsdesignserver/dds-manual) gidin
2. Sağ üstteki "Fork" near the top right, then click "Create Fork" on the next screen
3. GitHub Desktop'ı açın ve "Clone a repository from the Internet..." seçeneğini tıklayın veya en üst soldaki ```file -> Clone repository...``` menüsüne gidin
4. "GitHub.com" altında, çatalladığınız ```[kullanıcı adı]/dds-manual``` deposunu seçin ve "Clone" düğmesine tıklayın
5. Depo klonlandıktanında (bilgisayarınıza bir kopyasını indirir), size çatallamayı nasıl kullanmayı planladığınızı soracaktır. "To contribute to the parent project" seçeneğini seçin ve "Continue" düğmesine tıklayın

**İç Katkıda Bulunanlar İçin (ana depoya eklenenler):**

1. GitHub Desktop'ı açın ve "Clone a repository from the Internet..." seçeneğini tıklayın veya en üst soldaki ```file -> Clone repository...``` menüsüne gidin
2. "GitHub.com" altında ```davidsdesignserver/dds-manual``` deposunu seçin ve "Clone" düğmesine tıklayın
3. Depo klonlandıktan sonra (bilgisayarınıza bir kopyasını indirir), size çatallamayı nasıl kullanmayı planladığınızı soracaktır. "To contribute to the parent project" seçeneğini seçin ve "Continue" düğmesine tıklayın

**Katkıları Yazma ve Çekme İsteği Oluşturma**

1. GitHub Desktop'ın üst kısmındaki "Current branch" açılır menüsüne gidin, "New branch" düğmesine basın, adlandırın ve "Create branch" düğmesine tıklayarak yeni bir dal oluşturun.
    - Genellikle değişiklikleri ana dalda (main) değil dallarda yaparsınız, ardından değişikliklerinizi orijinal ana dala "çekilmesini" sağlamak için "pull request" (çekme isteği) adı verilen bir işlem yaparsınız
    - Dalı yaptığınız genel değişikliklerle ilgili bir şey gibi adlandırın, örneğin "contributors-guide" veya "3A-cleanup". Bir çekme isteğinden sonra dalı silmeyi beklemelisiniz, bu yüzden değişikliklerinize yeterince özgün tutun
    - Yeni bir dal oluşturduktan sonra sonra çıkan düğmeye tıklayarak dalı yayınlayın (publish)
2. VS Code'u açmak için "Open in Visual Studio Code" düğmesine tıklayın.
3. "Klasörün üst klasöründeki dosyaların yazarlarına güveniyor musunuz?" gibi bir açılır pencere alırsanız, "Trust the authors of all files in the parent folder 'GitHub" onay kutusunu işaretleyin (gelecekte depo klonlarken başka açılır pencereler olmaması için) ve "Yes, I trust the authors" düğmesine tıklayın.
4. İlk kez çalıştırıyorsanız VS Code'u nasıl isterseniz ayarlayın (temalar, uzantılar).
    - "Code Spell Checker" uzantısı önerilir
    - ```file``` menüsünde otomatik kaydı açmak için değiştirin
5. Bir dizi değişiklik yapın.
    - Tüm web sitesi dosyaları ve klasörleri ```docs``` klasöründedir, ```mkdocs.yml``` dosyası hariç ki web sitesinin kenar çubuğu için dizini içerir

6. Bulutunuza değişiklikleri kaydetmek için uygun bir durma noktasına her ulaştığınızda "commit" (işleme) adı verilen bir işlem yapmanız gerekir, bu işlemde değişiklikler dala kaydedilir. Ardından işleme işlemlerini buluta yüklemek için "push" (itme) yapmanız gerekir, aksi takdirde yerel olarak kalırlar. Bunu VS Code veya GitHub Desktop üzerinden yapabilirsiniz, ancak tüm sürüm kontrol eylemlerini tek bir yerde toplamak için GitHub Desktop üzerinden geçeceğiz.
7. Github Desktop'ı açın ve kenar çubuğunda "Changes" seçeneğinin seçildiğinden emin olun. Kenar çubuğunda seçilen tüm değişiklikler işleme için eklenecektir (değişiklikler işleme için "hazırlanır"). İşleme için bir özet girin (açıklama isteğe bağlı) ve "Commit to [branch]" düğmesine basın.
8. Yaptığınız işlemeleri buluta itmek için ekrandaki düğmeye tıklayın (yukarıda veya ekranın ortasında).
    - "Fetch origin" düğmesine tıklamak, başkaları tarafından yapılan ve buluta itilen geçerli daldaki tüm işlemleri getirir

9. Kodunuzu orijinal deponun ana dalıyla güncel tutmak için ekranın üst kısmındaki "branch" menüsünü açın ve "Update from main" düğmesine tıklayın. Ana daldan bazı işlemler dalınıza çekilirse, dalınızı bulutta tekrar güncellemek için tekrar itebilirsiniz.
    - Dalınızı ana daldan sık sık güncelleyin! Yapmazsanız, değişiklikleriniz ve başkasının ana dala yaptığı değişiklikler arasında büyük çakışmaları çözmeniz gerekebilir. Çakışmalarla karşılaşırsanız, GitHub Desktop'taki istemleri izleyerek çakışmaları VS Code'de açın ve orada çözün. Tüm çakışmalar çözüldüğünde, birleşmeyi tamamlamak için GitHub Desktop'a geri dönün.

10. Web sitesine eklenmesini istediğiniz değişiklik setinden yeterince memnun kaldığınızda ve tüm değişiklikleri işlediğinizde, güncellemeleri kontrol ettiğinizde ve tüm işlemleri ittiğinizde, GitHub Desktop'ın ortasındaki menüden bir çekme isteği (pull request) oluşturun. Bu sizi web sitesine götürecektir, orada yaptığınız değişiklikleri ve web sitesine çekmek istediklerinizi tanımlayabilir ve çözeceği bir sorunu atayabilirsiniz. Çekme isteğinizi gönderdikten sonra bir iç katkıda bulunan inceleyecek ve ya ana dalla birleştirecek veya birleştirilmeden önce düzeltilmesi gereken şeyler hakkında yorum yapacaktır.

Katkı adımlarını özetlemek için, dal oluşturma ve yayınlama, değişiklikleri ve işleme yapma, ana daldan güncelleme, işleme itme ve çekme isteği oluşturma kombinasyonunu yapın.


### Web Sitesinin Yerel Önizlemesini Çalıştırma
Web sitesinin yerel barındırılan bir sürümünü edinirken düzenlerken canlı önizleme alabilirsiniz.

1. Depoyu VS Code'da açın (hangi dal olduğu önemli değil)
2. Alt panel yoksa ```Ctrl + J``` kısayolu ile açın
3. Alt panelin sağ üst köşesindeki + yanındaki açılır menüyü tıklayın ve "Git Bash" seçeneğini tıklayın
4. Bir sanal ortam oluşturmak için ```python -m venv venv``` komutunu çalıştırın (İLK SEFER)
5. Gerekli tüm python paketlerini yüklemek için ```./installdependencies.sh``` komutunu çalıştırın (İLK SEFER)
6. Sunucuyu başlatmak için ```./runlocal.sh``` komutunu çalıştırın
7. Her şey yolunda giderse "Serving on" bir şeyler söylemeli ```http://127.0.0.1:8000```

Düzenlemek için VS Code'u her açtığınızda Git Bash'de ```./runlocal.sh``` çalıştırdığınızdan emin olun.

İpucu: Alt paneldeki terminale tıkladıktan sonra Ctrl + C tuşlarını kullanarak yerel web sitesi barındırmayı sonlandırabilirsiniz.

Not: GitHub Desktop kullanarak dallar arasında geçiş yaptığınızda yerel önizleme herhangi bir sorun olmadan takip edecektir
