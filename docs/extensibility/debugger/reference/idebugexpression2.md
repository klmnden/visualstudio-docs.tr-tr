---
title: IDebugExpression2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugExpression2
helpviewer_keywords:
- IDebugExpression2 interface
ms.assetid: f5e4b124-1e30-47c8-a511-80084a02dba5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b8027f34b48b4a160c19f14f0d9cbfb8194a506f
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56688488"
---
# <a name="idebugexpression2"></a>IDebugExpression2
Bu arabirim bağlama ve değerlendirmek için ayrıştırılmış ifade hazır temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugExpression2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE) uyumluluğunun değerlendirilebilmesi hazır bir ayrıştırılmış ifadesini göstermek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir çağrı [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) bu arabirimi döndürür. [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) döndürür [IDebugExpressionContext2](../../../extensibility/debugger/reference/idebugexpressioncontext2.md) arabirimi. Bu arabirimler yalnızca hata ayıklanan programa duraklatıldı ve bir yığın çerçevesini kullanılabilir erişilebilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugExpression2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md)|Bu ifade zaman uyumsuz olarak değerlendirilir.|
|[Abort](../../../extensibility/debugger/reference/idebugexpression2-abort.md)|Zaman uyumsuz bir ifade değerlendirme sona erer.|
|[EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md)|Bu ifade zaman uyumlu olarak değerlendirilir.|

## <a name="remarks"></a>Açıklamalar
 Bir program durdu, oturum hata ayıklama Yöneticisi (SDM) bir yığın çerçevesi bir çağrı ile DE elde [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md). SDM sonra çağıran [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) almak için [IDebugExpressionContext2](../../../extensibility/debugger/reference/idebugexpressioncontext2.md) arabirimi. Bu çağrı takip [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) oluşturmak için `IDebugExpression2` değerlendirilecek hazır ayrıştırılmış ifadeyi temsil eden arabirim.

 SDM ya da çağırır [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) veya [EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) gerçekten ifadeyi değerlendirir ve bir değer üretir.

 Uygulaması içinde `IDebugExpressionContext2::ParseText`, DE COM'ın kullandığı `CoCreateInstance` ifade değerlendiricisi oluşturmak ve almak için işlevi bir [IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md) arabirimi (örnekte bakın `IDebugExpressionEvaluator` arabirimi). Daha sonra DE çağırır [ayrıştırma](../../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md) almak için bir [IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md) arabirimi. Bu arabirim uygulamasında kullanılan `IDebugExpression2::EvaluateSync` ve `IDebugExpression2::EvaluateAsync` değerlendirmeyi gerçekleştirmek için.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [GetExpression](../../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getexpression.md)