---
title: Kesme modunda Adımlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- break mode, stepping
- stepping, in break mode
- debugging [Debugging SDK], stepping in break mode
ms.assetid: b08dc8ee-6c63-4462-a097-6f525cfbb35a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: eb7b7e847c116f3aab38a12ec9801988bb8b3fc1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62912850"
---
# <a name="stepping-in-break-mode"></a>Kesme modunda Adımlama
Aşağıdaki bölümde hata ayıklayıcı kesme modundayken ve kodunuz içinde adım adım gerekir oluşan süreci açıklanmaktadır:

## <a name="stepping-process"></a>İşlem Adımlama

1. Çağrı [IDebugProgram2::Step](../../extensibility/debugger/reference/idebugprogram2-step.md) ile [STEPKIND](../../extensibility/debugger/reference/stepkind.md) ve [STEPUNIT](../../extensibility/debugger/reference/stepunit.md) bir adımı yürütmeye yönelik bağımsız değişkenleri.

2. Bu adım tamamlandığında, gönderme bir [IDebugStepCompleteEvent2](../../extensibility/debugger/reference/idebugstepcompleteevent2.md) durdurma olay olarak.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcısı olaylarını çağırma](../../extensibility/debugger/calling-debugger-events.md)