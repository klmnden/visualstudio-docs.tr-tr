---
title: Denetim olaylarına | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], events
ms.assetid: 0fc63484-5fb6-4887-9ea4-1905b459ca9d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0c79abb6ca0912ba0a8872d87c830ba455836595
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66312449"
---
# <a name="control-events"></a>Denetim olayları
Olay denetimli programınızı yürütülmesi sırasında göndermeniz gerekir. Tüm olayları kullanılarak gönderilen [IDebugEvent2](../../extensibility/debugger/reference/idebugevent2.md) uygulamak ihtiyaç duyduğunuz özniteliklere sahip ve arabirim [IDebugEvent2::GetAttributes](../../extensibility/debugger/reference/idebugevent2-getattributes.md) yöntemi.

## <a name="additional-methods"></a>Ek yöntemleri
 Bazı olaylar şu şekilde ek yöntemleri uygulaması gerekir:

- Gönderme [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) hata ayıklama altyapısı (DE) başlatıldığında arabirim uygulamak gerektirir [IDebugEngineCreateEvent2::GetEngine](../../extensibility/debugger/reference/idebugenginecreateevent2-getengine.md) yöntemi.

- Yürütme denetimi gibi denetim olaylar uygulaması gerektirir [IDebugBreakEvent2](../../extensibility/debugger/reference/idebugbreakevent2.md) ve[IDebugStepCompleteEvent2](../../extensibility/debugger/reference/idebugstepcompleteevent2.md) arabirimleri. **IDebugBreakEvent2** yalnızca zaman uyumsuz kesmeleri için gereklidir.

- İşlevlerin içine Adımlama gerektirir uygulaması [IDebugStepCompleteEvent2](../../extensibility/debugger/reference/idebugstepcompleteevent2.md) arabirimi ve yöntemleri.

  Kesme noktaları türetme olayları gerektiren uygulaması [IDebugBreakpointErrorEvent2](../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md), [IDebugBreakpointEvent2](../../extensibility/debugger/reference/idebugbreakpointevent2.md), ve [IDebugBreakpointBoundEvent2](../../extensibility/debugger/reference/idebugbreakpointboundevent2.md) arabirimleri, hem de [IDebugBreakpointBoundEvent2::GetPendingBreakpoint](../../extensibility/debugger/reference/idebugbreakpointboundevent2-getpendingbreakpoint.md) ve [EnumBoundBreakpoints](../../extensibility/debugger/reference/idebugbreakpointboundevent2-enumboundbreakpoints.md) yöntemleri.

  Zaman uyumsuz bir ifade değerlendirme uygulamak gerektirir [IDebugExpressionEvaluationCompleteEvent2](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md) arabirimi ve kendi [IDebugExpressionEvaluationCompleteEvent2::GetExpression](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getexpression.md) [ve GetResult](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getresult.md) yöntemleri.

  Zaman uyumlu olayları gerektiren uygulama [IDebugEngine2::ContinueFromSynchronousEvent](../../extensibility/debugger/reference/idebugengine2-continuefromsynchronousevent.md) yöntemi.

  Altyapınız dize stili çıkışını yazmak uygulamanız gereken [IDebugOutputStringEvent2::GetString](../../extensibility/debugger/reference/idebugoutputstringevent2-getstring.md) yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [Yürütme denetimi ve durum değerlendirmesi](../../extensibility/debugger/execution-control-and-state-evaluation.md)