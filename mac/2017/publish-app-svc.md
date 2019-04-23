---
title: Azure App Service’e yayımlama
ms.date: 01/17/2019
ms.topic: quickstart
helpviewer_keywords:
- deployment, website
ms.assetid: 8524a4c5-97a9-41ac-a2a0-034efb9bfc57
author: sayedihashimi
ms.author: sayedha
manager: unniravindranathan
ms.prod: visual-studio-mac
ms.custom: video
ms.workload:
- azure
ms.openlocfilehash: 48cf25a7164fabc96924897c0a4a28bbbe4bea74
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60053591"
---
# <a name="publish-a-web-app-to-azure-app-service-using-visual-studio-for-mac"></a>Mac için Visual Studio kullanarak Azure App Service'e bir Web uygulaması yayımlama

Azure App Service'e ASP.NET Core uygulamaları yayımlamak için Yayımla Aracı'nı kullanabilirsiniz.

## <a name="prerequisites"></a>Önkoşullar

- [Mac için Visual Studio 2017](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs4mac2017) etkin ASP.NET Core ile yüklü.
- Bir Azure aboneliği. Bir abonelik zaten yoksa [ücretsiz olarak kaydolun](https://azure.microsoft.com/free/dotnet/), içeren 200 ABD Doları değerinde kredi 30 gün ve popüler ücretsiz Hizmetleri 12 ay için.
- Bir ASP.NET Core projesi. Bir proje zaten yoksa, şunları yapabilirsiniz [yeni bir tane oluşturun](https://docs.microsoft.com/visualstudio/mac/create-new-projects?view=vsmac-2017).

## <a name="publish-to-azure-app-service"></a>Azure App Service’e yayımlama

 1. Çözüm panelinde projeye sağ tıklayıp seçin **Yayımla**.

    ![Yayımla bağlam menüsü](media/publish-context-menu.png)

 2. Bu proje daha önce Azure App Service'e yayımladıysanız, yayımlama profilini menüsünde görürsünüz. Yayımlama işlemini başlatmak için bu yayımlama profilini seçin.

 3. Bu proje App Service'e ilk kez yayımlamak için seçin **azure'a yayımlama**

    ![App Service bağlam azura'a Yayımla bağlam menüsü](media/publish-to-azure-context-menu.png)

 4. **Azure App Service'e yayımlama** iletişim kutusu açılır ve var olan tüm uygulama hizmetleri gösterilir. Var olan bir uygulama hizmetinde yayımlamak için App Service listeden seçin ve ardından **Yayımla**.

    ![Yayımlama için Azure App Service iletişim kutusu](media/publish-to-app-service-dialog.png)

 5. Yeni bir App Service'ı oluşturmak için tıklayın **yeni** düğmesi.

    ![App Service iletişim yayımlama](media/publish-to-app-service-dialog-new-selected.png)

 6. **Yeni App Service** iletişim kutusu görüntülenir. Bu iletişim kutusunda, yeni uygulama hizmetiniz için ayarları yapılandırabilirsiniz.

    ![Yeni App Service iletişim kutusu](media/publish-new-app-service.png)

    Burada özelleştirme dikkate alınması gereken birkaç seçenek vardır. App Service adı proje adı için varsayılan. Adı kullanılabilir değilse bir uyarı işareti giriş alanı sağ tarafında görünür. Adı bir URL'de kullanılacak geçerli olması gerekir, Web sitesinin URL'sini App Service adı kullanılır.

    App Service kullanarak ilişkili olduğu abonelik değiştirebilirsiniz **abonelik** açılır.

    Mevcut bir seçebileceğiniz **kaynak grubu** veya açılan listeyi kullanarak ile yeni bir tane oluşturabilirsiniz **+** düğmesi.

    App Service planı için varolan bir tanesini seçin veya seçerek yeni bir tane oluşturun **özel** radyo düğmesi.

    Yeni App service'inizi oluşturmak ve bunu projenize yayımlamak için **Oluştur**.

    ' I tıklattıktan sonra **Oluştur** **yeni App Service** iletişim bölümü kapatılmış ve App Service oluşturma başlatıldığını belirten şu iletiyi görmeniz gerekir.

      ![App Service iletisi oluşturun](media/publish-create-app-service-message.png)

    ' I tıklattıktan sonra **Tamam** ileti kapatılır ve projeniz üzerinde çalışmaya devam edebilirsiniz. Durum çubuğu üstünde IDE ile yayımlama işleminin durumunu izleyebilirsiniz. Web uygulamanızı başarıyla yayımlandığında, sitenin varsayılan tarayıcınızda açılır.

## <a name="related-video"></a>İlgili Video

> [!Video https://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Visual-Studio-for-Mac-Publish-to-Azure/player]
