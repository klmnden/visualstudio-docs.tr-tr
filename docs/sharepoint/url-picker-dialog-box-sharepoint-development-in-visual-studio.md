---
title: URL Seçici iletişim kutusu (Visual Studio'da SharePoint Geliştirme) | Microsoft Docs
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
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: ffeca5bf0149ce5a36e5abb77eab673e87f36dc7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53925907"
---
# <a name="url-picker-dialog-box-sharepoint-development-in-visual-studio"></a>URL Seçici iletişim kutusu (Visual Studio'da SharePoint Geliştirme)
  URL Seçici iletişim kutusu içinde SharePoint çalıştıran yerel sunucu ana sayfa dosyası veya projenizdeki veya bulunan görüntü dosyaları gibi dosyaları seçebilirsiniz.  
  
 Özellik ayarlamak için bir dosya seçmek için seçeneği varsa, bu iletişim kutusu görüntülenir. Üç nokta düğmesini seçerek bu iletişim kutusunu açabilirsiniz (![ASP.NET Mobil Tasarımcısı elips](../sharepoint/media/mwellipsis.gif "ASP.NET Mobil Tasarımcısı elips")) çeşitli özelliklerinde yanındaki **özellikleri** penceresi. Belirli öznitelikler için değerleri atadığınızda üç nokta düğmesini de bir IntelliSense komut istemi görünür **kaynak** Tasarımcı görünümü.  
  
## <a name="uielement-list"></a>UIElement listesi
 **Proje klasörleri**  
 Proje veya SharePoint çalıştıran yerel sunucu üzerinde tanımlanan klasörlerin listesini görüntüler. Alt klasörleri görüntülemek için genişletme düğmesini seçin.  
  
 Genişletin **proje** düğümünü, projenizdeki dosyaları seçin. İletişim kutusundaki olarak seçilebilir görünmesi için projenizdeki dosyaları aşağıdaki ölçütleri karşılaması gerekir:  
  
- Dosya eşlenmiş bir klasörde bulunmalıdır.  
  
- Dosya çözüm paketine eklenmesi gerekir.  
  
- Dosya başka bir projede yer almamalıdır.  
  
  Bu ölçütleri karşılamayan dosyalara başvurmak istiyorsanız, dosyanın yolu el ile girmek zorunda.  
  
  Genişletin **sunucu** düğümünü SharePoint çalıştıran yerel sunucu üzerinde bulunan dosyaları seçin. Bu dosyalar olarak seçilebilir iletişim kutusunda görünmesi için aşağıdaki ölçütleri karşılaması gerekir:  
  
- Dosya aşağıdaki eşlenen klasörler birinde bulunmalıdır: **Görüntüleri**, **düzenleri**, veya **ControlTemplates**.  
  
- Dosyanın SharePoint içerik veritabanı bulunamıyor.  
  
  Bu ölçütleri karşılamayan dosyalara başvurmak istiyorsanız, dosyanın yolu el ile girmek zorunda.  
  
  **Klasör içeriği**  
  Seçilen klasördeki dosyaların bir listesini görüntüler. Bir dosya seçin ve ardından **Tamam** düğmesine iletişim kutusunu kapatmak ve onu çağıran işleme seçiminizi göndermek.  
  
  **Dosya türü**  
  Gerçekleştirdiğiniz görev için uygun olan dosyalar listesinden seçmenize olanak sağlar.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint için uygulama sayfaları oluşturma](../sharepoint/creating-application-pages-for-sharepoint.md)   
 [SharePoint için Web bölümleri oluşturma](../sharepoint/creating-web-parts-for-sharepoint.md)   
 [Web bölümleri veya uygulama sayfaları için yeniden kullanılabilir denetimler oluşturma](../sharepoint/creating-reusable-controls-for-web-parts-or-application-pages.md)   
