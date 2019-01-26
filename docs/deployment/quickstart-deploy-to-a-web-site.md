---
title: Bir Web sitesi için yayımlama
ms.date: 06/22/2018
ms.topic: quickstart
helpviewer_keywords:
- deployment, website
ms.assetid: fc82b1f1-d342-4b82-9a44-590479f0a895
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5f26bab92d2004969c5cbd83cd9c7eef36f483c6
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54936339"
---
# <a name="publish-a-web-app-to-a-web-site-using-visual-studio"></a>Visual Studio kullanarak bir web sitesi için bir Web uygulaması yayımlama

Kullanabileceğiniz **Yayımla** ASP.NET, ASP.NET Core, .NET Core ve Python uygulamaları bir Web sitesine Visual Studio'dan yayımlamak için aracı. Node.js için adımları desteklenir ancak kullanıcı arabirimi farklıdır.

[!INCLUDE [quickstart-prereqs](includes/quickstart-prereqs.md)]

## <a name="publish-to-a-web-site"></a>Bir Web sitesi için yayımlama

1. Çözüm Gezgini'nde projeye sağ tıklayıp seçin **Yayımla** (veya **derleme** > **Yayımla** menü öğesi).

    ![Çözüm Gezgini'nde proje bağlam menüsünde Yayımla komutunu](../deployment/media/quickstart-publish.png "seçin yayımlama")

1. Tüm yayımlama profilleri, daha önce yapılandırdıysanız **Yayımla** bölmesi görünür. Seçin **yeni profil oluşturma**.

1. İçinde **yayımlama hedefi çekme** iletişim kutusunda, seçin **IIS, FTP, vb**.

    ![IIS, FTP, vb.'yi seçin.](../deployment/media/quickstart-publish-iis-ftp.png "seçin IIS, FTP, vb..")

1. **Yayımla**’yı seçin. Profil yayımlama Ayarları iletişim kutusu açılır.

    ![Klasör Seç](../deployment/media/quickstart-publish-settings-web.png "klasörü seçin")

1. İçinde **yayımlama yöntemi** alan, bir yöntem gibi seçin **Web dağıtımı** veya **FTP**. Gördüğünüz ayarları sonraki yayımlama yönteminize karşılık gelir. Web dağıtımı IIS sunucuları için Web uygulamaları ve Web siteleri dağıtımını basitleştirir ve sunucu üzerindeki bir uygulama olarak yüklenmelidir. Kullanım [Web Platformu yükleyicisi](https://www.microsoft.com/web/downloads/platform.aspx) yükleyin.

1. Yayımlama yöntemi için gerekli ayarları yapılandırın ve seçin **bağlantıyı doğrula**. Sunucu veya hedef kullanılabilir ve ayarlarınızın doğru olduğundan, bağlantı belirten bir ileti doğrulanır ve yayımlamak hazırız.

    ![Bağlantınızı doğrulama](../deployment/media/quickstart-publish-web-deploy.png "bağlantınızı doğrulama")

1. Seçin **ayarları** gibi bir hata ayıklama veya sürüm yapılandırmasına dağıtın ve ardından diğer dağıtım ayarlarını yapılandırmak için **Kaydet**. Uzaktan hata ayıklaması, hata ayıklama yapılandırması gereklidir.

1. Yayımlamak için seçin **Yayımla**. Dağıtım ilerleme durumu ve sonuçları çıktı penceresini gösterir.

## <a name="next-steps"></a>Sonraki adımlar

Bu hızlı başlangıçta, bir yayımlama profili oluşturmak için Visual Studio kullanmayı öğrendiniz. Ayrıca bir yayımlama yapılandırabilirsiniz alarak profili yayımlama ayarları.

> [!div class="nextstepaction"]
> [Yayımlama ayarlarını içeri aktarma ve IIS’ye dağıtma](tutorial-import-publish-settings-iis.md)
