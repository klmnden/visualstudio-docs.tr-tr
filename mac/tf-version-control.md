---
title: Team Foundation sürüm denetimi (TFVC)
description: Mac için Visual Studio Team Foundation sürüm denetimi (TFVC) ile Team Foundation Server/Azure DevOps bağlanıyor.
author: conceptdev
ms.author: crdun
ms.date: 04/04/2019
ms.topic: article
ms.technology: vs-ide-general
ms.assetid: 52D3D26A-4D01-4FD1-AAA1-AE7D7BD39746
ms.openlocfilehash: d98ffc8c9d864afaf0b42d029a4d65850f64d806
ms.sourcegitcommit: 0e22ead8234b2c4467bcd0dc047b4ac5fb39b977
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59366165"
---
# <a name="connecting-to-team-foundation-version-control"></a>Team Foundation sürüm denetimine bağlama

> [!NOTE]
> MacOS en iyi sürüm denetim deneyimi için Git, Team Foundation sürüm denetimi (TFVC) yerine kullanılmasını öneririz. Git Mac için Visual Studio'da desteklendiği ve Team Foundation Server (TFS) barındırılan depolar için varsayılan seçenek / Azure DevOps. Git, TFS/Azure DevOps ile kullanma hakkında daha fazla bilgi edinmek için [bir Git deposu ayarlama](/visualstudio/mac/set-up-git-repository) makalesi.

Azure depoları, sürüm denetimi, iki modeli sağlar: [Git](/azure/devops/repos/git/?view=azure-devops), bir dağıtılmış sürüm denetim sistemini ve [Team Foundation sürüm denetimi](/azure/devops/repos/tfvc/index?view=azure-devops) (TFVC) merkezi sürüm denetimi sistemi.

Mac için Visual Studio, Git depoları için tam destek sağlar, ancak TFVC ile çalışmak için bazı geçici çözümler gerektirir. Bugün sürüm denetimi için TFVC kullanıyorsanız, kaynak kodunuzu TFVC'de barındırılan erişmek için kullanabileceğiniz bazı çözümler aşağıda verilmiştir.

* [Visual Studio Code ve Azure depoları uzantısı için bir grafik kullanıcı Arabirimi kullanın.](#use-visual-studio-code-and-the-azure-repos-extension)
* [Team Explorer Everywhere komut satırı istemcisini (CLC TEE) kullanarak deponuza bağlanma](#connecting-using-the-team-explorer-everywhere-command-line-client)
* [TFVC (desteklenmeyen) Team Foundation sürüm denetimi uzantısı için Mac için Visual Studio kullanarak bağlanma](#connect-to-tfvc-using-the-team-foundation-version-control-extension)

Bu makalenin geri kalanında, yukarıda listelenen seçenekler açıklanmaktadır.

## <a name="requirements"></a>Gereksinimler

* Visual Studio Community, Professional veya Enterprise Mac 7,8 veya sonraki bir sürümü için.
* Azure DevOps Hizmetleri, Team Foundation Server 2013 ve üzeri ya da Azure DevOps sunucu 2018 ve üzeri.
* Azure DevOps Services veya Team Foundation Server/Azure DevOps Team Foundation sürüm denetimi kullanmak üzere yapılandırılmış sunucusu, bir proje.

## <a name="use-visual-studio-code-and-the-azure-repos-extension"></a>Visual Studio Code ve Azure depoları uzantısını kullanma

Sürüm denetiminde dosyalarınızı yönetmek için bir grafik arabirim çalışmak istiyorsanız, Visual Studio Code için Azure depoları uzantısı Microsoft tarafından desteklenen bir çözüm sağlar. Başlamak için Yükle [Visual Studio Code](https://code.visualstudio.com) ve daha sonra öğrenin nasıl [Azure depoları uzantısını yapılandırmak](https://marketplace.visualstudio.com/items?itemName=ms-vsts.team).

## <a name="connecting-using-the-team-explorer-everywhere-command-line-client"></a>Team Explorer Everywhere komut satırı istemcisini kullanarak bağlanma

MacOS Terminal, ardından Team Explorer Everywhere komut satırı istemcisini kullanarak hakimseniz (TEE CLC) TFVC kaynak bağlanmak için desteklenen bir yol sağlar.

TFVC ve değişiklikleri bağlantınızı kurmak için aşağıdaki adımları izleyebilirsiniz.

Chris Pilcher, bir geliştirici topluluğumuzdaki uzmanlarımız sayesinde özel olan [TEE CLC için özgün yönergeleri](https://gist.github.com/chris-pilcher/a3f14eb081d7ab983e5c) Bu bölümde temel.

### <a name="setting-up-the-tee-clc"></a>TEE CLC ayarlama

TEE CLC kuruluma almanın iki yolu vardır.

* İstemcisini yüklemek için Homebrew kullanın veya
* İstemcisini indirme ve el ile yükleme

En kolay çözümdür **HomeBrew kullanarak**, macOS için Paket Yöneticisi olan. Bu yöntemi kullanarak yüklemek için:

1. MacOS Terminal uygulamasını başlatın.
1. Terminal ve yönergeleri kullanarak Homebrew yükleme [Homebrew giriş sayfası](https://brew.sh/).
1. Homebrew yüklendikten sonra terminalde aşağıdaki komutu çalıştırın: `brew install tee-clc`

İçin **TEE CLC el ile Kurulum**:

1. [Tee clc en son sürümünü indirin](https://github.com/Microsoft/team-explorer-everywhere/releases) sürümleri sayfasından Team Explorer Everywhere GitHub deposunun (örn: t-clc-14.134.0.zip bu makalenin yazıldığı sırada).
1. Diskteki bir klasöre .zip içeriğini ayıklayın.
1. MacOS Terminal uygulamasını açın ve kullanmak `cd` önceki adımda kullanılan klasöre değiştirmek için komutu.
1. Klasör içinde çalıştırılan komut `./tf` komut satırı istemci çalıştırabileceğiniz test etmek için Java veya diğer bağımlılıkları yüklemeniz istenebilir.

TEE CLC yüklendikten sonra komutu çalıştırabilirsiniz `tf eula` görüntülemek ve istemcisi için lisans sözleşmesini kabul edin.

Son olarak, TFS/Azure DevOps ortamınız ile kimlik doğrulamak için sunucuda bir kişisel erişim belirteci oluşturma gerekecektir. Daha fazla bilgi edinin [kişisel erişim belirteçleri ile kimlik doğrulaması](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/pats?view=azure-devops). TFVC ile kullanmak için kişisel erişim belirteci oluştururken, belirteç yapılandırırken tam erişim sağlamak üzere emin olun.

### <a name="using-the-tee-clc-to-connect-to-your-repo"></a>TEE CLC kullanarak deponuza bağlanma

Kaynak kodunuzu bağlanmak için önce kullanarak bir çalışma alanı oluşturmak için ihtiyacınız `tf workspace` komutu. Örneğin, aşağıdaki komutları bir kuruluşta Azure DevOps "MyOrganization" olarak adlandırılan hizmetleri bağlanın: 

```bash
export TF_AUTO_SAVE_CREDENTIALS=1
tf workspace -new MyWorkspace -collection:https://dev.azure.com/MyOrganization
```

`TF_AUTO_SAVE_CREDENTIALS` Ortam ayarını, bunları birden çok kez girmeniz istenmez böylece kimlik bilgilerinizi kaydetmek için kullanılır. Bir kullanıcı adı için istendiğinde, önceki bölümde oluşturduğunuz kişisel erişim belirteci kullanın ve boş bir parola kullanın.

Şimdi kaynak dosyalarını yerel bir klasöre ilişkin bir eşleme oluşturmak için kullanacağınız `tf workfold` komutu. Aşağıdaki örnek "MyRepository" TFVC gelen "WebApp.Services" adlı bir klasör eşler proje ve yerel ~/Projects/ klasörüne (yani "Projeler" klasöründeki bir klasörün geçerli kullanıcı giriş) kopyalanacak ayarlayın.

```bash
tf workfold -map $/MyRepository/WebApp.Services -workspace:MyWorkspace ~/Projects/
```

Son olarak, kaynak dosyaları sunucudan almak ve yerel olarak kopyalamak için aşağıdaki komutu kullanın:

```bash
tf get
```

### <a name="committing-changes-using-the-tee-clc"></a>TEE CLC kullanarak değişiklikler işleniyor

Mac için Visual Studio dosyalarında değişiklik yaptıktan sonra yaptığınız düzenlemeleri denetlemek için Terminal geri dönebilirsiniz. `tf add` Komut dosyaları bekleyen değişiklikler iade edilecek listesine eklemek için kullanılır ve `tf checkin` gerçek iade sunucuya komutu gerçekleştirir. `checkin` Komut yorum ekleyebilir ya da bir ilgili iş öğesini ilişkilendirmek için parametreleri içerir. Aşağıdaki kod parçacığında, tüm dosyaları bir `WebApp.Services` klasör eklenir, yinelemeli olarak iade etme için. Ardından, kod bir yorum ile işaretli ve "42" Kimliğine sahip bir iş öğesi ile ilişkilendirilmiş.

```bash
cd WebApp.Services
tf add * /recursive
tf checkin -comment:"Replaced 'Northwand' typos with the correct word Northwind" -associate:42
```

Burada belirtilen komutları veya diğerleri hakkında daha fazla bilgi için terminalde aşağıdaki komutu kullanabilirsiniz:

`tf help`

## <a name="connect-to-tfvc-using-the-team-foundation-version-control-extension"></a>Team Foundation sürüm denetimi uzantısını kullanarak TFVC için Bağlan

> [!NOTE]
> MacOS en iyi sürüm denetim deneyimi için Git, Team Foundation sürüm denetimi (TFVC) yerine kullanılmasını öneririz. Git Mac için Visual Studio'da desteklendiği ve Team Foundation Server (TFS) barındırılan depolar için varsayılan seçenek / Azure DevOps. Git, TFS/Azure DevOps ile kullanma hakkında daha fazla bilgi edinmek için [bir Git deposu ayarlama](/visualstudio/mac/set-up-git-repository) makalesi.

Mac uzantı Galerisi için Visual Studio için TFVC bağlanmak için sınırlı destek sağlayan bir Team Foundation sürüm denetim uzantısı yok. Uzantı desteklenmiyor ve deneyiminizi kullanırken değişebilir. Bu nedenle bazı bilinen sorunlar vardır.

Uzantıyı yüklemek için Mac için Visual Studio'yu başlatın ve seçin **Visual Studio > Uzantılar** menüsü. İçinde **galeri** sekmesinde **sürüm denetimi > Team Foundation sürüm denetimi, TFS ve Azure DevOps için** tıklatıp **yükle...** :

![Uzantı Yöneticisi](media/tfvc-install.png)

Uzantıyı yüklemek için istemleri izleyin. Yüklendikten sonra IDE yeniden başlatın.

### <a name="updating-the-extension"></a>Uzantıyı güncelleştirirken

TFVC uzantı güncelleştirmeleri düzenli olarak gerçekleştirilir. Güncelleştirmeleri erişmek, seçin **Visual Studio > uzantılar...**  seçin ve menüden **güncelleştirmeleri** sekmesi. Uzantı listesi ve ENTER tuşuna seçin **güncelleştirme** düğmesi:

Tuşuna **yükleme** sonraki iletişim kutusunda eski paketi kaldırın ve yenisini yükleyin.

### <a name="using-the-extension"></a>Uzantısını kullanma

Uzantıyı yükledikten sonra seçin **sürüm denetimi > TFS/Azure DevOps > Uzak depodan Aç...**  menü öğesi.

![Uzantı açmak için menü öğesi](media/tfvc-source-control-explorer-devops.png)

VSTS veya Team Foundation Server kullanmaya başlayın ve basın seçin **devam**:

![Bir sunucuyla bağlanma](media/tfvc-choose-server-type-devops.png)

#### <a name="azure-repos-authentication"></a>Azure depoları kimlik doğrulaması

Azure depoları üzerinde barındırılan bir proje seçtiğinizde, Microsoft hesabı ayrıntılarını girin istenir:

![Azure depoları ile bağlanma](media/tfvc-vsts-login.png)

#### <a name="tfs-authentication"></a>TFS kimlik doğrulaması

TFS'ye bağlanmak için sunucu ayrıntıları ve hesap kimlik bilgilerinizi girin. Aksi takdirde temel kimlik doğrulaması kullanmak için boş bırakın, NTLM kimlik doğrulaması kullanmak için bir etki alanını girin. Seçin **sunucusu ekleme**:

![Bir TFS sunucusuna oturum açın](media/tfvc-login.png)

### <a name="selecting-a-project"></a>Bir proje seçme

Başarıyla kimlik doğrulaması yaptınız sonra hesabı ile ilişkili olan depolar listesini görebilirsiniz **kaynak denetiminden Aç** iletişim:

![Kaynak denetimi iletişim kutusunda görüntülenen projeleri ile Aç](media/tfvc-vsts-projects.png)

Bu iletişim kutusunda, aşağıdaki düğümleri düzenlenmiştir:

- Azure DevOps kuruluş veya koleksiyon – Bu, oturum açtığınız Microsoft hesabı bağlı tüm organizasyonlar görüntüler.
- Her Kuruluş ve koleksiyon - projeleri projelerinin sayısına sahip olabilir. Kaynak kodu, iş öğeleri ve otomatik yapılara barındırıldığı bir projedir.

Bu noktada, arama filtre ve bir proje veya kuruluş adına göre.

#### <a name="adding-a-new-server"></a>Yeni bir sunucu ekleme

Listeye yeni bir sunucu eklemek için basın **konak Ekle** düğmesini **kaynak denetiminden Aç** iletişim:

![Vurgulanmış yeni sunucu listesine eklemek için düğme ekleme](media/tfvc-add-new-server.png)

Listeden sağlayıcıyı seçin ve kimlik bilgilerinizi girin:

![Kaynak denetimi sağlayıcısı için seçeneğini gösteren iletişim](media/tfvc-add-new-creds-devops.png)

### <a name="creating-a-new-workspace"></a>Yeni bir çalışma alanı oluşturma

Bir proje ile çalışmaya başlamak için ihtiyacınız bir _çalışma_. Bir çalışma alanı yoksa, bir oluşturabilirsiniz **çalışma** combobox içinde **kaynak denetiminden Aç** iletişim:

![Yeni çalışma alanı combobox seçenek oluştur](media/tfvc-create-new-workspace.png)

Yeni bir çalışma alanınız için yerel yolunu ve adını ayarlar ve **çalışma alanı oluştur**:

![Yeni çalışma alanı için bir ad ve yerel yol girme](media/tfvc-local-workspace.png)

### <a name="using-the-source-code-explorer"></a>Kaynak kod Gezgini kullanma

Bir çalışma alanı oluşturup projenizi eşlenen ile çalışmaya başlayabilir _kaynak kod Gezgini_.

Kaynak kod gezginini açmak için seçmeniz **sürüm denetimi > TFS/Azure DevOps > Kaynak Denetim Gezgini** menü öğesi.

Kaynak kod Gezgini eşlenen tüm projeler, dosyalar ve klasörler gitmenizi sağlar. Ayrıca gibi tüm temel kaynak denetim eylemleri gerçekleştirmenize olanak sağlar:

- En son sürümü Al
- Belirli Sürümü Al
- Dosyaları kullanıma alma ve iade etme
- Kilitleme ve dosyaları kilidini açma
- Ekleme, silme ve dosyaları yeniden adlandırma
- Geçmişi görüntüle
- Değişiklikleri Karşılaştır.

Bu eylemlerin çoğunu, projenin bağlam eylemleri aracılığıyla sunulur:

![Bir proje için bağlam menüsünü eylemleri](media/tfvc-sourcecode-actions.png)

### <a name="managing-workspaces"></a>Çalışma alanlarını yönetme

Açıklandığı zaten bir çalışma alanı oluşturmadıysanız, [çalışma alanı oluşturma](#creating-a-new-workspace) bölümünde seçeneğinde kaynak kod Gezgini boştur:

![boş bir kaynak kod Gezgini](media/tfvc-setup-empty-sce.png)

Uzak bir yerel çalışma alanı projenizle ayarlamak için aşağıdaki adımları kullanın:

1. Seçin **sunucu** Açılır kutudan.
1. Yerel yol "Eşlenmemiş" ise ve "çalışma alanı" olduğunu unutmayın. Seçin **eşlenmedi** görüntülemek için bağlantıyı **yeni çalışma alanı oluşturma** iletişim.
1. Çalışma alanı için bir ad belirtin ve ardından **çalışma klasörü Ekle** bilgisayarınızdaki bir yerel klasör proje eşlemek için:

    ![Varsayılan seçenekleri gösteren yeni bir çalışma alanı iletişim kutusu oluşturma](media/tfvc-workspace1.png)

1. Sunucunuzdaki tüm projeleri aynı çalışma alanına eşleme her bir proje seçin veya tıklayın "$" klasörü seçin **Tamam**:

    ![Tüm projeler gösteren klasör iletişim kutusu için Gözat](media/tfvc-workspace2.png)

1. Yerel makinenizde ve projeleri için harita tıklayın istediğiniz konumu seçin **Klasör Seç**.
1. Yeni çalışma alanı ayrıntılarını tuşlarına basarak onaylayın **Tamam**

    ![Eklenen çalışma klasörü ile yeni çalışma alanı iletişim kutusu oluşturma](media/tfvc-workspace3.png)

Çalışma alanınızı ayarladıktan sonra onu değiştirilebilir ya tıklayarak kaldırıldı **çalışma alanlarını yönet** düğmesi kaynak kod gezginindedir.

![Çalışma alanlarını yönetme](media/tfvc-workspace4.png)

## <a name="troubleshooting-and-known-issues"></a>Sorun Giderme ve Bilinen Sorunlar

#### <a name="problems-using-basic-authentication"></a>Temel kimlik doğrulaması kullanma ile ilgili sorunlar

Bir sunucunun kimliğini doğrulamak için aşağıdaki seçenekler kullanılabilir:

- OAuth
- Temel
- NTLM

Bunu etkinleştirmek için gereken temel kimlik doğrulaması kullanacak şekilde **alternatif kimlik doğrulama bilgilerini** aşağıdaki adımları izleyerek Azure DevOps Hizmetleri:

1. Azure DevOps kuruluşunuza sahibi olarak oturum açın (https://dev.azure.com/{organization}/{project}).

2. Kuruluş, araç çubuğunda, dişli simgesini seçin ve seçin **ilke**:

    ![Seçili İlkesi ayarları seçeneği](media/tfvc-auth2.png)

3. Uygulama bağlantı ayarlarınızı gözden geçirin. Güvenlik ilkelerine bağlı olarak, bu ayarları değiştirin:

    ![Seçili İlkesi ayarları seçeneği](media/tfvc-auth.png)

#### <a name="i-do-not-see-anything-in-tfvc"></a>Tfvc'de herhangi bir şey göremiyorum

Geliştirme makinenizde Team Foundation sürüm denetimi (TFVC) kurmak ayarlamak için **gerekir** açıklandığı bir çalışma alanı oluşturma [çalışma alanlarını yönetme](#managing-workspaces) bölümü.

Kaynak denetimi Gezgini'nde basın **çalışma alanlarını yönet** düğmesi. Projenin geliştirme makinenizde bir klasörü eşlemek için adımları izleyin.

#### <a name="i-do-not-see-any--all-of-my-projects"></a>Göremiyorum / all, projelerim

Kimlik doğrulandıktan sonra projelerinin listesini görmeniz gerekir. Varsayılan olarak, yalnızca TFS projelerine gösterilmektedir. Diğer proje türleri görmek için "tüm projeleri bkz" kutusunu işaretleyin.

Doğru ayrıcalıklara sahip değilseniz, sunucu üzerinde olan projeler görünmez göz önünde bulundurun.

##### <a name="i-am-getting-the-error-cannot-create-the-workspace-please-try-again"></a>Hatası "çalışma alanı oluşturulamıyor. alıyorum Lütfen yeniden deneyin"

Çalışırken [yeni bir çalışma alanı oluşturma](#creating-a-new-workspace), aşağıdaki koşulların yerine getirildiğinden emin olmanız gerekir:

- Çalışma alanı adı geçersiz karakterler markaları kullanılamaz.
- Ad 64 karakterden kısa olmalıdır.
- Yerel yol diğer çalışma alanları tarafından kullanılamaz.

### <a name="see-also"></a>Ayrıca bkz.

- [Geliştirin ve kodunuzu Visual Studio (Windows üzerinde) kullanarak tfvc'de paylaşma](/azure/devops/repos/tfvc/share-your-code-in-tfvc-vs)