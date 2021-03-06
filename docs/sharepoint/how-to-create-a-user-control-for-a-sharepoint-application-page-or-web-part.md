---
title: SharePoint uygulama sayfası veya web bölümü için kullanıcı denetimi oluşturma
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- user controls [SharePoint development in Visual Studio], creating
- user controls [SharePoint development in Visual Studio], adding
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 3a88a59e9b87a193329433e5eb0625afa1428026
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66401488"
---
# <a name="how-to-create-a-user-control-for-a-sharepoint-application-page-or-web-part"></a>Nasıl yapılır: Bir SharePoint uygulama sayfası veya web bölümü için bir kullanıcı denetimi oluşturma
  SharePoint çözümünüz için özel işlevler sağlayan özel kullanıcı denetimi oluşturabilir ve projenize içinde bu işlevi kullanabilirsiniz. Bir web bölümü veya uygulamadaki kullanıcı denetimleri dahil edebileceğiniz sayfasında, diğer ASP.NET denetimleri ve SharePoint denetimleri ekleyin ve denetimi için özellikleri ve yöntemleri tanımlar. Kullanıcı denetimleri hakkında daha fazla bilgi için bkz: [web bölümleri veya uygulama sayfaları için yeniden kullanılabilir denetimler oluşturma](../sharepoint/creating-reusable-controls-for-web-parts-or-application-pages.md) ve [kullanıcı denetimleri ve SharePoint Server denetimlerinde](https://blogs.msdn.microsoft.com/kaevans/2011/04/28/user-controls-and-server-controls-in-sharepoint/).

### <a name="to-create-a-user-control-for-sharepoint"></a>SharePoint için bir kullanıcı denetimi oluşturmak için

1. Visual Studio'da SharePoint projesi oluşturun veya açın.

     Bkz: [SharePoint projesi ve proje öğesi şablonları](../sharepoint/sharepoint-project-and-project-item-templates.md).

2. İçinde **Çözüm Gezgini**, proje düğümünü seçin.

3. Menü çubuğunda, **proje** > **Yeni Öğe Ekle**.

     **Yeni Öğe Ekle** iletişim kutusu açılır.

4. İçinde **yüklü** bölmesinde seçin **Office/SharePoint** düğümü.

5. SharePoint şablonları listesinde seçin **kullanıcı denetimi (yalnızca Grup çözümü)** .

    > [!NOTE]
    > Kullanıcı denetimleri, yalnızca Grup çözümlerinde çalışır.

6. İçinde **adı** kutusunda, kullanıcı denetimi için bir ad belirtin ve ardından **Ekle** düğmesi.

     Visual Studio, birçok klasörleri ve dosyaları projenize ekler. Bu dosyalar hakkında daha fazla bilgi için bkz. [web bölümleri veya uygulama sayfaları için yeniden kullanılabilir denetimler oluşturma](../sharepoint/creating-reusable-controls-for-web-parts-or-application-pages.md).

     Varsayılan olarak, kullanıcı denetimi dosyası görünür **kaynak** Visual Web Developer tasarımcısını görünümü. Bu görünümde, denetimin XML işaretlemesini düzenleyebilirsiniz. Geçebilirsiniz **tasarım** denetimlerden sürükleyerek denetimin görsel olarak tasarlamak istiyorsanız görüntülemek **araç kutusu**. Bkz: [Tasarım görünümü, Web sayfası tasarımcısı](/previous-versions/aspnet/ms178149\(v\=vs.100\)).

7. Denetimde gerçekleşen olayları işlemek istiyorsanız, kullanıcı denetimi kod dosyası için kodu ekleyin.

     Bu dosya görünür **Çözüm Gezgini** altında kullanıcı Denetim dosyası ve bir *.cs* veya *.vb* projenin dile bağlı olarak bir uzantı.

## <a name="see-also"></a>Ayrıca bkz.
- [Web bölümleri veya uygulama sayfaları için yeniden kullanılabilir denetimler oluşturma](../sharepoint/creating-reusable-controls-for-web-parts-or-application-pages.md)
- [SharePoint için uygulama sayfaları oluşturma](../sharepoint/creating-application-pages-for-sharepoint.md)
- [SharePoint için Web bölümleri oluşturma](../sharepoint/creating-web-parts-for-sharepoint.md)
