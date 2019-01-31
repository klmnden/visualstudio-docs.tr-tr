---
title: Azure App Service’e yayımlama
ms.date: 01/29/2019
ms.topic: quickstart
helpviewer_keywords:
- deployment, website
ms.assetid: fc82b1f1-d342-4b82-9a44-590479f0a895
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- azure
ms.openlocfilehash: 114c6aca7ec7ed05858868b22f7547b0a071420f
ms.sourcegitcommit: e3d96b20381916bf4772f9db52b22275763bb603
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55483763"
---
# <a name="publish-a-web-app-to-azure-app-service-using-visual-studio"></a>Visual Studio kullanarak Azure App Service'e bir Web uygulaması yayımlama

Azure App Service veya Azure App Service (kapsayıcılar kullanarak) Linux ASP.NET, ASP.NET Core, Node.js ve .NET Core uygulamaları yayımlayın aşağıdaki yöntemlerden birini kullanarak.

* Azure DevOps ile sürekli (veya otomatik) dağıtımı uygulamalar için kullanmak [Azure işlem hatları](https://docs.microsoft.com/azure/devops/pipelines/get-started-yaml?view=azdevops).

* Tek seferlik (veya elle) dağıtımı uygulamalar için kullanmak **Yayımla** Azure App Service veya App Service (kapsayıcılar kullanarak) Linux için ASP.NET, ASP.NET Core, Node.js ve .NET Core uygulamaları dağıtmak için Visual Studio araç. Python uygulamaları için adımları takip edin [Python - Azure App Service'e yayımlama](../python/publishing-python-web-applications-to-azure-from-visual-studio.md).

Bu makalede nasıl kullanılacağını **Yayımla** tek seferlik bir dağıtım için aracı.

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
