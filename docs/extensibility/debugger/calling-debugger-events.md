---
title: Hata ayıklayıcı olayları çağırma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], events
ms.assetid: b3440ac3-80af-40c6-bef4-cbf00fa67885
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7564010055218065a8971f40989af2152acd5d95
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66332487"
---
# <a name="call-debugger-events"></a>Hata ayıklayıcı olayları çağırma
Hata ayıklama oturumları, olayları belirli bir sırayla oluşur.

## <a name="discussion"></a>Tartışma
 Hata ayıklama altyapısı (DE) ve oturum hata ayıklama Yöneticisi (SDM) arasındaki çağrıların desenini anlamak için tipik hata ayıklama oturumunda gerçekleşen olaylara arama sırası şunları gösterir:

1. [Ekleme ve programdan ayırma](../../extensibility/debugger/attaching-and-detaching-to-a-program.md)

2. [Hata ayıklayıcı başlatılıyor](../../extensibility/debugger/launching-the-debugger.md)

3. [Program sonlandırma](../../extensibility/debugger/terminating-a-program.md)

4. [Bir kesme noktası oluşturma](../../extensibility/debugger/creating-a-breakpoint.md)

5. [Ne zaman bir kesme noktası bağlar veya ilişkisiz olma](../../extensibility/debugger/when-a-breakpoint-binds-or-becomes-unbound.md)

6. [Kesme noktası hataları](../../extensibility/debugger/breakpoint-errors.md)

7. [Kesme noktasına ulaşma](../../extensibility/debugger/hitting-a-breakpoint.md)

8. [Kesme noktasını silme](../../extensibility/debugger/deleting-a-breakpoint.md)

9. [Kesme moduna girme](../../extensibility/debugger/entering-break-mode.md)

10. [Kesme modunda Adımlama](../../extensibility/debugger/stepping-in-break-mode.md)

11. [Kesme modunda ifade değerlendirme](../../extensibility/debugger/expression-evaluation-in-break-mode.md)

12. [Özel durum işleme](../../extensibility/debugger/exception-handling-visual-studio-sdk.md)

## <a name="see-also"></a>Ayrıca bkz.
- [Bir özel hata ayıklama altyapısı oluşturma](../../extensibility/debugger/creating-a-custom-debug-engine.md)