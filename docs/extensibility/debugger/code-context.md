---
title: Kod bağlamı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], contexts
ms.assetid: 65e4d37a-086b-426e-9394-a3534967fd59
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 868fa51d24b0ae3206d55ae8364224dead69e7f7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55003376"
---
# <a name="code-context"></a>Kod bağlamı
İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama, bir **kod bağlamı**:  
  
-   Hata ayıklama Altyapısı'na (DE) bilinen bir konum kod bir soyutlamasıdır sağlar. Çoğu çalışma zamanı mimarileri için bugün, bir kod bağlamı, bir programın yönerge stream'de adresi olarak düşünülebilir. Burada kod yönergeleri ile gösterilebilir değil, nontraditional diller için kod bağlamı başka bir yolla tarafından temsil edilebilir.  
  
-   Hata ayıklama programı yürütme stream'de geçerli konumu açıklar.  
  
-   Yalnızca bir programın bir kesme noktasında ne zaman durdurdu var.  
  
-   İlişkili belge içeriğine sahiptir.  
  
-   Tarafından uygulanan bir [IDebugCodeContext2](../../extensibility/debugger/reference/idebugcodecontext2.md) arabirimi.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Belge bağlamı](../../extensibility/debugger/document-context.md)   
 [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md)