---
title: Kesme moduna girme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- break mode
- debugging [Debugging SDK], entering break mode
ms.assetid: e9a8a241-cd21-4d4e-999a-283554c288b1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8da96c1df3423665ed223fecdd43007ba5a6e671
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62925761"
---
# <a name="enter-break-mode"></a>Kesme moduna girin
Aşağıdaki bilgiler, bir işlevin Adımlama, imleç içerdiğinden kaynak kod satırının çalışan ya da bir kesme noktası için çalışan bir kesme noktası karşılaşıldığında oluşan işlemi açıklanmaktadır.

## <a name="break-mode-process"></a>Kesme modu işlemi

1. Hata ayıklama altyapısı (DE) gönderir [IDebugBreakpointEvent2](../../extensibility/debugger/reference/idebugbreakpointevent2.md), [IDebugExceptionEvent2](../../extensibility/debugger/reference/idebugexceptionevent2.md), veya diğer tüm durdurma olay Kesme moduna girmek IDE neden olacak.

2. SDM çağrı yığını bilgilerini iş parçacığından aşağıdaki gibi alır:

    - [IDebugThread2::EnumFrameInfo](../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)

    - [IEnumDebugFrameInfo2::GetCount](../../extensibility/debugger/reference/ienumdebugframeinfo2-getcount.md)

    - [IEnumDebugFrameInfo2::Next](../../extensibility/debugger/reference/ienumdebugframeinfo2-next.md)

    - [IDebugStackFrame2::GetDocumentContext](../../extensibility/debugger/reference/idebugstackframe2-getdocumentcontext.md) kaynak kod bilgisi almak için

    - [IDebugDocumentContext2::GetName](../../extensibility/debugger/reference/idebugdocumentcontext2-getname.md) dosya adını almak için

    - [IDebugDocumentContext2::GetStatementRange](../../extensibility/debugger/reference/idebugdocumentcontext2-getstatementrange.md) deyim aralığı almak için

    - [IDebugStackFrame2::GetCodeContext](../../extensibility/debugger/reference/idebugstackframe2-getcodecontext.md) bellek bilgileri almak için

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcısı olaylarını çağırma](../../extensibility/debugger/calling-debugger-events.md)