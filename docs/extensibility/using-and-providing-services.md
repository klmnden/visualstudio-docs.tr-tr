---
title: Hizmetleri kullanma ve sağlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- examples [Visual Studio SDK], services
- Visual Studio, services
- services
ms.assetid: c0b415ba-b825-4da0-9faf-8a60a663e302
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f547afd33166a6a7b10284e6cb55e73baeefc861
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53886286"
---
# <a name="using-and-providing-services"></a>Hizmetleri Kullanma ve Sağlama
Bir sözleşme iki Vspackage'lar arasında olan bir hizmettir. Bir VSPackage'ı kullanmak başka bir VSPackage arabirimleri belirli bir kümesini sunar. Örneğin, [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] sunar <xref:Microsoft.VisualStudio.Shell.Interop.SVsActivityLog> isteğe bağlı olarak bir Vspackage'e yükleri hizmet. Bu hizmet sağlayan <xref:Microsoft.VisualStudio.Shell.Interop.IVsActivityLog> etkinlik günlüğüne yazmak için kullanılan arabirim. Daha fazla bilgi için [nasıl yapılır: Etkinlik günlüğü'nün](../extensibility/how-to-use-the-activity-log.md).  
  
 VSPackage'ları, kendi başlarına kullanmanın Hizmetleri sunabilir <xref:Microsoft.VisualStudio.Shell.Interop.IProfferService> arabirimi...  
  
 Visual Studio aşağıdaki gibi önemli hizmetler sunar:  
  
|IDE hizmeti|Açıklama|  
|-----------------|-----------------|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsShell>|Temel işlevleri, VSPackages ve kayıt defteri ile ilgilenen Hizmetleri IDE için erişim sağlar.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsUIShell>|Temel Pencereleme ve araç ve belge pencereleri oluşturma olanağı gibi IDE kullanıcı Arabirimi ile ilgili işlevleri sağlar.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsSolution>|Projeleri listeleme, yeni projeler oluşturmak ve proje değişiklikleri izleme özelliği gibi temel çözümü ile ilgili işlevleri sağlar.|  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Hizmet Temel Bileşenleri](../extensibility/internals/service-essentials.md)  
 Visual Studio hizmeti önemli öğelerini gösterir.  
  
 [Nasıl yapılır: Hizmet alma](../extensibility/how-to-get-a-service.md)  
 İstek anlatılmaktadır (kullanabilir) bir hizmet.  
  
 [Nasıl yapılır: Bir hizmeti sağlama](../extensibility/how-to-provide-a-service.md)  
 Bir hizmetin nasıl ele alınmaktadır.  
  
 [Nasıl yapılır: Bir zaman uyumsuz Visual Studio hizmeti sağlama](../extensibility/how-to-provide-an-asynchronous-visual-studio-service.md)  
 Zaman uyumsuz bir hizmetin nasıl ele alınmaktadır.  
  
 [Nasıl yapılır: Hizmetleri sorunlarını giderme](../extensibility/how-to-troubleshoot-services.md)  
 Ortak sorunları açıklar ve bunların çözümleri sunar.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Visual Studio SDK](../extensibility/visual-studio-sdk.md)