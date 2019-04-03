---
title: Bir klasöre yayımlayın
ms.date: 04/02/2019
ms.topic: quickstart
helpviewer_keywords:
- deployment, website
ms.assetid: e963fb4b-6d32-4d45-86bb-ef7e4d3028b0
author: sayedihashimi
ms.author: sayedha
manager: unniravindranathan
ms.prod: visual-studio-mac
ms.openlocfilehash: 0ab1b01900077fdbad5dec3fb968abcf46db62d8
ms.sourcegitcommit: 509fc3a324b7748f96a072d0023572f8a645bffc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58856534"
---
# <a name="publish-a-web-app-to-a-folder-using-visual-studio-for-mac"></a>Mac için Visual Studio kullanarak bir klasör için bir Web uygulaması yayımlama

ASP.NET Core uygulamaları için bir klasör yayımlamak için Yayımla Aracı'nı kullanabilirsiniz.

## <a name="prerequisites"></a>Önkoşullar

 - [Mac için Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs4mac2019) etkin ASP.NET Core ile yüklü.
 - Bir ASP.NET Core projesi. Bir proje zaten yoksa, şunları yapabilirsiniz [yeni bir tane oluşturun](https://docs.microsoft.com/visualstudio/mac/create-new-projects?view=vsmac-2019).

## <a name="publish-to-folder"></a>Klasöründe yayımlayın

Mac için Visual Studio kullanarak ASP.NET Core projeleriniz Yayımla Aracı'nı kullanarak bir klasöre yayımlayabilirsiniz. Bir klasöre yayımlamadan sonra farklı bir ortama almak için web sunucunuza dosyaları aktarabilirsiniz. Yayımlamak için bir klasör için şu adımları izleyin.

 1. Çözüm panelinde projeye sağ tıklayıp seçin **Yayımla**.

    ![Yayımla bağlam menüsü](media/publish-context-menu.png)

 2. Daha önce bu proje yayımladıysanız, yayımlama profilini menüsünde görürsünüz. Yayımlama işlemini başlatmak için bu yayımlama profilini seçin.

 3. Bu proje için ilk kez bir klasöre yayımlamak için seçin **klasörüne Yayımla**

    ![Klasör içeriği azura'a Yayımla bağlam menüsü](media/publish-to-folder-context-menu.png)

 4. **Yayımlama klasörüne** iletişim kutusu görüntülenir. Bu iletişim kutusunda, projeyi burada yayımlanacak klasörü özelleştirebilirsiniz. Kullanabileceğiniz **Gözat** Bunu yapmak için düğme ya da bir yolda yapıştırın.

 5. ' I tıklattıktan sonra **Yayımla** birkaç şey olur. Önce bir yayımlama profili oluşturulur. Bir yayımlama profili yayımlama işlemi sırasında bir projeye içeri aktarılan bir MSBuild dosyasıdır. Bu yayımlama işlemi sırasında kullanılan özellikler içerir. Bu dosyalar depolanan `Properties/PublishProfiles` ve uzantı `.pubxml`. Ardından, yayımlama işlemi başlatıldı. Mac için Visual Studio durum çubuğunda izleyerek ilerleme durumunu izleyebilirsiniz.

    ![IDE durum çubuğu yayımlama durumu](media/publish-to-folder-status-bar.png)

 6. Yayımlama başarıyla tamamlandıktan sonra yayımlama klasörü için bir Bulucu penceresi açılır. Bir yayımlama profili oluşturulduktan sonra Yayımla bağlam menüsü görüntülenir.

    ![Bağlam menüsü klasörüne profil ile yayımlama](media/publish-context-menu-with-folder-profile.png)

 7. Projenin aynı ayarlarla yeniden yayımlamak için Yayımla bağlam menüsü profile tıklayabilirsiniz.

## <a name="customize-publish-options"></a>Özelleştirme seçenekleri Yayımla

(Bu Yayımla bağlam menüsü görüntülenir) yayımlama profili adını değiştirmek için yayımlama profili dosyasını yeniden adlandırın. Dosya uzantısı değil değiştirdiğinizden emin olun (`.puxbml`).

Yayımlama klasörü yolu değiştirmek için yayımlama profilini açın ve düzenleyin `publishUrl` değeri.

Kullanılan derleme yapılandırmasını değiştirmek için `LastUsedBuildConfiguration` yayımlama profili özelliği.
