---
title: Hizmetleri kullanma ve sağlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- examples [Visual Studio SDK], services
- Visual Studio, services
- services
ms.assetid: c0b415ba-b825-4da0-9faf-8a60a663e302
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1c9b0dbf2122b5a76d557cdd70da27660b886041
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66337033"
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
- [Hizmet temel bileşenleri](../extensibility/internals/service-essentials.md) bir Visual Studio hizmetin önemli öğeleri gösterir.

- [Nasıl yapılır: Hizmet alma](../extensibility/how-to-get-a-service.md) istek anlatılmaktadır (kullanabilir) bir hizmet.

- [Nasıl yapılır: Bir hizmetin](../extensibility/how-to-provide-a-service.md) bir hizmetin nasıl ele alınmaktadır.

- [Nasıl yapılır: Zaman uyumsuz bir Visual Studio hizmeti sağlama](../extensibility/how-to-provide-an-asynchronous-visual-studio-service.md) uyumsuz bir hizmet sağlamak nasıl ele alınmaktadır.

- [Nasıl yapılır: Sorun Giderme Hizmetleri](../extensibility/how-to-troubleshoot-services.md) ortak sorunları açıklar ve bunların çözümleri sunar.

## <a name="related-sections"></a>İlgili Bölümler
- [Visual Studio SDK](../extensibility/visual-studio-sdk.md)