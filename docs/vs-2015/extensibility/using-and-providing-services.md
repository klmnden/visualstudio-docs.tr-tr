---
title: Hizmetleri kullanma ve sağlama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- examples [Visual Studio SDK], services
- Visual Studio, services
- services
ms.assetid: c0b415ba-b825-4da0-9faf-8a60a663e302
caps.latest.revision: 42
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7f58e29797e9a7760aa0f48c68868199f51b3c92
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68177434"
---
# <a name="using-and-providing-services"></a>Hizmetleri Kullanma ve Sağlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir sözleşme iki Vspackage'lar arasında olan bir hizmettir. Bir VSPackage'ı kullanmak başka bir VSPackage arabirimleri belirli bir kümesini sunar. Örneğin, [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] sunar <xref:Microsoft.VisualStudio.Shell.Interop.SVsActivityLog> isteğe bağlı olarak bir Vspackage'e yükleri hizmet. Bu hizmet sağlayan <xref:Microsoft.VisualStudio.Shell.Interop.IVsActivityLog> etkinlik günlüğüne yazmak için kullanılan arabirim. Daha fazla bilgi için [nasıl yapılır: Etkinlik günlüğü'nün](../extensibility/how-to-use-the-activity-log.md).  
  
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
  
 [Nasıl yapılır: Hizmet Alma](../extensibility/how-to-get-a-service.md)  
 İstek anlatılmaktadır (kullanabilir) bir hizmet.  
  
 [Nasıl yapılır: Hizmet Sağlama](../extensibility/how-to-provide-a-service.md)  
 Bir hizmetin nasıl ele alınmaktadır.  
  
 [Nasıl yapılır: Zaman Uyumsuz Visual Studio Hizmeti Sağlama](../extensibility/how-to-provide-an-asynchronous-visual-studio-service.md)  
 Zaman uyumsuz bir hizmetin nasıl ele alınmaktadır.  
  
 [Nasıl yapılır: Hizmetlerde Sorun Giderme](../extensibility/how-to-troubleshoot-services.md)  
 Ortak sorunları açıklar ve bunların çözümleri sunar.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Visual Studio SDK](../extensibility/visual-studio-sdk.md)
