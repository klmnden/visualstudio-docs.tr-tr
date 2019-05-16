---
title: Linux üzerinde App Service'e yayımlama
ms.date: 01/29/2019
ms.topic: quickstart
helpviewer_keywords:
- deployment, website
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- azure
ms.openlocfilehash: 9609b636c6121ec2dac41559344485d4048e9cc5
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65680071"
---
# <a name="publish-an-aspnet-core-app-to-app-service-on-linux-using-visual-studio"></a>Visual Studio kullanarak Linux üzerinde App Service'e bir ASP.NET Core uygulaması yayımlama

Visual Studio 2017 sürüm 15.7 başlayarak, Azure App Service (kapsayıcılar kullanarak) Linux için ASP.NET Core uygulamaları yayımlayabilirsiniz aşağıdaki yöntemlerden birini kullanarak.

* Azure DevOps ile sürekli (veya otomatik) dağıtımı uygulamalar için kullanmak [Azure işlem hatları](https://docs.microsoft.com/azure/devops/pipelines/get-started-yaml?view=azdevops).

* Tek seferlik (veya elle) dağıtımı uygulamalar için kullanmak **Yayımla** (kapsayıcıları kullanarak) Linux için App Service'e ASP.NET Core uygulamaları yayımlamak için Visual Studio araç.

Bu makalede nasıl kullanılacağını **Yayımla** tek seferlik bir dağıtım için aracı.

[!INCLUDE [quickstart-prereqs-azure-linux](includes/quickstart-prereqs-azure-linux.md)]

## <a name="publish-to-app-service-on-linux"></a>Linux üzerinde App Service'e yayımlama

1. Çözüm Gezgini'nde projeye sağ tıklayıp seçin **Yayımla** (veya **derleme** > **Yayımla** menü öğesi).

    ![Çözüm Gezgini'nde proje bağlam menüsünde Yayımla komutunu](../deployment/media/quickstart-publish.png "seçin yayımlama")

1. Tüm yayımlama profilleri, daha önce yapılandırdıysanız **Yayımla** bölmesi görünür, büyük/küçük harf hangi seçin **yeni profil oluşturma**.

1. İçinde **yayımlama hedefi seçin** iletişim kutusunda **App Service Linux**.

    ![Azure uygulama hizmeti seçin](../deployment/media/quickstart-publish-linux.png "Azure uygulama hizmeti seçin")

1. **Yayımla**’yı seçin. **App Service Oluştur** iletişim kutusu görüntülenir. Gerekirse, ardından varsayılan uygulama hizmeti ayarlarını alanları doldurun, size Azure hesabıyla oturum açın.

    ![App Service Oluştur](../deployment/media/quickstart-publish-settings-app-service-linux.png "Azure App Service oluştur")

1. **Oluştur**’u seçin. Visual Studio için Azure App Service uygulama dağıtır ve tarayıcınızda web uygulaması yükler. Proje özelliklerini **Yayımla** site URL'sini ve diğer ayrıntıları bölmesi gösterir.

    ![Yayımlama profili Özet gösteren özellik bölmesi](../deployment/media/quickstart-publish-app-service-summary.png)

## <a name="clean-up-resources"></a>Kaynakları temizleme

Önceki adımlarda, Azure kaynaklarını bir kaynak grubunda oluşturuldu. Gelecekte bu kaynaklara ihtiyaç duymayacağınızı düşünüyorsanız, kaynak grubunu silerek bunları silebilir.
Azure portalında sol menüden seçim yapın **kaynak grupları** seçip **myResourceGroup**.
Kaynak grubunuzun sayfasında, listelenen kaynakları silmek istediğiniz kaynaklar olduğundan emin olun.
Seçin **Sil**, türü **myResourceGroup** metin kutusuna ve ardından **Sil**.

## <a name="next-steps"></a>Sonraki adımlar

Bu hızlı başlangıçta Linux üzerinde App Service'e dağıtımı için bir yayımlama profili oluşturmak için Visual Studio kullanmayı öğrendiniz. Azure'ı kullanarak Linux için yayımlama hakkında daha fazla bilgi isteyebilirsiniz.

> [!div class="nextstepaction"]
> [Linux uygulama hizmeti](/azure/app-service/containers/app-service-linux-intro)
