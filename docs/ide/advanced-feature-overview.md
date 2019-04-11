---
title: Gelişmiş özellikler
ms.date: 06/01/2018
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f7a9fdb7d6f17df009920e1677c615cb41df7f6c
ms.sourcegitcommit: 7eb85d296146186e7a39a17f628866817858ffb0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/11/2019
ms.locfileid: "59504308"
---
# <a name="features-of-visual-studio"></a>Visual Studio özellikleri

[Visual Studio IDE'ye genel bakış](../get-started/visual-studio-ide.md) makale, Visual Studio için temel bir giriş sağlar. Bu makalede, deneyimli geliştiriciler veya Visual Studio ile ilgili bilgi sahibi olan bu geliştiriciler için daha uygun olabilir özelliklerini açıklar.

## <a name="modular-installation"></a>Modüler yükleme

Visual Studio modüler yükleyici seçin ve yüklemek tanır *iş yükleri*. İş yükleri programlama dili veya tercih ettiğiniz platform için gerekli özellikleri gruplarıdır. Bu strateji, yükler ve çok daha hızlı güncelleştirmeler ayak izini daha küçük, Visual Studio yüklemesinin kalmasına yardımcı olur.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range=">=vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz yüklemek için sayfa.

::: moniker-end

Sisteminizde Visual Studio'yu ayarlama hakkında daha fazla bilgi edinmek için [Visual Studio'yu yükleyin](../install/install-visual-studio.md).

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

- Yerel C++ uygulamaları iOS, Android ve Windows için derleme cihazlar. Kullanarak iOS, Android ve Windows, yerleşik kitaplıklarda ortak kod paylaşma [C++ platformlar arası geliştirme için](../cross-platform/visual-cpp-for-cross-platform-mobile-development.md).

- Dağıtın, test edin ve Android uygulamaları ile hata ayıklama [Android öykünücüsü](../cross-platform/visual-studio-emulator-for-android.md).

## <a name="connect-to-databases"></a>Veritabanlarına bağlanma

**Sunucu Gezgini** göz atın ve SQL Server örnekleri ve varlıkları yerel olarak, uzaktan ve Azure, Salesforce.com, Office 365 ve Web siteleri üzerinde yönetmenize yardımcı olur. Açmak için **Sunucu Gezgini**, ana menüsünde **görünümü** > **Sunucu Gezgini**. Sunucu Gezgini kullanma hakkında daha fazla bilgi için bkz. [yeni bağlantı ekleme](../data-tools/add-new-connections.md).

[SQL Server veri Araçları (SSDT)](/sql/ssdt/download-sql-server-data-tools-ssdt) SQL Server, Azure SQL veritabanı ve Azure SQL veri ambarı için bir güçlü bir geliştirme ortamıdır. Derleme, hata ayıklama, korumak ve veritabanlarını yeniden düzenleme sağlar. Bir veritabanı projesiyle veya doğrudan ile bir bağlı veritabanı örneği veya kapalı-şirket içinde çalışabilir.

**SQL Server Nesne Gezgini** Visual Studio'da veritabanı nesnelerini SQL Server Management Studio'ya benzer bir görünüm sağlar. SQL Server Nesne Gezgini light vergileri veritabanı yönetimi ve tasarım işlerini yapmasına imkan sağlar. Tablo verilerini, şemalar, SQL Server nesne Gezgini'nde sağ bağlam menüleri ve daha fazlasını kullanarak sorgular yürütme karşılaştırma düzenleme iş örnek verilebilir.

![SQL Server Object Explorer](../ide/media/vs2015_sqlobjectexplorer.png)

## <a name="debug-test-and-improve-your-code"></a>Hata ayıklama, test etme ve kodunuzu geliştirme

Kod yazmak, çalıştırmak ve hataları ve performans için test gerekir. Visual Studio'nun en son hata ayıklama sistem projenizdeki yerel veya uzak cihaz üzerinde çalışan kodda hata ayıklamak sağlayan bir [cihaz öykünücüsünü](../cross-platform/visual-studio-emulator-for-android.md). Aynı anda bir deyim kod adım adım ve kullandıkça değişkenleri denetleyin. Belirtilen bir koşul true olduğunda yalnızca isabet kesme noktaları ayarlayabilirsiniz. Hata ayıklama seçenekleri yönetilen kod düzenleyicisinde kendisi, böylece kodunuzdan çıkmanıza gerek yoktur. Visual Studio'da hata ayıklama hakkında daha fazla bilgi edinmek için bkz. [hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md).

Visual Studio'nun kullanıma kullanıma alma uygulamalarınızın performansını iyileştirme hakkında daha fazla bilgi edinmek için [profil oluşturma](../profiling/profiling-feature-tour.md) özelliği.

İçin [test](../test/improve-code-quality.md), Visual Studio birim testi, Live Unit Testing, Intellitest, yük ve performans testi ve daha fazlasını sunar. Visual Studio Gelişmiş de [Kod Analizi](../code-quality/code-analysis-for-managed-code-overview.md) tasarım, güvenlik ve diğer türleri standartlarımızı yakalamak için özellikleri.

## <a name="deploy-your-finished-application"></a>Tamamlanmış uygulama dağıtma

Uygulamanızın kullanıcıları veya müşterileri dağıtmak hazır olduğunda, Visual Studio Bunu yapmak için gereken araçları sağlar. Dağıtım seçenekleri için Microsoft Store, bir SharePoint sitesine veya InstallShield veya Windows Installer teknolojileriyle içerir. Bu, tüm IDE erişilebilir. Daha fazla bilgi için [uygulamaları, hizmetleri ve bileşenleri dağıtma](../deployment/deploying-applications-services-and-components.md).

## <a name="manage-your-source-code-and-collaborate-with-others"></a>Kaynak kodunuzu yönetin ve başkalarıyla işbirliği yapın

GitHub dahil olmak üzere herhangi bir sağlayıcı tarafından barındırılan Git depolarındaki kaynak kodunuzu yönetebilirsiniz. Veya [Azure DevOps Hizmetleri](/azure/devops/index) hataların yanında kodu yönetmek ve iş öğelerinin projenizin tamamında. Bkz: [Azure depoları ve Git ile çalışmaya başlama](/azure/devops/repos/git/gitquickstart?tabs=visual-studio) Visual Studio'da Takım Gezgini'ni kullanarak Git depoları yönetme hakkında daha fazla bilgi edinmek için. Visual Studio'nun diğer yerleşik kaynak denetimi özellikleri de vardır. Bunlar hakkında daha fazla bilgi edinmek için [yeni Git özellikleri (blog) Visual Studio'da](https://devblogs.microsoft.com/devops/new-git-features-in-visual-studio-2017/).

Azure DevOps planlamak, ana bilgisayar, otomatikleştirin ve yazılım dağıtma ve teams'de işbirliği etkinleştirmek için bulut tabanlı hizmetlere hizmetleridir. Azure DevOps hizmetleriyle Git depoları (dağıtılmış sürüm denetimi) hem de Team Foundation sürüm denetimi (merkezi sürüm denetimi) destekler. Bunlar için sürekli derleme ve sürüm denetim sisteminde depolanan kod (CI/CD) yayın işlem hatları destekler. Azure DevOps hizmetleriyle, Scrum ve CMMI Çevik Geliştirme yöntemleri de destekler.

Team Foundation Server (TFS) Visual Studio uygulama yaşam döngüsü yönetimi hub ' dir. Tek bir çözüm kullanarak katılmak için geliştirme işlemine dahil olan herkes sağlar. TFS, heterojen takımlara ve projelere, çok yönetimi için avantajlıdır.

Azure DevOps kuruluş veya Team Foundation Server ağınız üzerinde varsa aracılığıyla bağlanmanız **Takım Gezgini** Visual Studio'daki. Bu pencereden içine veya dışına kaynak denetimi kodunu kontrol edin, çalışma öğelerini yönetmek, derlemeler ve erişim takım odaları ve çalışma alanları başlatın. Açabileceğiniz **Takım Gezgini** arama kutusundan ya da ana menüde **görünümü** > **Takım Gezgini** veya **takım**  >  **Bağlantıları yönetme**.

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
- [Visual Studio 2017’deki yenilikler](../ide/whats-new-visual-studio-2017.md)
- [Visual Studio 2019’daki yenilikler](../ide/whats-new-visual-studio-2019.md)
