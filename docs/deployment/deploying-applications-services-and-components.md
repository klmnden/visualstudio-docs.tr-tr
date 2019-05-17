---
title: Dağıtım özellik turu
description: Visual Studio'dan uygulamaları dağıtmak için seçenekleri hakkında bilgi edinin.
ms.custom: mvc
ms.date: 01/29/2019
ms.topic: quickstart
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- .NET applications, deploying
- components [Visual Studio], deploying
- installers
- publishing
- deploying applications [Visual Studio]
- deploying applications [Visual Studio], about deploying applications
- components [.NET Framework], deploying
ms.assetid: 63fcdd5b-2e54-4210-9038-65bc23167725
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e66eb7fc2915514b91135e8c89843a0d979abf4a
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65845902"
---
# <a name="first-look-at-deployment-in-visual-studio"></a>Visual Studio'daki dağıtımı da ilk bakma

Bir uygulama, hizmet ya da bileşeni dağıtarak, yüklemenin diğer bilgisayarlar, cihazlar veya sunucular üzerinde veya bulutta dağıtın. İhtiyacınız olan dağıtım türü için uygun yöntemi Visual Studio'da seçebilirsiniz. (Burada açıklanmamaktadır, diğer dağıtım araçları komut satırı dağıtımı veya NuGet gibi birçok uygulama türlerini destekler.)

Hızlı Başlangıçlar ve öğreticilerle adım adım dağıtım yönergeleri için bkz. Dağıtım seçeneklerine genel bakış için bkz. [hangi Yayımlama seçenekleri benim için en uygun?](deploying-applications-services-and-components-resources.md#what-publishing-options-are-right-for-me).

## <a name="deploy-to-local-folder"></a>Yerel klasöre dağıtma

Yerel bir klasöre dağıtım genellikle test etmek veya başka bir aracı son dağıtım için kullanılan aşamalı bir dağıtım başlatmak için kullanılır.

- **ASP.NET**, **ASP.NET Core**, **Node.js**, **Python**, ve. **NET Core**: Bir yerel klasöre dağıtma yayımlama aracını kullanın. Kullanılabilir seçenekler, uygulama türüne bağlıdır. Çözüm Gezgini'nde projenize sağ tıklayıp seçin **Yayımla**. (Tüm yayımlama profilleri daha önce yapılandırmadıysanız, ardından tıklamanız **yeni profil oluşturma**.) Ardından, **klasör**. Daha fazla bilgi için [bir yerel klasöre dağıtma](quickstart-deploy-to-local-folder.md).

    ![Seçin yayımlama](../deployment/media/quickstart-publish.png)

- **Windows Masaüstü** Windows masaüstü uygulaması bir klasöre ClickOnce dağıtımını kullanarak yayımlayabilirsiniz. Kullanıcılar, daha sonra uygulamayı tek bir tıklamayla yükleyebilir. Daha fazla bilgi için [ClickOnce kullanarak masaüstü uygulaması dağıtma](how-to-publish-a-clickonce-application-using-the-publish-wizard.md) (C# ve Visual Basic). İçin C++/CLR, bkz: [ClickOnce kullanarak yerel bir uygulama dağıtma](/cpp/ide/clickonce-deployment-for-visual-cpp-applications) veya C /C++, bkz: [bir kurulum projesi kullanarak yerel bir uygulama dağıtma](/cpp/ide/walkthrough-deploying-a-visual-cpp-application-by-using-a-setup-project).

## <a name="publish-to-azure"></a>Azure'a Yayımlama

- **ASP.NET**, **ASP.NET Core**, **Python**, ve **Node.js**: Azure App Service veya Azure App Service (kapsayıcılar kullanarak) Linux yayımlamak aşağıdaki yöntemlerden birini kullanarak.

  - Azure DevOps ile sürekli (veya otomatik) dağıtımı uygulamalar için kullanmak [Azure işlem hatları](https://docs.microsoft.com/azure/devops/pipelines/get-started-yaml?view=azdevops).

  - Tek seferlik (veya elle) dağıtımı uygulamalar için kullanmak **Yayımla** Visual Studio'da araç.

  Sunucunun daha özelleştirilmiş bir yapılandırma sağlayan bir dağıtım için de kullanabilirsiniz **Yayımla** uygulamaları dağıtmak için bir Azure sanal makinesi için aracı.

  Kullanılacak **Yayımla** aracı, Çözüm Gezgini'nde projeye sağ tıklayıp seçin **Yayımla**. (Tüm yayımlama profilleri daha önce yapılandırdıysanız, ardından tıklamanız **yeni profil oluşturma**.) Yayımla iletişim kutusunda seçin **App Service** veya **Azure sanal makineler**ve ardından yapılandırma adımlarını izleyin.

  ![Azure uygulama hizmeti seçin](../deployment/media/quickstart-publish-azure.png "Azure uygulama hizmeti seçin")

  Visual Studio 2017 sürüm 15.7 başlayarak, ASP.NET Core uygulamaları dağıtabilirsiniz **Linux için App Service**.

  Python uygulamaları için Ayrıca bkz: [Python - Azure App Service'te yayımlama](../python/publishing-python-web-applications-to-azure-from-visual-studio.md?toc=/visualstudio/deployment/toc.json&bc=/visualstudio/deployment/_breadcrumb/toc.json).

  Hızlı bir giriş için bkz. [azure'a Yayımla](quickstart-deploy-to-azure.md) ve [Linux'a yayımlama](quickstart-deploy-to-linux.md). Ayrıca bkz [Azure'a bir ASP.NET Core uygulaması yayımlama](/aspnet/core/tutorials/publish-to-azure-webapp-using-vs). Git'i kullanarak dağıtım için bkz [ASP.NET core'un Git ile azure'a sürekli dağıtım](/aspnet/core/publishing/azure-continuous-deployment).

  Bir yayımlama profili, Visual Studio için Azure App Service'ten alma hakkında daha fazla bilgi için bkz: [yayımlama ayarlarını içeri aktarma ve Azure'a dağıtma](../deployment/tutorial-import-publish-settings-azure.md).

  > [!NOTE]
  > Zaten bir Azure hesabınız yoksa, şunları yapabilirsiniz [buradan kaydolun](https://azure.microsoft.com/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=doc&utm_campaign=visualstudio).

## <a name="publish-to-web-or-deploy-to-network-share"></a>Web'de Yayımla veya ağ paylaşımına dağıtma

- **ASP.NET**, **ASP.NET Core**, **Node.js**, ve **Python**: Yayımla aracı, FTP veya Web dağıtımını kullanarak bir Web sitesine dağıtmak için kullanabilirsiniz. Daha fazla bilgi için [bir web sitesine dağıtma](quickstart-deploy-to-a-web-site.md).

    Çözüm Gezgini'nde projeye sağ tıklayıp seçin **Yayımla**. (Tüm yayımlama profilleri daha önce yapılandırdıysanız, ardından tıklamanız **yeni profil oluşturma**.) Yayımlama aracında yapılandırma adımlarını izleyin ve istediğiniz seçeneği belirleyin.

    ![IIS, FTP, vb.'ı seçin.](../deployment/media/quickstart-publish-iis-ftp.png)

    Visual Studio'da bir yayımlama profilini içeri aktarma hakkında daha fazla bilgi için bkz: [IIS'ye dağıtma ve yayımlama ayarlarını içeri aktarma](../deployment/tutorial-import-publish-settings-iis.md).

    Ayrıca, ASP.NET uygulamaları ve Hizmetleri diğer çeşitli yollarla dağıtabilirsiniz. Daha fazla bilgi için [dağıtma ASP.NET web uygulamaları ve Hizmetleri](http://www.asp.net/aspnet/overview/deployment).

- **Windows Masaüstü** Windows masaüstü uygulaması için bir web sunucusu veya ClickOnce dağıtımını kullanarak bir ağ dosya paylaşımına yayımlayabilirsiniz. Kullanıcılar, daha sonra uygulamayı tek bir tıklamayla yükleyebilir. Daha fazla bilgi için [ClickOnce kullanarak masaüstü uygulaması dağıtma](how-to-publish-a-clickonce-application-using-the-publish-wizard.md) (C# ve Visual Basic). İçin C++/CLR, bkz: [ClickOnce kullanarak yerel bir uygulama dağıtma](/cpp/ide/clickonce-deployment-for-visual-cpp-applications) veya C /C++, bkz: [bir kurulum projesi kullanarak yerel bir uygulama dağıtma](/cpp/ide/walkthrough-deploying-a-visual-cpp-application-by-using-a-setup-project).

## <a name="publish-to-microsoft-store"></a>Microsoft Store için yayımlama

Visual Studio'dan Microsoft Store için dağıtım için uygulama paketi oluşturabilirsiniz.

- **UWP**: Uygulamanızı paketleme ve menü öğeleri kullanarak dağıtın. Daha fazla bilgi için [Visual Studio kullanarak UWP uygulaması paketleme](/windows/uwp/packaging/packaging-uwp-apps).

    ![Uygulama paketi oluşturma](../deployment/media/feature-tour-create-app-package.jpg)

- **Windows Masaüstü**: Microsoft Store Masaüstü Köprüsü'nü kullanarak Visual Studio 2017 sürüm 15.4 başlangıç dağıtabilirsiniz. Bunu yapmak için bir Windows uygulaması paketleme projesi oluşturarak başlayın. Daha fazla bilgi için [bir masaüstü uygulaması için Microsoft Store (Masaüstü köprüsü) paketini](/windows/uwp/porting/desktop-to-uwp-packaging-dot-net).

    ![Masaüstü köprüsü](../deployment/media/feature-tour-desktop-bridge.png)

## <a name="deploy-to-a-device-uwp"></a>Bir cihaz (UWP) dağıtma

Bir cihazda test etmek için bir UWP uygulaması dağıtıyorsanız, bkz. [Visual Studio'da uzak bir makinede çalıştırmak UWP uygulamaları](../debugger/run-windows-store-apps-on-a-remote-machine.md).

## <a name="create-an-installer-package-windows-desktop"></a>Bir yükleyici paketi (Windows Masaüstü) oluştur

Bir masaüstü uygulamasının karmaşık bir kurulum daha ihtiyaç duyuyorsanız [ClickOnce](how-to-publish-a-clickonce-application-using-the-publish-wizard.md) sağlayabilir, bir Windows Installer paketi (MSI veya EXE yükleme dosyası) veya özel bir önyükleyici oluşturabilirsiniz.

- Bir MSI tabanlı yükleyicide paket kullanılarak oluşturulabilir. [WiX Toolset Visual Studio 2017 uzantısı](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension). Bu bir komut satırı araç setidir.

- Bir MSI ya da EXE Yükleyici paketi kullanılarak oluşturulabilir. [InstallShield](https://www.flexerasoftware.com/producer/products/software-installation/installshield-software-installer/tab/requirements) Flexera yazılım. InstallShield, Visual Studio 2017 ve sonraki sürümlerine (Community Edition desteklenmiyor) kullanılabilir. InstallShield Limited Edition'ın artık Visual Studio'ya dahildir ve Visual Studio 2017 ve sonraki sürümlerinde desteklenmeyen unutmayın. danışın [Flexera yazılım](http://learn.flexerasoftware.com/content/IS-EVAL-InstallShield-Limited-Edition-Visual-Studio) gelecekteki kullanılabilirliği hakkında.

- Bir MSI ya da EXE Yükleyici paketi, using a Setup project (vdproj) oluşturulabilir. Bu seçeneği kullanmak için yükleme [Visual Studio yükleyici projeleri uzantısı](https://marketplace.visualstudio.com/items?itemName=VisualStudioProductTeam.MicrosoftVisualStudio2017InstallerProjects#overview).

- Ayrıca, Masaüstü uygulamaları için önkoşul bileşenleri bir önyükleyici olarak bilinen genel bir yükleyici yapılandırarak yükleyebilirsiniz. Daha fazla bilgi için [Uygulama dağıtımının önkoşulları](../deployment/application-deployment-prerequisites.md).

## <a name="deploy-to-test-lab"></a>Laboratuvar test etmek için dağıtma

Daha karmaşık geliştirme ve test uygulamalarınızı sanal ortamlara dağıtarak etkinleştirebilirsiniz. Daha fazla bilgi için [bir laboratuvar ortamında Test](../test/lab-management/using-a-lab-environment-for-your-application-lifecycle.md).

## <a name="continuous-deployment"></a>Sürekli dağıtım

Azure işlem hatları, uygulamanızı sürekli dağıtımını etkinleştirmek için kullanabilirsiniz. Daha fazla bilgi için [Azure işlem hatları](/azure/devops/pipelines/index?view=vsts) ve [azure'a Dağıt](/azure/devops/deploy-azure/index?view=vsts).

## <a name="deployment-for-other-app-types"></a>Diğer uygulama türleri için dağıtım

| Uygulama türü | Dağıtım Senaryosu | Bağlantı |
| --- | --- | --- |
| **Office uygulama** | Bir eklenti Office Visual Studio'dan yayımlayabilirsiniz. | [Office eklentinizi yayımlama ve dağıtma](https://dev.office.com/docs/add-ins/publish/publish) |
| **WCF veya OData hizmeti** | Diğer uygulamalar, web sunucusuna dağıttığınız WCF RIA hizmetlerini kullanabilir. | [Geliştirme ve WCF veri hizmetlerini dağıtma](/dotnet/framework/data/wcf/developing-and-deploying-wcf-data-services) |
| **LightSwitch** | LightSwitch, Visual Studio 2017'den itibaren artık desteklenir, ancak yine de Visual Studio 2015 ve daha önce dağıtılabilir. | [LightSwitch uygulamalarını dağıtma](https://msdn.microsoft.com/Library/4818d933-295c-4ecc-9148-7ad9ca28dcdb) |

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticide, farklı uygulamalar için dağıtım seçeneklerini hızlı bir bakış sürdü.

> [!div class="nextstepaction"]
> [Hangi Yayımlama seçenekleri benim için uygun?](deploying-applications-services-and-components-resources.md#what-publishing-options-are-right-for-me)
