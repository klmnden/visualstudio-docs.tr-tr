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
ms.openlocfilehash: 862310c8c763ce366798bfacd4f4759d606bb33c
ms.sourcegitcommit: 53bc4c11b82882ab658e34c65ae374060f823531
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71128205"
---
# <a name="deploy-an-app-to-a-local-folder-using-visual-studio"></a>Visual Studio kullanarak bir uygulamayı yerel bir klasöre dağıtma

**Yayımla** aracını, Visual Studio 'dan yerel bir klasöre ASP.NET, ASP.NET Core, .NET Core ve Python uygulamaları yayımlamak için kullanabilirsiniz. Node. js için, adımlar desteklenir, ancak kullanıcı arabirimi farklıdır.

[!INCLUDE [quickstart-prereqs](includes/quickstart-prereqs.md)]

> [!NOTE]
> Bir Windows masaüstü uygulamasını yerel bir klasöre yayımlamanız gerekiyorsa bkz. ClickOnce (C# veya Visual Basic) [kullanarak masaüstü uygulaması dağıtma](how-to-publish-a-clickonce-application-using-the-publish-wizard.md) . /CLI C++için bkz. [ClickOnce kullanarak yerel uygulama dağıtma](/cpp/windows/clickonce-deployment-for-visual-cpp-applications) veya C/C++için bkz. [Kurulum projesi kullanarak yerel uygulama dağıtma](/cpp/windows/walkthrough-deploying-a-visual-cpp-application-by-using-a-setup-project).

## <a name="deploy-to-a-local-folder"></a>Yerel klasöre dağıtma

1. Çözüm Gezgini, projeye sağ tıklayın ve **Yayımla** ' yı seçin (veya **Yapı** > **Yayımla** menü öğesini kullanın).

    ![Çözüm Gezgini içindeki proje bağlam menüsündeki Yayımla komutu](../deployment/media/quickstart-publish.png "Yayımla") ' yı seçin

1. Daha önce herhangi bir yayımlama profili yapılandırdıysanız, **Yayımla** bölmesi görüntülenir. **Yeni Profil oluştur**' u seçin.

1. **Bir Yayımla hedefi seç** Iletişim kutusunda **klasör**' i seçin.

    ![Yerel klasörü Yayımla hedefi olarak Seç](../deployment/media/quickstart-publish-folder.png "Klasör Seç")

1. Bir yol girin veya yerel bir klasör belirtmek için **Araştır** ' ı seçin.

1. **Yayımla**’yı seçin. Visual Studio projeyi oluşturur ve belirtilen klasöre yayımlar. Bir profil Özeti gösteren proje özellikleri **Yayımla** bölmesi görüntülenir.

    ![Profil özetini gösteren özellik bölmesini Yayımla](../deployment/media/quickstart-publish-folder-summary.png)

1. Dağıtım ayarlarını yapılandırmak için profil özetinde **Yapılandır** ' ı seçin ve **Ayarlar** sekmesini seçin.

    ![Profil ayarları](../deployment/media/quickstart-profile-settings.png "Profil ayarları")

1. Bir hata ayıklama veya sürüm yapılandırması dağıtıp dağıtmayacağı gibi seçenekleri yapılandırın ve ardından **Kaydet**' i seçin.

1. Yeniden yayımlamak için **Yayımla**' yı seçin.

Yayınlanan dosyaları dilediğiniz gibi dağıtın. Örneğin, bunları bir *. zip* dosyasında paketleyebilir, basit bir kopyalama komutu kullanabilir veya istediğiniz herhangi bir yükleme paketiyle dağıtabilirsiniz.

## <a name="next-steps"></a>Sonraki adımlar

- [Yayımla aracı ile .NET Core Uygulaması dağıtma](/dotnet/core/deploying/deploy-with-vs?toc=/visualstudio/deployment/toc.json&bc=/visualstudio/deployment/_breadcrumb/toc.json)
- [Bir masaüstü uygulamasını Microsoft Store için paketleme (Masaüstü Köprüsü)](/windows/uwp/porting/desktop-to-uwp-packaging-dot-net?toc=/visualstudio/deployment/toc.json&bc=/visualstudio/deployment/_breadcrumb/toc.json)
- .Net [.NET Framework ve uygulamaları dağıtma](/dotnet/framework/deployment/)
