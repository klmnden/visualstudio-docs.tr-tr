---
title: URL Seçici iletişim kutusu (SharePoint Geliştirme)
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.VWD.URLPicker
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, URL picker
- SharePoint development in Visual Studio, designer
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 991693c3379e008a2a907efd3127290c7e804c22
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66261939"
---
# <a name="url-picker-dialog-box-sharepoint-development-in-visual-studio"></a>URL Seçici iletişim kutusu (Visual Studio'da SharePoint Geliştirme)
  URL Seçici iletişim kutusu içinde SharePoint çalıştıran yerel sunucu ana sayfa dosyası veya projenizdeki veya bulunan görüntü dosyaları gibi dosyaları seçebilirsiniz.

 Özellik ayarlamak için bir dosya seçmek için seçeneği varsa, bu iletişim kutusu görüntülenir. Üç nokta düğmesini seçerek bu iletişim kutusunu açabilirsiniz (![ASP.NET Mobil Tasarımcısı elips](../sharepoint/media/mwellipsis.gif "ASP.NET Mobil Tasarımcısı elips")) çeşitli özelliklerinde yanındaki **özellikleri** penceresi. Belirli öznitelikler için değerleri atadığınızda üç nokta düğmesini de bir IntelliSense komut istemi görünür **kaynak** Tasarımcı görünümü.

## <a name="uielement-list"></a>UIElement listesi
 **Proje klasörleri** proje ya da SharePoint çalıştıran yerel sunucu üzerinde tanımlanan klasörlerin listesini görüntüler. Alt klasörleri görüntülemek için genişletme düğmesini seçin.

 Genişletin **proje** düğümünü, projenizdeki dosyaları seçin. İletişim kutusundaki olarak seçilebilir görünmesi için projenizdeki dosyaları aşağıdaki ölçütleri karşılaması gerekir:

- Dosya eşlenmiş bir klasörde bulunmalıdır.

- Dosya çözüm paketine eklenmesi gerekir.

- Dosya başka bir projede yer almamalıdır.

  Bu ölçütleri karşılamayan dosyalara başvurmak istiyorsanız, dosyanın yolu el ile girmek zorunda.

  Genişletin **sunucu** düğümünü SharePoint çalıştıran yerel sunucu üzerinde bulunan dosyaları seçin. Bu dosyalar olarak seçilebilir iletişim kutusunda görünmesi için aşağıdaki ölçütleri karşılaması gerekir:

- Dosya aşağıdaki eşlenen klasörler birinde bulunmalıdır: **Görüntüleri**, **düzenleri**, veya **ControlTemplates**.

- Dosyanın SharePoint içerik veritabanı bulunamıyor.

  Bu ölçütleri karşılamayan dosyalara başvurmak istiyorsanız, dosyanın yolu el ile girmek zorunda.

  **Klasörünün içeriğini** seçili klasörde bulunan dosyaları listesini görüntüler. Bir dosya seçin ve ardından **Tamam** düğmesine iletişim kutusunu kapatmak ve onu çağıran işleme seçiminizi göndermek.

  **Dosya türü** görevin yapmakta olduğunuz için uygun olan dosyalar listesinden seçim yapmanızı sağlar.

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint için uygulama sayfaları oluşturma](../sharepoint/creating-application-pages-for-sharepoint.md)
- [SharePoint için Web bölümleri oluşturma](../sharepoint/creating-web-parts-for-sharepoint.md)
- [Web bölümleri veya uygulama sayfaları için yeniden kullanılabilir denetimler oluşturma](../sharepoint/creating-reusable-controls-for-web-parts-or-application-pages.md)
