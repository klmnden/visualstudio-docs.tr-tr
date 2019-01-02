---
title: Azure App Service’e yayımlama
ms.date: 06/22/2018
ms.topic: quickstart
helpviewer_keywords:
- deployment, website
ms.assetid: fc82b1f1-d342-4b82-9a44-590479f0a895
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- azure
ms.openlocfilehash: 4e7cf13658c33caf6b58d6a4e661a8431f377845
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53853599"
---
# <a name="publish-a-web-app-to-azure-app-service-using-visual-studio"></a>Visual Studio kullanarak Azure App Service'e bir Web uygulaması yayımlama

Kullanabileceğiniz **Yayımla** Azure App Service veya Azure App Service (kapsayıcılar kullanarak) Linux için ASP.NET, ASP.NET Core, Node.js ve .NET Core uygulamaları yayımlamak için aracı. Python uygulamaları için adımları takip edin [Python - Azure App Service'e yayımlama](../python/publishing-python-web-applications-to-azure-from-visual-studio.md).

[!INCLUDE [quickstart-prereqs-azure](includes/quickstart-prereqs-azure.md)]

## <a name="publish-to-azure-app-service"></a>Azure App Service’e yayımlama

1. Çözüm Gezgini'nde projeye sağ tıklayıp seçin **Yayımla** (veya **derleme** > **Yayımla** menü öğesi).

    ![Çözüm Gezgini'nde proje bağlam menüsünde Yayımla komutunu](../deployment/media/quickstart-publish.png "seçin yayımlama")

1. Tüm yayımlama profilleri, daha önce yapılandırdıysanız **Yayımla** bölmesi görünür, büyük/küçük harf hangi seçin **yeni profil oluşturma**.

1. İçinde **yayımlama hedefi seçin** iletişim kutusunda **App Service**.

    ![Azure uygulama hizmeti seçin](../deployment/media/quickstart-publish-azure.png "Azure uygulama hizmeti seçin")

1. **Yayımla**’yı seçin. **App Service Oluştur** iletişim kutusu görüntülenir. Gerekirse, ardından varsayılan uygulama hizmeti ayarlarını alanları doldurun, size Azure hesabıyla oturum açın.

    ![App Service Oluştur](../deployment/media/quickstart-publish-settings-app-service.png "Azure App Service oluştur")

1. **Oluştur**’u seçin. Visual Studio için Azure App Service uygulama dağıtır ve tarayıcınızda web uygulaması yükler. Proje özelliklerini **Yayımla** site URL'sini ve diğer ayrıntıları bölmesi gösterir.

    ![Yayımlama profili Özet gösteren özellik bölmesi](../deployment/media/quickstart-publish-app-service-summary.png)

## <a name="clean-up-resources"></a>Kaynakları temizleme

Önceki adımlarda, Azure kaynaklarını bir kaynak grubunda oluşturuldu. Gelecekte bu kaynaklara ihtiyaç duymayacağınızı düşünüyorsanız, kaynak grubunu silerek bunları silebilir.
Azure portalında sol menüden seçim yapın **kaynak grupları** seçip **myResourceGroup**.
Kaynak grubunuzun sayfasında, listelenen kaynakları silmek istediğiniz kaynaklar olduğundan emin olun.
Seçin **Sil**, türü **myResourceGroup** metin kutusuna ve ardından **Sil**.

## <a name="next-steps"></a>Sonraki adımlar

Bu hızlı başlangıçta, azure'a dağıtım için bir yayımlama profili oluşturmak için Visual Studio kullanmayı öğrendiniz. Ayrıca bir yayımlama yapılandırabilirsiniz alarak profili, Azure App Service ayarlarını yayımlayın.

> [!div class="nextstepaction"]
> [Yayımlama ayarlarını içeri aktarma ve Azure’a dağıtma](tutorial-import-publish-settings-azure.md)
