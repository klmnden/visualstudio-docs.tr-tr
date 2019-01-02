---
title: Kod bağlamı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], contexts
ms.assetid: 65e4d37a-086b-426e-9394-a3534967fd59
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: bbbeb9eab33bbdad7264a0296a4f6c9f86fb8a5d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53851293"
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