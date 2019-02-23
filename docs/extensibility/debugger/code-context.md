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
ms.openlocfilehash: 114537976561e72a9b1922c41d94ffa5e7ce613b
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56714551"
---
# <a name="code-context"></a>Kod bağlamı
İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama, bir **kod bağlamı**:

-   Hata ayıklama Altyapısı'na (DE) bilinen bir konum kod bir soyutlamasıdır sağlar. Çoğu çalışma zamanı mimarileri için bugün, bir kod bağlamı, bir programın yönerge stream'de adresi olarak düşünülebilir. Burada kod yönergeleri ile gösterilebilir değil, nontraditional diller için kod bağlamı başka bir yolla tarafından temsil edilebilir.

-   Hata ayıklama programı yürütme stream'de geçerli konumu açıklar.

-   Yalnızca bir programın bir kesme noktasında ne zaman durdurdu var.

-   İlişkili belge içeriğine sahiptir.

-   Tarafından uygulanan bir [IDebugCodeContext2](../../extensibility/debugger/reference/idebugcodecontext2.md) arabirimi.

## <a name="see-also"></a>Ayrıca bkz.
- [Belge bağlamı](../../extensibility/debugger/document-context.md)
- [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md)