---
title: Bir ASP.NET Core Docker kapsayıcısı Azure App Service'e dağıtma | Microsoft Docs
description: Azure App Service'e bir ASP.NET Core web uygulaması dağıtmak için Docker için Visual Studio Araçları'nı kullanmayı öğrenin
author: ghogen
manager: jillfra
ms.technology: vs-azure
ms.devlang: dotnet
ms.topic: article
ms.date: 03/08/2019
ms.author: ghogen
ms.openlocfilehash: 4f28494bcb15cc66d8563fdc371a33a15fde85a3
ms.sourcegitcommit: 3d37c2460584f6c61769be70ef29c1a67397cf14
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2019
ms.locfileid: "58322684"
---
# <a name="deploy-an-aspnet-core-container-to-azure-app-service-using-visual-studio"></a>Visual Studio kullanarak Azure App Service'e bir ASP.NET Core kapsayıcı dağıtma

Bu öğreticide, kapsayıcıda barındırılan ASP.NET Core web uygulamanızı yayımlamak için Visual Studio kullanarak açıklanmaktadır bir [Azure App Service](/azure/app-service). Azure App Service, Azure'da barındırılan bir tek kapsayıcı web uygulaması için uygun bir hizmettir.

Azure aboneliğiniz yoksa başlamadan önce [ücretsiz bir hesap](https://azure.microsoft.com/free/dotnet/?utm_source=acr-publish-doc&utm_medium=docs&utm_campaign=docs) oluşturun.

## <a name="prerequisites"></a>Önkoşullar

Bu öğreticiyi tamamlamak için:

::: moniker range="vs-2017"
- En son sürümünü yükleyin [Visual Studio 2017](https://azure.microsoft.com/downloads/) "ASP.NET ve web geliştirme" iş yüküyle birlikte sağlanır
::: moniker-end
::: moniker range=">=vs-2019"
- [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019+rc) ile *ASP.NET ve web geliştirme* iş yükü.
::: moniker-end
- Yükleme [Docker Masaüstü](https://docs.docker.com/docker-for-windows/install/)

## <a name="create-an-aspnet-core-web-app"></a>Bir ASP.NET Core web uygulaması oluşturma

Aşağıdaki adımlar Bu öğreticide kullanılan temel bir ASP.NET Core uygulaması oluşturmada size yol.

::: moniker range="vs-2017"
1. Visual Studio menüden **Dosya > Yeni > Proje**.
2. Altında **şablonları** bölümünü **yeni proje** iletişim kutusunda **Visual C# > Web**.
3. Seçin **ASP.NET Core Web uygulaması**.
4. Uygulamanızı yeni bir ad verin (veya varsayılan olması) seçip **Tamam**.
5. Seçin **Web uygulaması**.
6. Denetleme **Docker desteğini etkinleştir** onay kutusu.
7. Seçin **Linux** kapsayıcı türü ve tıklatın **Tamam**. Windows kapsayıcıları, kapsayıcı olarak Azure App Service'e dağıtmak için desteklenmez.
::: moniker-end
::: moniker range=">= vs-2019"
1. Visual Studio Başlangıç penceresinden seçin **yeni bir proje oluşturma**.
1. Seçin **ASP.NET Core Web uygulaması**ve **sonraki**.
1. Uygulamanızı yeni bir ad verin (veya varsayılan olması) ve **Oluştur**.
1. Seçin **Web uygulaması**.
1. SSL desteği kullanarak isteyip istemediğinizi seçin **HTTPS için Yapılandır** onay kutusu.
1. Denetleme **Docker desteğini etkinleştir** onay kutusu.
1. Seçin **Linux** kapsayıcı türü seçeneğine tıklayıp **Oluştur**. Windows kapsayıcıları, kapsayıcı olarak Azure App Service'e dağıtmak için desteklenmez.
::: moniker-end

## <a name="deploy-the-container-to-azure"></a>Azure'da kapsayıcı dağıtma

1. Projenize sağ tıklayın **Çözüm Gezgini** ve **Yayımla**.
1. Yayımlama hedefi iletişim kutusunda seçin **App Service Linux**.
1. App Service'te yayımlayabilirsiniz veya App Service ve Azure Container Registry (ACR) için yayımlayabilirsiniz. Bir Azure Container Registry (ACR) kapsayıcıya yayımlamak için **kapsayıcılar için yeni App Service Oluştur**, tıklatıp **Yayımla**.

   ![Yayımla iletişim kutusunun ekran görüntüsü](media/docker-deploy-app-service/publish-app-service-linux.PNG)

   Azure Container Registry'yi kullanarak olmadan bir Azure App Service yalnızca yayımlamak için **Yeni Oluştur**, tıklatıp **Yayımla**.

1. Azure aboneliğinizle ilişkilendirilmiş hesapla oturum açtıysanız denetleyip bir benzersiz ad, abonelik, kaynak grubu, barındırma planı ve kapsayıcı kayıt defteri (varsa) seçin veya Varsayılanları kabul edin.

   ![Yayımlama ayarları ekran görüntüsü](media/docker-deploy-app-service/publish-app-service-linux2.png)

1. **Oluştur**’u seçin. Kapsayıcı, seçili kaynak grubu ve kapsayıcı kayıt defteri Azure'da dağıtılır. Bu işlem biraz zaman alır. Tamamlandığında, **Yayımla** sekmesi, ne, site URL'si dahil olmak üzere yayımlanan hakkında bilgi gösterir.

   ![Yayımlama sekmesinin Ekran görüntüsü](media/docker-deploy-app-service/publish-succeeded.PNG)

1. Uygulamanız Azure'da beklendiği gibi doğrulamak için site bağlantısına tıklayın.

   ![Web uygulamasının ekran görüntüsü](media/docker-deploy-app-service/web-application-running.png)

1. Yayımlama profili, kaynak grubu ve kapsayıcı kayıt defteri gibi seçtiğiniz tüm ayrıntılarıyla kaydedilir.
1. Aynı yayımlama profili ile yeniden dağıtmak için kullanın **Yayımla** düğmesi **Yayımla** düğmesini **Web yayımlama etkinliği** penceresi ya da projeye sağ tıklayın **Çözüm Gezgini** ve **Yayımla** bağlam menüsünde öğesi.

## <a name="clean-up-resources"></a>Kaynakları temizleme

Bu öğretici ile ilişkili tüm Azure kaynakları kaldırmak için kullanarak kaynak grubu silme [Azure portalında](https://portal.azure.com). Yayımlanan web uygulaması ile ilişkili kaynak grubunu bulmak için **görünümü** > **diğer Windows** > **Web yayımlama etkinliği**, ve dişli simgesini seçin. **Yayımla** sekmesi açılır, hangi kaynak grubunu içerir.

Azure portalında, **kaynak grupları**, Ayrıntılar sayfasını açmak için kaynak grubunu seçin. Doğru kaynak grubu olduğunu doğrulayın ve ardından **kaynak grubunu kaldırma**adını yazın ve seçin **Sil**.

## <a name="next-steps"></a>Sonraki adımlar

Sürekli tümleştirme ve teslim (CI/CD) ile ayarlama [Azure işlem hatları](/azure/devops/pipelines/?view=azure-devops).

## <a name="see-also"></a>Ayrıca bkz.

[Azure Container Registry'ye dağıtma](vs-azure-tools-docker-hosting-web-apps-in-docker.md)