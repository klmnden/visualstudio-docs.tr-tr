---
title: Azure'da alarak yayımlama yayımlama ayarları
description: Oluşturma ve bir uygulamayı Visual Studio'dan Azure App Service dağıtmak için bir yayımlama profilini İçeri Aktar
ms.date: 05/07/2018
ms.topic: tutorial
helpviewer_keywords:
- deployment, publish settings
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bd040b613a5b982050d651f341456c5fafc2954b
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65679183"
---
# <a name="publish-an-application-to-azure-app-service-by-importing-publish-settings-in-visual-studio"></a>İçeri aktararak Azure App Service'e bir uygulamayı yayımladığınızda Visual Studio'da yayımlama ayarları

Kullanabileceğiniz **Yayımla** almak için aracı yayımlama ayarları ve uygulamanızın dağıtabilirsiniz. Bu makalede kullandığımız Azure App Service için yayınlama ayarlarını ancak kullanabileceğiniz yayımlama ayarlarını içeri aktarmak için benzer adımları [IIS](../deployment/tutorial-import-publish-settings-iis.md). Bir yayımlama ayarları profili Hizmeti'ne Visual Studio'nun her yükleme için dağıtım el ile yapılandırma daha hızlı olabilir, bazı senaryolarda kullanın.

Visual Studio'da ASP.NET, ASP.NET Core ve .NET Core uygulamaları için aşağıdaki adımları uygulayın. Ayrıca Al için yayınlama ayarlarını [Python](../python/publishing-python-web-applications-to-azure-from-visual-studio.md) uygulamalar.

Bu öğreticide şunları yapacaksınız:

> [!div class="checklist"]
> * Azure uygulama Hizmeti'nden yayımlama ayarları dosyası oluştur
> * Yayımlama ayarları dosyasını Visual Studio'ya içeri aktarma
> * Uygulamayı Azure App Service'e dağıtma

Yayımlama ayarları dosyası (*\*.publishsettings*) farklı bir yayımlama profili (*\*.pubxml*) Visual Studio'da oluşturulan. Yayımlama ayarları dosyasını Azure App Service tarafından oluşturulur ve ardından Visual Studio'ya içeri aktarılabilir.

> [!NOTE]
> Bir Visual Studio yayımlama profilini kopyalamak istiyorsanız (*\*.pubxml* dosya) Visual Studio için başka bir yükleme yayımlama profilini bulabilirsiniz  *\<profilename\>.pubxml*,  *\\< projectname\>\Properties\PublishProfiles* yönetilen proje türleri için klasör. Web siteleri için altına bakın *\App_Data* klasör. Yayımlama profillerini MSBuild XML dosyalarıdır.

## <a name="prerequisites"></a>Önkoşullar

::: moniker range=">=vs-2019"

* Visual Studio 2019 yüklü olması gerekir ve **ASP.NET ve web geliştirme** iş yükü.

    Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/) ücretsiz yüklemek için sayfa.
::: moniker-end

::: moniker range="vs-2017"

* Visual Studio 2017 yüklü olması gerekir ve **ASP.NET ve web geliştirme** iş yükü.

    Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/) ücretsiz yüklemek için sayfa.
::: moniker-end

* Azure App Service'e oluşturun. Ayrıntılı yönergeler için bkz. [Visual Studio'yu kullanarak Azure'a bir ASP.NET Core web uygulaması dağıtma](/aspnet/core/tutorials/publish-to-azure-webapp-using-vs).

## <a name="create-a-new-aspnet-project-in-visual-studio"></a>Visual Studio'da yeni bir ASP.NET projesi oluşturma

1. Visual Studio çalıştıran bilgisayarda, yeni bir proje oluşturun.

    Doğru şablonu seçin. Bu örnekte seçin ya da **ASP.NET Web uygulaması (.NET Framework)** veya (için C# yalnızca) **ASP.NET Core Web uygulaması**ve ardından **Tamam**.

    Belirtilen proje şablonları görmüyorsanız tıklayın **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu. Visual Studio Yükleyicisi'ni başlatır. Yükleme **ASP.NET ve web geliştirme** iş yükü.

    (ASP.NET veya ASP.NET Core) seçtiğiniz proje şablonu, ASP.NET web sunucusunda yüklü sürümüne karşılık gelmelidir.

1. Seçin ya da **MVC** (.NET Framework) veya **Web uygulaması (Model-View-Controller)** (için .NET Core) emin olun **kimlik doğrulaması yok** seçilir ve ardından **Tamam**.

1. Gibi bir ad yazın **mywebapp şeklindedir** tıklatıp **Tamam**.

    Visual Studio projesi oluşturur.

1. Seçin **derleme** > **Çözümü Derle** Projeyi derlemek için.

## <a name="create-the-publish-settings-file-in-azure-app-service"></a>Azure App Service'te yayımlama ayarları dosyası oluşturma

1. Azure portalında, Azure App Service'ı açın.

1. Tıklayın **yayımlama profili Al** ve profili yerel olarak kaydedin.

    ![Yayımlama profili Al](../deployment/media/tutorial-azure-app-service-get-publish-profile.png)

    Bir dosya bir *.publishsettings* dosya uzantısı, kaydettiğiniz bu konumda oluşturulan. Aşağıdaki kod dosyasının (bir daha okunabilir biçimlendirme) kısmi bir örnek gösterir.

    ```xml
    <publishData>
      <publishProfile
        profileName="DeployASPDotNetCore - Web Deploy"
        publishMethod="MSDeploy"
        publishUrl="deployaspdotnetcore.scm.azurewebsites.net:443"
        msdeploySite="DeployASPDotNetCore"
        userName="$DeployASPDotNetCore"
        userPWD="abcdefghijklmnopqrstuzwxyz"
        destinationAppUrl="http://deployaspdotnetcore20180508031824.azurewebsites.net"
        SQLServerDBConnectionString=""
        mySQLDBConnectionString=""
        hostingProviderForumLink=""
        controlPanelLink="http://windows.azure.com"
        webSystem="WebSites">
        <databases />
      </publishProfile>
    </publishData>
    ```

    Genellikle, önceki *.publishsettings dosyasını Visual Studio'da bir Web dağıtımı ve bir FTP kullanarak dağıtma kullanarak dağıtmak için kullanabileceğiniz iki yayımlama profillerini içerir. Yukarıdaki kod, Web dağıtımı profili gösterir. Profili içeri aktardığınızda her iki profili de daha sonra içeri aktarılır.

## <a name="import-the-publish-settings-in-visual-studio-and-deploy"></a>Visual Studio'da yayımlama ayarlarını içeri aktarın ve dağıtın

[!INCLUDE [import publish settings](../deployment/includes/import-publish-settings-vs.md)]

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticide, bir yayımlama ayarları dosyası oluşturuldu, Visual Studio'ya içe ve ASP.NET uygulamasını Azure App Service'e dağıtılır. Visual Studio'da yayımlama seçeneklerine genel bakış isteyebilirsiniz.

> [!div class="nextstepaction"]
> [Dağıtıma ilk bakış](../deployment/deploying-applications-services-and-components.md)
