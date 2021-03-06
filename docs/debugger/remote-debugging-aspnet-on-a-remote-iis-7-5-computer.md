---
title: IIS bilgisayarında ASP.NET hatalarını uzaktan ayıklama
ms.custom:
- remotedebugging
- seodec18
ms.date: 05/21/2018
ms.topic: conceptual
ms.assetid: 9cb339b5-3caf-4755-aad1-4a5da54b2a23
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: ba255d1d1e906e8fe7bacd05d1f4afd4b7bf413b
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63407849"
---
# <a name="remote-debug-aspnet-on-a-remote-iis-computer"></a>Bir uzak IIS bilgisayarında ASP.NET hatalarını uzaktan ayıklama
IIS'ye dağıtılan bir ASP.NET uygulamasında hata ayıklamak için yükleme ve uzak Araçlar, uygulamanızın dağıtıldığı bilgisayarda çalıştırın ve ardından Visual Studio'dan çalışan uygulamanıza ekleyin.

![Uzaktan hata ayıklayıcı bileşenleri](../debugger/media/remote-debugger-aspnet.png "Remote_debugger_components")

Bu kılavuz, ayarlayın ve Visual Studio ASP.NET MVC 4.5.2 uygulama yapılandırmak, IIS'ye dağıtma ve Visual Studio'dan uzak hata ayıklayıcıyı iliştirmek açıklanmaktadır.

> [!NOTE]
> Uzaktan için ASP.NET Core yerine hata ayıklamak için bkz: [IIS bilgisayarında uzaktan hata ayıklama ASP.NET Core](../debugger/remote-debugging-aspnet-on-a-remote-iis-computer.md). Azure App Service için kolayca dağıtabilir ve IIS kullanarak önceden yapılandırılmış bir örneğinde hata ayıklama [Snapshot Debugger](../debugger/debug-live-azure-applications.md) (.NET 4.6.1 gerekli) ya da [Haya ayıklayıcı Sunucu Gezgini'nden](../debugger/remote-debugging-azure.md).

## <a name="prerequisites"></a>Önkoşullar

::: moniker range=">=vs-2019"
Visual Studio 2019 bu makaledeki adımları izlemeniz gerekir.
::: moniker-end
::: moniker range="vs-2017"
Visual Studio 2017, bu makaledeki adımları tamamlayabilmeniz için gereklidir.
::: moniker-end

Bu yordamlar bu sunucu yapılandırmaları üzerinde test edilmiştir:
* Windows Server 2012 R2 ve IIS 8 (için Windows Server 2008 R2, server adımlarla farklı)

## <a name="network-requirements"></a>Ağ gereksinimleri

Uzaktan hata ayıklayıcı, Windows Server 2008 Service Pack 2 ile başlayarak Windows Server'da desteklenir. Gereksinimlerinin tam listesi için bkz. [gereksinimleri](../debugger/remote-debugging.md#requirements_msvsmon).

> [!NOTE]
> Bir proxy üzerinden bağlı iki bilgisayar arasında hata ayıklama desteklenmiyor. Ülkeler yüksek gecikme süresi veya çevirmeli, Internet gibi düşük bant genişliği bağlantı üzerinden veya Internet üzerinden hata ayıklama önerilmez ve başarısız olabilir veya edilemeyecek kadar yavaş.

## <a name="app-already-running-in-iis"></a>Zaten IIS içinde çalışan uygulama?

Bu makalede, temel bir Windows server IIS yapılandırmasını ayarlama ve uygulamayı Visual Studio'dan dağıtma adımlarını içerir. Sunucu bileşenleri yüklü, uygulamanın doğru şekilde çalıştırabilir ve uzaktan hata ayıklama için hazır olduğunu istedi emin olmak için bu adımları dahildir.

* Uygulamanızı IIS çalıştıran ve yalnızca istiyorsanız uzaktan hata ayıklayıcı indir ve hata ayıklama başlatmak için Git [indirin ve Windows Server'da uzak Araçları'nı yükleme](#BKMK_msvsmon).

* Emin olmak için Yardım istiyorsanız uygulamanızı, dağıtılan, ayarlanır ve böylece hata ayıklaması yapabilirsiniz, IIS'de doğru çalışmasını, bu konudaki tüm adımları izleyin.

## <a name="create-the-aspnet-452-application-on-the-visual-studio-computer"></a>ASP.NET 4.5.2 oluşturun Visual Studio bilgisayardaki uygulama

1. Yeni bir ASP.NET MVC uygulaması oluşturun.

    ::: moniker range=">=vs-2019"
    Visual Studio 2019 içinde yazın **Ctrl + Q** arama kutusunu açmak için şunu yazın **asp.net**, seçin **şablonları**, ardından **yeni ASP.NET Web uygulaması (.NET oluşturma Framework)** . Görüntülenen iletişim kutusunda, projeyi adlandırın **MyASPApp**ve ardından **Oluştur**. Seçin **MVC** ve **Oluştur**.
    ::: moniker-end
    ::: moniker range="vs-2017"
    Visual Studio 2017'de bunun tercih **Dosya > Yeni > Proje**, ardından **Visual C# > Web > ASP.NET Web uygulaması**. İçinde **ASP.NET 4.5.2** şablonları bölümünden **MVC**. Emin olun **Docker desteğini etkinleştir** seçilmezse ve **kimlik doğrulaması** ayarlanır **kimlik doğrulaması yok**. Projeyi adlandırın **MyASPApp**.)
    ::: moniker-end

2. HomeController.cs dosyasını açın ve bir kesim noktası `About()` yöntemi.

## <a name="bkmk_configureIIS"></a> Yükleme ve Windows Server'da IIS yapılandırma

[!INCLUDE [remote-debugger-install-iis-role](../debugger/includes/remote-debugger-install-iis-role.md)]

## <a name="update-browser-security-settings-on-windows-server"></a>Windows Server'da tarayıcınızın güvenlik ayarlarını güncelleştirin

(Varsayılan olarak etkindir) Internet Explorer Artırılmış Güvenlik Yapılandırması etkinse, bazı web sunucusu bileşenlerini yükleme sağlamak için Güvenilen siteler bazı etki alanları eklemek gerekebilir. Güvenilen siteler giderek ekleme **Internet Seçenekleri > Güvenlik > Güvenilen siteler > siteleri**. Aşağıdaki etki alanlarını ekleyin.

- Microsoft.com
- go.microsoft.com
- download.microsoft.com
- IIS.NET

Yazılımı indirdiğinizde, çeşitli web sitesi komut dosyaları ve kaynakları yüklemeye izin vermek için istekleri alabilirsiniz. Bu kaynaklardan bazıları, gerekli değildir, ancak sürecini basitleştirmek için tıklatın **Ekle** istendiğinde.

## <a name="BKMK_deploy_asp_net"></a> ASP.NET 4.5, Windows Server yükleme

IIS üzerinde ASP.NET yüklemek için daha ayrıntılı bilgi isterseniz bkz [IIS 8.0 kullanarak ASP.NET 3.5 ve ASP.NET 4.5](/iis/get-started/whats-new-in-iis-8/iis-80-using-aspnet-35-and-aspnet-45).

1. Sunucu Yöneticisi'nin sol bölmesinde, seçin **IIS**. Sunucuya sağ tıklayıp **Internet Information Services (IIS) Yöneticisi'ni**.

1. ASP.NET 4.5 yüklemek için Web Platformu Yükleyicisi (Webpı) kullanın (Windows Server 2012 R2'de sunucu düğümünden seçin **yeni Web Platformu bileşenlerini Al** ve ASP.NET için arama)

    ![RemoteDBG_IIS_AspNet_45](../debugger/media/remotedbg_iis_aspnet_45.png "RemoteDBG_IIS_AspNet_45")

    > [!NOTE]
    > Windows Server 2008 R2 kullanıyorsanız, bunun yerine şu komutu kullanarak ASP.NET 4'ü yükleyin:

     **C:\Windows\Microsoft.NET\Framework64\v4.0.30319\aspnet_regiis.exe -ir**

2. Sistemi yeniden başlatın (veya yürütme **net stop olan /y** ardından **net start w3svc** sistem YOLUNU bir değişiklik almak için bir komut isteminden).

## <a name="choose-a-deployment-option"></a>Bir dağıtım seçeneği seçin

IIS uygulama dağıtmak için yardıma gereksinim duyarsanız, bu seçenekleri göz önünde bulundurun:

* IIS'de bir yayımlama ayarları dosyası oluşturarak ve Visual Studio ayarları içeri aktarma dağıtın. Bazı senaryolarda, uygulamanızı dağıtmak için hızlı bir yolu budur. Yayımlama ayarları dosyası oluşturduğunuzda, IIS'de izinleri otomatik olarak ayarlanır.

* Yerel bir klasöre yayınlayarak ve IIS üzerinde bir hazır uygulamasını klasöre tarafından tercih edilen bir yöntem çıkışı kopyalama dağıtın.

## <a name="optional-deploy-using-a-publish-settings-file"></a>(İsteğe bağlı) Yayımlama ayarları dosyası kullanarak dağıtma

Bu seçeneği kullanabilirsiniz. Visual Studio'ya içeri aktarma ve yayımlama ayarları dosyası oluşturun.

> [!NOTE]
> Bu dağıtım yöntemi, Web dağıtımı kullanır. Web dağıtımı el ile Visual Studio ayarları içeri aktarma yerine yapılandırmak istiyorsanız, barındırma sunucuları için Web dağıtımı 3.6 yerine Web dağıtma 3.6 yükleyebilirsiniz. Ancak, Web dağıtımı el ile yapılandırırsanız, sunucuda bir uygulama klasör izinleri ve doğru değerleri ile yapılandırıldığından emin olun gerekecektir (bkz [yapılandırma ASP.NET Web sitesi](#BKMK_deploy_asp_net)).

### <a name="install-and-configure-web-deploy-for-hosting-servers-on-windows-server"></a>Yükleme ve Windows Server üzerinde barındırma sunucuları için Web dağıtımı yapılandırma

[!INCLUDE [install-web-deploy-with-hosting-server](../deployment/includes/install-web-deploy-with-hosting-server.md)]

### <a name="create-the-publish-settings-file-in-iis-on-windows-server"></a>IIS Windows Server'da yayımlama ayarları dosyası oluşturma

[!INCLUDE [install-web-deploy-with-hosting-server](../deployment/includes/create-publish-settings-iis.md)]

### <a name="import-the-publish-settings-in-visual-studio-and-deploy"></a>Visual Studio'da yayımlama ayarlarını içeri aktarın ve dağıtın

[!INCLUDE [install-web-deploy-with-hosting-server](../deployment/includes/import-publish-settings-vs.md)]

Uygulama başarıyla dağıtıldıktan sonra otomatik olarak başlayacaktır. Uygulamayı Visual Studio'dan başlatılmazsa, IIS'de uygulamayı başlatın.

1. İçinde **ayarları** iletişim kutusu, tıklayarak hata ayıklamayı etkinleştir **sonraki**, seçin bir **hata ayıklama** yapılandırma ve ardından **ek dosyaları Kaldır Hedef** altında **dosya yayımlama** seçenekleri.

    > [!NOTE]
    > Yayın yapılandırması seçerseniz, hata ayıklama devre dışı *web.config* yayımladığınızda, dosya.

1. Tıklayın **Kaydet** ve sonra uygulamayı yeniden yayımlayın.

## <a name="optional-deploy-by-publishing-to-a-local-folder"></a>(İsteğe bağlı) Yerel bir klasöre yayımlayarak dağıtma

RoboCopy, Powershell kullanarak IIS uygulama kopyalamak istediğiniz veya dosyaları el ile kopyalamak isterseniz, uygulamanızı dağıtmak için bu seçeneği kullanabilirsiniz.

### <a name="BKMK_deploy_asp_net"></a> Windows Server bilgisayarında ASP.NET Web sitesi yapılandırma

1. Windows Gezgini'ni açın ve yeni bir klasör oluşturun **C:\Publish**, ASP.NET projesi daha sonra dağıtacağınız.

2. Zaten açık değilse, açmak **Internet Information Services (IIS) Yöneticisi'ni**. (Sunucu Yöneticisi'nin sol bölmesinde, seçin **IIS**. Sunucuya sağ tıklayıp **Internet Information Services (IIS) Yöneticisi'ni**.)

3. Altında **bağlantıları** sol bölmede, Git **siteleri**.

4. Seçin **varsayılan Web sitesi**, seçin **temel ayarları**, ayarlayıp **fiziksel yolu** için **C:\Publish**.

5. Sağ **varsayılan Web sitesi** düğümünü seçip alt **uygulama Ekle**.

6. Ayarlama **diğer** alanı **MyASPApp**, uygulama havuzu varsayılan değeri kabul edin (**DefaultAppPool**) ve **fiziksel yolu** için **C:\Publish**.

7. Altında **bağlantıları**seçin **uygulama havuzları**. Açık **DefaultAppPool** ve uygulama havuzu alanın ayarlanacağı **ASP.NET v4.0** (ASP.NET 4.5 uygulama havuzu için bir seçenek değildir).

8. IIS Yöneticisi'nde site seçiliyken, seçin **düzenleme izinleri**ve o IUSR, IIS_IUSRS veya uygulama havuzu okuma & yürütme hakları olan yetkili bir kullanıcı için yapılandırılan kullanıcı emin olun. Bu kullanıcılar hiçbiri mevcut olması durumunda, okuma ve yürütme hakları olan bir kullanıcı olarak IUSR'yi ekleyin.

### <a name="publish-and-deploy-the-app-by-publishing-to-a-local-folder-from-visual-studio"></a>Yayımlama ve uygulamayı yayımlayarak bir yerel klasöre Visual Studio'dan dağıtma

Ayrıca, yayımlama ve dosya sistemi veya diğer araçları kullanarak uygulamayı dağıtırsınız.

1. (ASP.NET 4.5.2) Web.config dosyasının doğru sürümü .NET Framework'ün gösterdiğinden emin olun.  Örneğin, ASP.NET 4.5.2 hedefliyorsanız, bu sürüm, web.config dosyasında listelendiğinden emin olun.

    ```xml
    <system.web>
      <compilation debug="true" targetFramework="4.5.2" />
      <httpRuntime targetFramework="4.5.2" />
      <httpModules>
        <add name="ApplicationInsightsWebTracking" type="Microsoft.ApplicationInsights.Web.ApplicationInsightsHttpModule, Microsoft.AI.Web" />
      </httpModules>
    </system.web>

    ```

    Örneğin, ASP.NET 4 yerine 4.5.2 yüklerseniz sürümü 4.0 olmalıdır.

[!INCLUDE [remote-debugger-deploy-app-local](../debugger/includes/remote-debugger-deploy-app-local.md)]

## <a name="BKMK_msvsmon"></a> İndirme ve Windows Server'da uzak araçları yükleme

Visual Studio sürümünüzle eşleşen uzak Araçlar sürümü indirin.

[!INCLUDE [remote-debugger-download](../debugger/includes/remote-debugger-download.md)]

## <a name="BKMK_setup"></a> Windows Server'da uzaktan hata ayıklayıcı ayarlama

[!INCLUDE [remote-debugger-configuration](../debugger/includes/remote-debugger-configuration.md)]

> [!NOTE]
> Gerektiğinde ek kullanıcılar için izinler eklemek için kimlik doğrulama modunu değiştirmek veya bağlantı noktası numarası için uzaktan hata ayıklayıcı değilse [uzaktan hata ayıklayıcı yapılandırma](../debugger/remote-debugging.md#configure_msvsmon).

Uzaktan hata ayıklayıcıyı bir hizmet olarak çalıştırma hakkında daha fazla bilgi için bkz: [uzaktan hata ayıklayıcıyı bir hizmet olarak çalıştırmak](../debugger/remote-debugging.md#bkmk_configureService).

## <a name="BKMK_attach"></a> Visual Studio bilgisayardan ASP.NET uygulamasına ekleme

1. Visual Studio bilgisayarda hata ayıklamaya çalıştığınız çözümü açın (**MyASPApp** bu makaledeki adımları takip ediyorsanız).
2. Visual Studio'da **hata ayıklama > iliştirme** (Ctrl + Alt + P).

    > [!TIP]
    > Visual Studio 2017 ve sonraki sürümlerinde, daha önce ekli kullanarak aynı işleme iliştirebilirsiniz **hata ayıklama > İliştir...** (Shift + Alt + P).

3. Niteleyici alanın ayarlanacağı  **\<uzak bilgisayar adı >** basın **Enter**.

    Visual Studio biçiminde görünür bilgisayar adı gerekli bağlantı noktası eklediğini doğrulayın:  **\<uzak bilgisayar adı >: bağlantı noktası**

    ::: moniker range=">=vs-2019"
    Visual Studio 2019 üzerinde görmelisiniz  **\<uzak bilgisayar adı >: 4024**
    ::: moniker-end
    ::: moniker range="vs-2017"
    Visual Studio 2017'de görmelisiniz  **\<uzak bilgisayar adı >: 4022**
    ::: moniker-end
    Bağlantı noktası gereklidir. Bağlantı noktası numarasını görmüyorsanız, el ile ekleyin.

4. Tıklayın **Yenile**.
    Bazı işlemler görünür görmelisiniz **kullanılabilir işlemler** penceresi.

    Herhangi bir işlem görmüyorsanız (bağlantı noktası gereklidir) uzak bilgisayar adı yerine IP adresini kullanarak deneyin. Kullanabileceğiniz `ipconfig` IPv4 adresini almak için komut satırında.

5. Denetleme **tüm kullanıcıların işlemlerini göster**.

6. Hızlı bir şekilde bulmak için bir işlem adının ilk harfi yazın **w3wp.exe** ASP.NET 4.5 için.

    Birden çok işlem gösteren varsa **w3wp.exe**, kontrol **kullanıcı adı** sütun. Bazı senaryolarda **kullanıcı adı** sütunda görüntülenir, uygulama havuzu adı gibi **IIS APPPOOL\DefaultAppPool**. Uygulama havuzu bakın, doğru işlemi tanıtmak için kolay bir yolunu yeni bir uygulama havuzu ayıklamak istediğiniz uygulama örneği için adlandırılmış bir gruptur ve ardından kolay bulabileceğinizi **kullanıcı adı** sütun.

    ::: moniker range=">=vs-2019"
    ![RemoteDBG_AttachToProcess](../debugger/media/vs-2019/remotedbg-attachtoprocess.png "RemoteDBG_AttachToProcess")
    ::: moniker-end
    ::: moniker range="vs-2017"
    ![RemoteDBG_AttachToProcess](../debugger/media/remotedbg-attachtoprocess.png "RemoteDBG_AttachToProcess")
    ::: moniker-end

7. Tıklayın **ekleme**

8. Uzak bilgisayarın Web sitesini açın. Bir tarayıcıda Git **http://\<uzak bilgisayar adı >** .

    ASP.NET web sayfası görmeniz gerekir.
9. Çalışan ASP.NET uygulama bağlantısını tıklayın **hakkında** sayfası.

    Visual Studio'da kesme noktasına isabet.

## <a name="bkmk_openports"></a> Sorun giderme: Windows Server üzerinde gerekli bağlantı noktalarını açma

Çoğu ayarlar ASP.NET ve uzaktan hata ayıklayıcı yüklemesi tarafından gerekli bağlantı noktalarının açıldığından. Ancak, bağlantı noktalarının açık olduğunu doğrulamak gerekebilir.

> [!NOTE]
> Bir Azure sanal makinesinde aracılığıyla bağlantı noktalarını açmanız gerekir [ağ güvenlik grubu](/azure/virtual-machines/windows/nsg-quickstart-portal).

Gerekli bağlantı noktaları:

* 80 - IIS için gerekli
::: moniker range=">=vs-2019"
* 4024 - gerekli Visual Studio 2019 ' uzaktan hata ayıklama için (bkz [uzaktan hata ayıklayıcı bağlantı noktası atamaları](../debugger/remote-debugger-port-assignments.md) daha fazla bilgi için).
::: moniker-end
::: moniker range="vs-2017"
* 4022 - gerekli Visual Studio 2017'den uzaktan hata ayıklama için (bkz [uzaktan hata ayıklayıcı bağlantı noktası atamaları](../debugger/remote-debugger-port-assignments.md) daha fazla bilgi için).
::: moniker-end
* UDP 3702 - (isteğe bağlı) bulma bağlantı sağlar, **Bul** düğme Visual Studio uzaktan hata ayıklayıcı eklerken.

1. Windows Server üzerindeki bir bağlantı noktasını açmak için Aç **Başlat** menüsünde **Gelişmiş Güvenlik Özellikli Windows Güvenlik Duvarı**.

2. Ardından **gelen kuralları > Yeni Kural > bağlantı noktası**. Seçin **sonraki** altında **belirli yerel bağlantı noktaları**, bağlantı noktası numarasını girin, tıklayın **sonraki**, ardından **bağlantıya izin**, İleri'ye tıklayın ve ad ekleyin (**IIS**, **Web dağıtımı**, veya **msvsmon**) gelen kuralı için.

    Windows Güvenlik Duvarı yapılandırma hakkında ayrıntılı bilgi isterseniz bkz [uzaktan hata ayıklama için Windows Güvenlik Duvarı Yapılandırma](../debugger/configure-the-windows-firewall-for-remote-debugging.md).

3. Diğer gerekli bağlantı noktaları için ek kurallar oluşturun.