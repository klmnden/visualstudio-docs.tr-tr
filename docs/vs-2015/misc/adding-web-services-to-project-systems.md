---
title: Proje sistemleri için Web Hizmetleri ekleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: devlang-csharp
ms.topic: conceptual
helpviewer_keywords:
- project systems, adding Web services
- Web services, adding to VSPackage project systems
ms.assetid: 8efa078b-68b2-45a2-9be2-44f807bc0d7f
caps.latest.revision: 8
manager: jillfra
ms.openlocfilehash: 8143db95d2f892c7e3438f240aa5f22cdda53c7f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54766066"
---
# <a name="adding-web-services-to-project-systems"></a>Proje sistemleri için Web Hizmetleri ekleme
XML Web Hizmetleri, genel olarak, SOAP (Basit Nesne Erişim Protokolü) protokolünü kullanarak proje sistemi programlı bilgi döndüren URL'yi adreslenebilir kaynaklardır. VSPackage proje sisteminizi kullanarak Web Hizmetleri tümleştirebilirsiniz <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddProjectItemDlg2> arabirimi.  
  
### <a name="to-add-a-web-service-to-your-project-system"></a>Bir Web hizmeti projesi sisteminize eklemek için  
  
1.  Çağrı `QueryService` için <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddProjectItemDlg2> aracılığıyla arabirim <xref:Microsoft.VisualStudio.Shell.Interop.SVsAddWebReferenceDlg> hizmeti.  
  
2.  Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2.AddWebReferenceDlg%2A> yöntemi. İçinde geçirirseniz `pDiscoverySession` parametre olarak `NULL`bulma oturumunda sizin için oluşturulur ve böylece tarafından kullanmak için kullanılabilir oturum önbelleğe alınmış <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2> arabirimi. <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2.AddWebReferenceDlg%2A> yöntemi, bir işaretçi döndürür <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoveryResult2>.  
  
3.  Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoveryResult.AddWebReference%2A> yöntemi. Web hizmeti başvuruları klasörü Otomasyon nesnesi içinde geçirin `pUnkWebReferenceFolder` parametresi. Visual Studio ortamını, ardından Web hizmeti zaten mevcut olup olmadığını denetler. Web hizmeti mevcut değilse, ortam indirir ve Web hizmeti bir klasörü ve klasörün alt düğümleri (.wsdl dosyaları gibi) ek tüm dosyaları ekler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoveryResult>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoverySession>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsDiscoveryService>