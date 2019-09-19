---
title: Bir klasöre yayımlama
ms.date: 04/02/2019
helpviewer_keywords:
- deployment, website, console, publish
ms.assetid: e963fb4b-6d32-4d45-86bb-ef7e4d3028b0
author: sayedihashimi
ms.author: sayedha
manager: unniravindranathan
ms.prod: visual-studio-mac
ms.openlocfilehash: 165cfc38b8289946e0966083785defd18ca87d77
ms.sourcegitcommit: 6993bcb0d2b0067b1b7b7899bfba52c31c70b7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2019
ms.locfileid: "71095416"
---
# <a name="publish-to-a-folder-using-visual-studio-for-mac"></a>Mac için Visual Studio kullanarak bir klasöre yayımlama

.NET Core konsolunu veya ASP.NET Core uygulamalarını bir klasöre yayımlamak için Yayımla aracını kullanabilirsiniz.

## <a name="prerequisites"></a>Önkoşullar

- .NET Core etkinken [Mac Için Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs4mac2019) yüklendi.
- Bir .NET Core konsolu veya ASP.NET Core projesi. Zaten bir projeniz yoksa [Yeni bir tane oluşturabilirsiniz](https://docs.microsoft.com/visualstudio/mac/create-new-projects?view=vsmac-2019).

## <a name="publish-to-folder"></a>Klasöre Yayımlama

Mac için Visual Studio kullanarak .NET Core projelerinizi Yayımla aracını kullanarak bir klasöre yayımlayabilirsiniz. Bir klasöre yayımladıktan sonra, dosyaları farklı bir ortama aktarabilirsiniz. Bir klasöre yayımlamak için aşağıdaki adımları izleyin.

 1. Çözüm Bölmesi projeye sağ tıklayın ve **Yayımla**' yı seçin.

    ![Yayımla bağlam menüsü](media/publish-context-menu.png)

 2. Bu projeyi daha önce yayımladıysanız, menüde Yayımla profilini görürsünüz. Yayımlama işlemini başlatmak için bu profili Yayımla ' yı seçin.

 3. Bu projeyi ilk kez bir klasöre yayımlamak için, **klasöre Yayımla** ' yı seçin.

    ![Klasöre Yayımla bağlam menüsü](media/publish-to-folder-context-menu.png)

 4. **Klasöre Yayımla** iletişim kutusu görüntülenir. Bu iletişim kutusunda projenin yayımlanacağı klasörü özelleştirebilirsiniz. Bunu yapmak için, **Araştır** düğmesini veya bir yolu yapıştırmak için kullanabilirsiniz.

 5. **Yayımla** ' ya tıkladıktan sonra birkaç şey meydana gelir. İlk olarak bir yayımlama profili oluşturulur. Yayımlama profili, yayımlama işlemi sırasında projeye içeri aktarılan bir MSBuild dosyasıdır. Yayımlama işlemi sırasında kullanılan özellikleri içerir. Bu dosyalar içinde `Properties/PublishProfiles` depolanır ve uzantısına `.pubxml`sahiptir. Sonra yayımlama işlemi başlatılır. Mac için Visual Studio ' de durum çubuğunu izleyerek ilerlemeyi izleyebilirsiniz.

    ![Yayımlama durumuyla IDE durum çubuğu](media/publish-to-folder-status-bar.png)

 6. Yayımlama başarıyla tamamlandığında, bir bulucu penceresi Yayımla klasörüne açılır. Şimdi bir yayımlama profili oluşturuldığına göre, Yayımla bağlam menüsünde görüntülenecektir.

    ![Bağlam menüsünü klasör profiliyle Yayımla](media/publish-context-menu-with-folder-profile.png)

 7. Projeyi aynı ayarlarla yeniden yayımlamak için Yayımla bağlam menüsünde profile tıklayabilirsiniz.

## <a name="customize-publish-options"></a>Yayımlama seçeneklerini özelleştirin

Yayımlama profilinin adını değiştirmek için (Yayımla bağlam menüsünde görüntülenir), yayımlama profili dosyasını yeniden adlandırın. Dosyanın (`.puxbml`) uzantısını değiştirmediğinden emin olun.

Yayımlama klasörü yolunu değiştirmek için yayımlama profilini açın ve `publishUrl` değeri düzenleyin.

Kullanılan yapı yapılandırmasını değiştirmek için yayımlama profilindeki `LastUsedBuildConfiguration` özelliği değiştirin.
