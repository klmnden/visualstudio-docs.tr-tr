---
title: Gelişmiş özellikler
ms.date: 06/01/2018
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 29f7f0a94939f06b74443ae08a2ef5b226a1e494
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70180364"
---
# <a name="features-of-visual-studio"></a>Visual Studio 'nun özellikleri

[Visual Studio IDE'ye genel bakış](../get-started/visual-studio-ide.md) makale, Visual Studio için temel bir giriş sağlar. Bu makalede, deneyimli geliştiriciler için daha uygun olabilecek özellikler veya Visual Studio 'Yu zaten bildiğiniz geliştiriciler açıklanmaktadır.

## <a name="modular-installation"></a>Modüler yükleme

Visual Studio 'nun modüler yükleyicisi, *iş yüklerini*seçmenizi ve yüklemenizi sağlar. İş yükleri, tercih ettiğiniz programlama dili veya platformu için gereken özellik gruplarıdır. Bu strateji, yükler ve çok daha hızlı güncelleştirmeler ayak izini daha küçük, Visual Studio yüklemesinin kalmasına yardımcı olur.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range=">=vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads) ücretsiz yüklemek için sayfa.

::: moniker-end

Visual Studio 'Yu sisteminizde ayarlama hakkında daha fazla bilgi edinmek için bkz. [Visual Studio 'Yu yüklemek](../install/install-visual-studio.md).

## <a name="create-cloud-enabled-apps-for-azure"></a>Azure için bulut özellikli uygulamalar oluşturma

Visual Studio takımının bir kolayca Microsoft Azure tarafından desteklenen bulut özellikli uygulamalar oluşturmanıza olanak sağlayan araçlar sunar. Yapılandırma, oluşturun, hata ayıklama, paket ve uygulamaları ve Hizmetleri doğrudan IDE üzerinden Microsoft Azure üzerinde dağıtın. Azure Araçları ve proje şablonları ulaşmak için **Azure geliştirme** Visual Studio'yu yüklediğinizde iş yükü.

![Azure geliştirme iş yükü](../data-tools/media/azure-development-workload.png)

::: moniker range="vs-2017"

Yükledikten sonra **Azure geliştirme** iş yükü, aşağıdaki **bulut** için C# şablonları kullanılabilir **yeni proje** iletişim:

![Bulut için Visual Studio Proje şablonları](media/cloud-project-templates.png)

::: moniker-end

Visual Studio'nun [Cloud Explorer](/azure/vs-azure-tools-resources-managing-with-cloud-explorer) görüntülemek ve Azure tabanlı bulut kaynaklarınızı Visual Studio içinden yönetmenize olanak sağlar. Bu kaynaklar sanal makineler, tablolar, SQL veritabanları ve daha fazlasını içerebilir. **Cloud Explorer** tüm hesapları Azure kaynakları yönetilen içine oturum Azure aboneliği altında gösterir. Ve Azure portalı, belirli bir işlemi gerektiriyorsa, **Cloud Explorer** portalında Git gereken yere yönlendiren bağlantılar sağlar.

![Visual Studio'daki bulut Gezgini'nde](media/cloud-explorer.png)

Azure hizmetlerini kullanarak uygulamalarınız için yararlanabileceğiniz **bağlı hizmetler** gibi:

- [Active Directory bağlı hizmetini](/azure/active-directory/develop/vs-active-directory-add-connected-service) kullanıcıların kendi hesapları kullanabilmeniz için [Azure Active Directory](/azure/active-directory/active-directory-whatis) web Apps'e bağlanmak için
- [Azure depolama bağlı hizmeti](/azure/vs-azure-tools-connected-services-storage) blob depolama, kuyruklar ve tablolar
- [Key Vault bağlı hizmeti](/azure/key-vault/vs-key-vault-add-connected-service) web uygulamaları için gizli verileri yönetmek için

Kullanılabilir **bağlı hizmetler** , proje türüne bağlıdır. Projeye sağ tıklayarak bir hizmet eklemek **Çözüm Gezgini** seçip **Ekle** > **bağlı hizmet**.

![Visual Studio bağlı hizmetler](media/connected-services.png)

Daha fazla bilgi için [ile Visual Studio ve Azure buluta taşıma](https://visualstudio.microsoft.com/vs/azure-tools/).

## <a name="create-apps-for-the-web"></a>Web için uygulamalar oluşturun

Modern Dünyamızı web sürücüleri ve Visual Studio için uygulamalar yazmanıza yardımcı olabilir. ASP.NET, Node.js, Python, JavaScript ve TypeScript kullanarak web uygulamaları oluşturabilirsiniz. Visual Studio gibi Açısal, jQuery, Express ve web çerçeveleri farkındadır. ASP.NET Core ve .NET Core Windows, Mac ve Linux işletim sistemleri üzerinde çalıştırın. [ASP.NET Core](http://www.asp.net/core/overview) MVC, Webapı ve SignalR önemli bir güncelleştirme ve Windows, Mac ve Linux üzerinde çalıştırır.  ASP.NET Core baştan ayarlama, yalın ve birleştirilebilir bir .NET ile modern bulut tabanlı web uygulamaları ve hizmetleri oluşturmak için yığın sağlamak için tasarlanmıştır.

Daha fazla bilgi için [Modern web araçları](https://visualstudio.microsoft.com/vs/modern-web-tooling/).

## <a name="build-cross-platform-apps-and-games"></a>Platformlar arası uygulamalar ve oyunlar oluşturun

Visual Studio, uygulamaları ve oyunları macOS, Linux ve Windows için yanı sıra Android, iOS ve diğer yapı için kullanabileceğiniz [mobil cihazları](https://visualstudio.microsoft.com/vs/mobile-app-development/).

- Derleme [.NET Core](/dotnet/core/) Windows, macOS ve Linux'ta çalışan uygulamalar.

- Windows, iOS ve Android için mobil uygulamalar oluşturmayı C# ve F# kullanarak [Xamarin](https://developer.xamarin.com/guides/cross-platform/windows/visual-studio/).

- Standart web teknolojileri kullanın&mdash;HTML, CSS ve JavaScript&mdash;kullanarak iOS, Android ve Windows için mobil uygulamalar oluşturmayı [Apache Cordova](/visualstudio/cross-platform/tools-for-cordova/).

- Kullanarak C# 2B ve 3B oyunlar oluşturun [Unity için Visual Studio Araçları](../cross-platform/visual-studio-tools-for-unity.md).

- İOS, C++ Android ve Windows cihazları için yerel uygulamalar oluşturun. [ C++ Platformlar arası geliştirme için](../cross-platform/visual-cpp-for-cross-platform-mobile-development.md)kullanarak iOS, Android ve Windows için oluşturulan kitaplıklarda ortak kod paylaşma.

- Dağıtın, test edin ve Android uygulamaları ile hata ayıklama [Android öykünücüsü](../cross-platform/visual-studio-emulator-for-android.md).

## <a name="connect-to-databases"></a>Veritabanlarına bağlanma

**Sunucu Gezgini** göz atın ve SQL Server örnekleri ve varlıkları yerel olarak, uzaktan ve Azure, Salesforce.com, Office 365 ve Web siteleri üzerinde yönetmenize yardımcı olur. Açmak için **Sunucu Gezgini**, ana menüsünde **görünümü** > **Sunucu Gezgini**. Sunucu Gezgini kullanma hakkında daha fazla bilgi için bkz. [yeni bağlantılar ekleme](../data-tools/add-new-connections.md).

[SQL Server veri Araçları (SSDT)](/sql/ssdt/download-sql-server-data-tools-ssdt) SQL Server, Azure SQL veritabanı ve Azure SQL veri ambarı için bir güçlü bir geliştirme ortamıdır. Derleme, hata ayıklama, korumak ve veritabanlarını yeniden düzenleme sağlar. Bir veritabanı projesiyle veya doğrudan ile bir bağlı veritabanı örneği veya kapalı-şirket içinde çalışabilir.

**SQL Server Nesne Gezgini** Visual Studio'da veritabanı nesnelerini SQL Server Management Studio'ya benzer bir görünüm sağlar. SQL Server Nesne Gezgini, açık hacimsiz veritabanı yönetimi ve tasarım işi yapmanızı sağlar. İş örnekleri, tablo verilerini düzenlemenizi, şemaları karşılaştırmayı, SQL Server Nesne Gezgini ' den çok bağlamsal menüler kullanarak sorguları yürütmeyi ve daha fazlasını içerir.

![SQL Server Object Explorer](../ide/media/vs2015_sqlobjectexplorer.png)

## <a name="debug-test-and-improve-your-code"></a>Hata ayıklama, test etme ve kodunuzu geliştirme

Kod yazmak, çalıştırmak ve hataları ve performans için test gerekir. Visual Studio'nun en son hata ayıklama sistem projenizdeki yerel veya uzak cihaz üzerinde çalışan kodda hata ayıklamak sağlayan bir [cihaz öykünücüsünü](../cross-platform/visual-studio-emulator-for-android.md). Aynı anda bir deyim kod adım adım ve kullandıkça değişkenleri denetleyin. Belirtilen bir koşul true olduğunda yalnızca isabet kesme noktaları ayarlayabilirsiniz. Hata ayıklama seçenekleri kod Düzenleyicisi 'nde yönetilebilir, böylece kodunuzda bırakmanız gerekmez. Visual Studio 'da hata ayıklama hakkında daha fazla bilgi edinmek için bkz. [hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md).

Visual Studio'nun kullanıma kullanıma alma uygulamalarınızın performansını iyileştirme hakkında daha fazla bilgi edinmek için [profil oluşturma](../profiling/profiling-feature-tour.md) özelliği.

İçin [test](../test/improve-code-quality.md), Visual Studio birim testi, Live Unit Testing, Intellitest, yük ve performans testi ve daha fazlasını sunar. Visual Studio Gelişmiş de [Kod Analizi](../code-quality/code-analysis-for-managed-code-overview.md) tasarım, güvenlik ve diğer türleri standartlarımızı yakalamak için özellikleri.

## <a name="deploy-your-finished-application"></a>Tamamlanmış uygulama dağıtma

Uygulamanız kullanıcılara veya müşterilere dağıtmaya hazırsa, Visual Studio bunu yapmak için gereken araçları sağlar. Dağıtım seçenekleri Microsoft Store, bir SharePoint sitesine veya InstallShield ya da Windows Installer teknolojilerine dahildir. Bu, tüm IDE erişilebilir. Daha fazla bilgi için [uygulamaları, hizmetleri ve bileşenleri dağıtma](../deployment/deploying-applications-services-and-components.md).

## <a name="manage-your-source-code-and-collaborate-with-others"></a>Kaynak kodunuzu yönetin ve başkalarıyla işbirliği yapın

GitHub dahil olmak üzere herhangi bir sağlayıcı tarafından barındırılan Git depolarındaki kaynak kodunuzu yönetebilirsiniz. Veya [Azure DevOps Hizmetleri](/azure/devops/index) hataların yanında kodu yönetmek ve iş öğelerinin projenizin tamamında. Bkz: [Azure depoları ve Git ile çalışmaya başlama](/azure/devops/repos/git/gitquickstart?tabs=visual-studio) Visual Studio'da Takım Gezgini'ni kullanarak Git depoları yönetme hakkında daha fazla bilgi edinmek için. Visual Studio'nun diğer yerleşik kaynak denetimi özellikleri de vardır. Bunlar hakkında daha fazla bilgi edinmek için bkz. [Visual Studio 'Da yeni git özellikleri (blog)](https://devblogs.microsoft.com/devops/new-git-features-in-visual-studio-2017/).

Azure DevOps Services, yazılımı planlamak, barındırmak, otomatikleştirmek ve dağıtmak ve ekiplerde işbirliği sağlamak için bulut tabanlı hizmetlerdir. Azure DevOps Services hem Git depoları (dağıtılmış sürüm denetimi) hem de Team Foundation Sürüm Denetimi (merkezi sürüm denetimi) destekler. Sürüm denetim sistemlerinde depolanan kodun sürekli derlemesi ve sürümü (CI/CD) için işlem hatlarını destekler. Azure DevOps hizmetleriyle, Scrum ve CMMI Çevik Geliştirme yöntemleri de destekler.

Team Foundation Server (TFS) Visual Studio uygulama yaşam döngüsü yönetimi hub ' dir. Tek bir çözüm kullanarak katılmak için geliştirme işlemine dahil olan herkes sağlar. TFS, heterojen takımlara ve projelere, çok yönetimi için avantajlıdır.

Azure DevOps kuruluş veya Team Foundation Server ağınız üzerinde varsa aracılığıyla bağlanmanız **Takım Gezgini** Visual Studio'daki. Bu pencereden içine veya dışına kaynak denetimi kodunu kontrol edin, çalışma öğelerini yönetmek, derlemeler ve erişim takım odaları ve çalışma alanları başlatın. **Takım Gezgini** arama kutusundan veya ana menüdeki**Takım Gezgini** **görüntüle** > ' den veya **takımdan** > **Bağlantıları Yönet**' den açabilirsiniz.

Aşağıdaki görüntüde **Takım Gezgini** penceresi Azure DevOps hizmetlerinde barındırılan bir çözüm.

![Visual Studio Takım Gezgini](../ide/media/vs2017_teamexplorer_devops.png)

Sürüm denetimine takımınızdaki geliştiriciler iade etmiş kod oluşturmak için yapı işleminizi otomatik hale getirebilirsiniz. Örneğin, gecelik bir veya daha fazla proje veya kodu iade her zaman oluşturabilirsiniz. Daha fazla bilgi için [Azure işlem hatları](/azure/devops/pipelines/index?view=vsts).

## <a name="extend-visual-studio"></a>Visual Studio’yu Genişletme

Visual Studio tam işlevselliğini ihtiyacınız yoksa, ekleyebilirsiniz! IDE, iş akışınıza ve stilinize göre kişiselleştirme, henüz Visual Studio ile tümleşik olmayan dış araçlarınız için destek ekleme ve üretkenliğinizi artırmak için var olan işlevselliği değiştirin. Visual Studio genişletilebilirlik Araçları (VS SDK) en son sürümünü bulmak için bkz: [Visual Studio SDK](../extensibility/visual-studio-sdk.md).

.NET derleyici Platformu ("Roslyn"), kendi kod Çözümleyicileri ve kod oluşturucuları yazmak için kullanabilirsiniz. İhtiyacınız olan her şeyi bulabilirsiniz [Roslyn](https://github.com/dotnet/Roslyn).

Bulma [mevcut Uzantılar](https://marketplace.visualstudio.com/vs) geliştirme topluluğumuza yanı sıra Microsoft geliştiricileri tarafından oluşturulan Visual Studio için.

Visual Studio'yu genişletme hakkında daha fazla bilgi için bkz: [Visual Studio IDE'yi genişletme](https://visualstudio.microsoft.com/vs/extend/).

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio IDE'ye genel bakış](../get-started/visual-studio-ide.md)
- [Visual Studio 2017'deki yenilikler](../ide/whats-new-visual-studio-2017.md)
- [Visual Studio 2019 ' deki yenilikler](../ide/whats-new-visual-studio-2019.md)
