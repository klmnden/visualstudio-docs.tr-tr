---
title: Tek dosya oluşturucular ekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- custom tools, implementing
- projects [Visual Studio SDK], extensibility
- projects [Visual Studio SDK], managed custom tools
ms.assetid: fe9ef6b6-4690-4c2c-872c-301c980d17fe
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 728a1748d4c78bd93bf827290404f65607076b6a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53847788"
---
# <a name="implementing-single-file-generators"></a>Tek Dosya Oluşturucular Ekleme
Özel araç — bazen tek dosya oluşturucu olarak da adlandırılır — genişletmek için kullanılan [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)] ve [!INCLUDE[csprcs](../../data-tools/includes/csprcs_md.md)] proje sistemleri [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Özel araç uygulayan bir COM bileşenidir <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator> arabirimi. Bu arabirim kullanarak özel bir araç tek çıktı dosyasına tek bir giriş dosyası dönüştürür. Dönüştürme sonucunu kaynak kodu olabilir veya diğer yararlı olan çıktı. İki örnek özel aracı tarafından oluşturulan kodu dosyalarının bir görsel tasarımcı ve Web Hizmetleri Açıklama Dili (WSDL) kullanılarak oluşturulan dosyaları değişikliklere yanıt olarak oluşturulan kodu verilmiştir.  
  
 Özel bir aracı yüklenir ve giriş dosyası kaydedilir, proje sistemi çağırır <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator.Generate%2A> yöntemi ve bir başvuru geçirir bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsGeneratorProgress> yapabildiği aracın rapor edebilir, ilerleme durumunu kullanıcıya geri çağırma arabirimi.  
  
 Özel aracının oluşturduğu çıkış dosyası bağımlılığı bulunan Giriş dosyası projeye eklenir. Proje sistemi otomatik olarak özel aracın uygulaması tarafından döndürülen dize göre çıktı dosyası adını belirleyen <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator.DefaultExtension%2A>.  
  
 Özel araç uygulamalıdır <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator> arabirimi. İsteğe bağlı olarak, özel araçları desteği <xref:Microsoft.VisualStudio.OLE.Interop.IObjectWithSite> giriş dosyası dışındaki bir kaynaktan bilgi almak için arabirim. Özel araç kullanabilmeniz için herhangi bir durumda, sistem veya kaydetmelisiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] yerel kayıt defteri. Özel Araçlar kaydetme ile ilgili daha fazla bilgi için bkz: [tek dosya oluşturucuları kaydetme](../../extensibility/internals/registering-single-file-generators.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Türleri Görsel Tasarımcıların Kullanımına Sunma](../../extensibility/internals/exposing-types-to-visual-designers.md)