---
title: Yerel klasöre dağıtma
ms.date: 01/29/2019
ms.topic: quickstart
helpviewer_keywords:
- deployment, local folder
ms.assetid: adb461c4-812a-4b8c-b2ab-96002379f6a9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0772e44bf7636edd84c88b3dbaedce7bf2f51604
ms.sourcegitcommit: e3d96b20381916bf4772f9db52b22275763bb603
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55483568"
---
# <a name="deploy-an-app-to-a-local-folder-using-visual-studio"></a>Visual Studio kullanarak yerel bir klasöre uygulama dağıtma

Kullanabileceğiniz **Yayımla** ASP.NET, ASP.NET Core, .NET Core ve Python uygulamaları yerel bir klasöre Visual Studio'dan yayımlamak için aracı. Node.js için adımları desteklenir ancak kullanıcı arabirimi farklıdır.

[!INCLUDE [quickstart-prereqs](includes/quickstart-prereqs.md)]

> [!NOTE]
> Yerel bir klasöre bir Windows Masaüstü uygulamasını yayınlamak gerekiyorsa bkz [ClickOnce kullanarak masaüstü uygulaması dağıtma](how-to-publish-a-clickonce-application-using-the-publish-wizard.md) (C# veya Visual Basic) veya [ClickOnce kullanarak yerel bir uygulama dağıtma](/cpp/ide/clickonce-deployment-for-visual-cpp-applications) (C++).

## <a name="deploy-to-a-local-folder"></a>Yerel klasöre dağıtma

1. Çözüm Gezgini'nde projeye sağ tıklayıp seçin **Yayımla** (veya **derleme** > **Yayımla** menü öğesi).

    ![Çözüm Gezgini'nde proje bağlam menüsünde Yayımla komutunu](../deployment/media/quickstart-publish.png "seçin yayımlama")

1. Tüm yayımlama profilleri, daha önce yapılandırdıysanız **Yayımla** bölmesi görünür. Seçin **yeni profil oluşturma**.

1. İçinde **yayımlama hedefi seçin** iletişim kutusunda **klasör**.

    ![Yayımlama hedefi olarak yerel klasörü seç](../deployment/media/quickstart-publish-folder.png "Klasör Seç")

1. Bir yol girin veya seçin **Gözat** yerel klasörü belirtin.

1. **Yayımla**’yı seçin. Visual Studio projeyi oluşturur ve belirtilen klasöre yayımlar. Proje özelliklerini **Yayımla** bir profili bölmesi görünür, Özet gösteriliyor.

    ![Yayımlama profili Özet gösteren özellik bölmesi](../deployment/media/quickstart-publish-folder-summary.png)

1. Dağıtım ayarları yapılandırmak için seçin **yapılandırma** Özet ve select profilinde **ayarları** sekmesi.

    ![Profil ayarları](../deployment/media/quickstart-profile-settings.png "profil ayarları")

1. Bir hata ayıklama veya sürüm yapılandırmasına dağıtın ve ardından gibi seçenekleri **Kaydet**.

1. Yeniden yayımlamak için seçin **Yayımla**.

Yayımlanan dosyaları istediğiniz herhangi bir şekilde dağıtın. Örneğin, bunları paketleyebilirsiniz bir *.zip* dosya, bir basit kopyası komutunu kullanın veya bunları seçtiğiniz herhangi bir yükleme paketi ile birlikte dağıtabilirsiniz.

## <a name="next-steps"></a>Sonraki adımlar

- [Yayımla aracı ile .NET Core Uygulaması dağıtma](/dotnet/core/deploying/deploy-with-vs?toc=/visualstudio/deployment/toc.json&bc=/visualstudio/deployment/_breadcrumb/toc.json)
- [Bir masaüstü uygulamasını Microsoft Store için paketleme (Masaüstü Köprüsü)](/windows/uwp/porting/desktop-to-uwp-packaging-dot-net?toc=/visualstudio/deployment/toc.json&bc=/visualstudio/deployment/_breadcrumb/toc.json)
- (.NET) [.NET Framework ve uygulamaları dağıtma](/dotnet/framework/deployment/)
