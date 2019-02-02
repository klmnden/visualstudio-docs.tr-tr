---
title: Yayımlama alarak IIS yayımlama ayarları
description: Oluşturma ve bir uygulamayı Visual Studio'dan IIS dağıtmak için bir yayımlama profilini İçeri Aktar
ms.date: 01/31/2019
ms.topic: tutorial
helpviewer_keywords:
- deployment, publish settings
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 392770ae5a4ae37431c588d8d15f26a318bdc2c2
ms.sourcegitcommit: 612f8c21d1448f1a013c30100cdecfbec5ddb24f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2019
ms.locfileid: "55571062"
---
# <a name="publish-an-application-to-iis-by-importing-publish-settings-in-visual-studio"></a>İçeri aktararak IIS uygulama yayımlama Visual Studio'da yayımlama ayarları

Kullanabileceğiniz **Yayımla** almak için aracı yayımlama ayarları ve uygulamanızın dağıtabilirsiniz. Bu makalede kullandığımız IIS ayarlarını yayımlamak, ancak kullanabileceğiniz yayımlama ayarlarını içeri aktarmak için benzer adımları [Azure App Service](../deployment/tutorial-import-publish-settings-azure.md). Bir yayımlama ayarları profili Visual Studio'nun her bir yükleme IIS'ye dağıtım el ile yapılandırma daha hızlı olabilir, bazı senaryolarda kullanın.

Visual Studio'da ASP.NET, ASP.NET Core ve .NET Core uygulamaları için aşağıdaki adımları uygulayın. Adımlar Visual Studio 2017 sürüm 15.6 karşılık gelir.

Bu öğreticide şunları yapacaksınız:

> [!div class="checklist"]
> * Yayımlama ayarları dosyası oluşturabilmesi IIS yapılandırma
> * Yayımlama ayarları dosyası oluşturma
> * Yayımlama ayarları dosyasını Visual Studio'ya içeri aktarma
> * IIS uygulaması dağıtma

Yayımlama ayarları dosyası (*\*.publishsettings*) farklı bir yayımlama profili (*\*.pubxml*) Visual Studio'da oluşturulan. Yayımlama ayarları dosyası, IIS veya Azure App Service tarafından oluşturulan veya el ile oluşturulabilir ve ardından Visual Studio'ya içeri aktarılabilir.

> [!NOTE]
> Bir Visual Studio yayımlama profilini kopyalamak istiyorsanız (\*.pubxml dosya) Visual Studio için başka bir yükleme yayımlama profilini bulabilirsiniz  *\<profilename\>.pubxml*, içinde  *\\< projectname\>\Properties\PublishProfiles* yönetilen proje türleri için klasör. Web siteleri için altına bakın *\App_Data* klasör. Yayımlama profillerini MSBuild XML dosyalarıdır.

## <a name="prerequisites"></a>Önkoşullar

* Geliştirme bilgisayarınızda Visual Studio 2017 yüklü olması gerekir ve **ASP.NET ve web geliştirme** iş yükü.

    Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

* Sunucunuzda, Windows Server 2012 veya Windows Server 2016 çalıştırmalıdır ve olmalıdır [IIS Web sunucusu rolü](/iis/get-started/whats-new-in-iis-8/iis-80-using-aspnet-35-and-aspnet-45) düzgün yüklenmemiş (Yayımlama ayarları dosyası oluşturmak için gereken (*\*. publishsettings*)). ASP.NET 4.5 ya da ASP.NET Core, sunucuda ayrıca yüklenmelidir. ASP.NET 4.5 ' ayarlamak için bkz [IIS 8.0 kullanarak ASP.NET 3.5 ve ASP.NET 4.5](/iis/get-started/whats-new-in-iis-8/iis-80-using-aspnet-35-and-aspnet-45). ASP.NET Core ' ayarlamak için bkz [ana bilgisayar Windows IIS üzerinde ASP.NET Core](/aspnet/core/publishing/iis?tabs=aspnetcore2x#iis-configuration). 

## <a name="create-a-new-aspnet-project-in-visual-studio"></a>Visual Studio'da yeni bir ASP.NET projesi oluşturma

1. Visual Studio çalıştıran bilgisayarda **dosya** > **yeni proje**.

1. Altında **Visual C#**  veya **Visual Basic**, seçin **Web**, Orta bölmede seçin **ASP.NET Web uygulaması (.NET Framework)** veya (için C# yalnızca) **ASP.NET Core Web uygulaması**ve ardından **Tamam**.

    Belirtilen proje şablonları görmüyorsanız tıklayın **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu. Visual Studio Yükleyicisi'ni başlatır. Yükleme **ASP.NET ve web geliştirme** iş yükü.

    (ASP.NET veya ASP.NET Core) seçtiğiniz proje şablonu karşılık gelmelidir 

1. Seçin ya da **MVC** (.NET Framework) veya **Web uygulaması (Model-View-Controller)** (için .NET Core) emin olun **kimlik doğrulaması yok** seçilir ve ardından **Tamam**.

1. Gibi bir ad yazın **mywebapp şeklindedir** tıklatıp **Tamam**.

    Visual Studio projesi oluşturur.

1. Seçin **derleme** > **Çözümü Derle** Projeyi derlemek için.

## <a name="install-and-configure-web-deploy-on-windows-server"></a>Yükleme ve Windows Server üzerinde Web Dağıtımı'nı yapılandırma

[!INCLUDE [install-web-deploy-with-hosting-server](../deployment/includes/install-web-deploy-with-hosting-server.md)]

## <a name="create-the-publish-settings-file-in-iis-on-windows-server"></a>IIS Windows Server'da yayımlama ayarları dosyası oluşturma

[!INCLUDE [create-publish-settings-iis](../deployment/includes/create-publish-settings-iis.md)]

## <a name="import-the-publish-settings-in-visual-studio-and-deploy"></a>Visual Studio'da yayımlama ayarlarını içeri aktarın ve dağıtın

[!INCLUDE [import-publish-settings](../deployment/includes/import-publish-settings-vs.md)]

Uygulama başarıyla dağıtıldıktan sonra otomatik olarak başlayacaktır. Visual Studio'dan başlatılmazsa, IIS'de uygulamayı başlatın. ASP.NET Core için uygulama havuzu için alan emin olmamız gerekiyor. **DefaultAppPool** ayarlanır **yönetilen kod yok**.

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticide, bir yayımlama ayarları dosyası oluşturuldu, Visual Studio'ya içe ve ASP.NET uygulaması IIS'e. Visual Studio'da yayımlama diğer seçeneklerine genel bakış isteyebilirsiniz.

> [!div class="nextstepaction"]
> [Dağıtıma ilk bakış](../deployment/deploying-applications-services-and-components.md)
