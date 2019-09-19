---
title: Bir Web sitesine yayımlama
ms.date: 01/29/2019
ms.topic: quickstart
helpviewer_keywords:
- deployment, website
ms.assetid: fc82b1f1-d342-4b82-9a44-590479f0a895
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1236c3057cd209bd5c7c81304a2168704927c506
ms.sourcegitcommit: 53bc4c11b82882ab658e34c65ae374060f823531
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71127931"
---
# <a name="publish-a-web-app-to-a-web-site-using-visual-studio"></a>Web uygulamasını Visual Studio kullanarak Web sitesinde yayımlama

**Yayımla** aracını, ASP.NET, ASP.NET Core, .NET Core ve Python uygulamalarını Visual Studio 'daki bir Web sitesine yayımlamak için kullanabilirsiniz. Node. js için, adımlar desteklenir, ancak kullanıcı arabirimi farklıdır.

[!INCLUDE [quickstart-prereqs](includes/quickstart-prereqs.md)]

> [!NOTE]
> Bir Windows masaüstü uygulamasını bir ağ dosya paylaşımında yayımlamanız gerekiyorsa bkz. ClickOnce (C# veya Visual Basic) [kullanarak masaüstü uygulaması dağıtma](how-to-publish-a-clickonce-application-using-the-publish-wizard.md) . /CLI C++için bkz. [ClickOnce kullanarak yerel uygulama dağıtma](/cpp/windows/clickonce-deployment-for-visual-cpp-applications) veya C/C++için bkz. [Kurulum projesi kullanarak yerel uygulama dağıtma](/cpp/windows/walkthrough-deploying-a-visual-cpp-application-by-using-a-setup-project).

## <a name="publish-to-a-web-site"></a>Web sitesinde yayımlama

1. Çözüm Gezgini, projeye sağ tıklayın ve **Yayımla** ' yı seçin (veya **Yapı** > **Yayımla** menü öğesini kullanın).

    ![Çözüm Gezgini içindeki proje bağlam menüsündeki Yayımla komutu](../deployment/media/quickstart-publish.png "Yayımla") ' yı seçin

1. Daha önce herhangi bir yayımlama profili yapılandırdıysanız, **Yayımla** bölmesi görüntülenir. **Yeni Profil oluştur**' u seçin.

1. İçinde **yayımlama hedefi çekme** iletişim kutusunda, seçin **IIS, FTP, vb**.

    ![IIS, FTP, vb. seçin.](../deployment/media/quickstart-publish-iis-ftp.png "IIS, FTP, vb. seçin.")

1. **Yayımla**’yı seçin. Profil yayımlama ayarları iletişim kutusu açılır.

    ![Klasör Seç](../deployment/media/quickstart-publish-settings-web.png "Klasör Seç")

1. **Yayımla yöntemi** alanında **Web dağıtımı** veya **FTP**gibi bir yöntem seçin. Sonraki gördüğünüz ayarlar yayımlama yönteminiz için karşılık gelir. Web Dağıtımı, Web uygulamalarının ve Web sitelerinin IIS sunucularına dağıtımını basitleştirir ve sunucuda bir uygulama olarak yüklenmelidir. Yüklemek için [Web Platformu Yükleyicisi](https://www.microsoft.com/web/downloads/platform.aspx) 'ni kullanın.

1. Yayımla yöntemi için gerekli ayarları yapılandırın ve **bağlantıyı doğrula**' yı seçin. Sunucu veya hedef kullanılabiliyorsa ve ayarlarınız doğruysa, bağlantının doğrulanacağını belirten bir ileti ve yayımlamaya hazırsınız demektir.

    ![Bağlantınızı doğrulama](../deployment/media/quickstart-publish-web-deploy.png "Bağlantınızı doğrulama")

1. Bir hata ayıklama veya sürüm yapılandırması dağıtıp dağıtmayacağı gibi diğer dağıtım ayarlarını yapılandırmak için **ayarları** seçin ve ardından **Kaydet**' i seçin. Uzaktan hata ayıklaması yapıyorsanız, hata ayıklama yapılandırması gerekir.

1. Yayımlamak için **Yayımla**' yı seçin. Çıkış penceresinde dağıtım ilerleme durumu ve sonuçları gösterilir.

## <a name="next-steps"></a>Sonraki adımlar

Bu hızlı başlangıçta, bir yayımlama profili oluşturmak için Visual Studio 'Yu nasıl kullanacağınızı öğrendiniz. Yayımlama ayarlarını içeri aktararak de bir yayımlama profili yapılandırabilirsiniz.

> [!div class="nextstepaction"]
> [Yayımlama ayarlarını içeri aktarma ve IIS’ye dağıtma](tutorial-import-publish-settings-iis.md)
