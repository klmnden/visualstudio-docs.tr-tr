---
title: IDebugExpression2::EvaluateAsync | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugExpression2::EvaluateAsync
helpviewer_keywords:
- IDebugExpression2::EvaluateAsync
ms.assetid: 848fe6cb-0759-42f2-890b-d2b551c527d6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: dd5c0c6c056dc72f3db49a9d666d6f2ba6295791
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66326011"
---
# <a name="idebugexpression2evaluateasync"></a>IDebugExpression2::EvaluateAsync
Bu yöntem, zaman uyumsuz olarak ifadeyi değerlendirir.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EvaluateAsync (
    EVALFLAGS             dwFlags,
    IDebugEventCallback2* pExprCallback
);
```

```csharp
int EvaluateAsync(
    enum_EVALFLAGS       dwFlags,
    IDebugEventCallback2 pExprCallback
);
```

## <a name="parameters"></a>Parametreler
`dwFlags`\
[in] Bayraklarının bir birleşimi [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) ifade değerlendirme denetleyen sabit listesi.

`pExprCallback`\
[in] Bu parametre, her zaman null değeri olur.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Tipik bir kodu verilmiştir:

|Hata|Açıklama|
|-----------|-----------------|
|E_EVALUATE_BUSY_WITH_EVALUATION|Başka bir ifade şu anda değerlendirilen ve eşzamanlı ifade değerlendirme desteklenmiyor.|

## <a name="remarks"></a>Açıklamalar
İfade değerlendirme başlatıldıktan hemen sonra bu yöntem döndürmelidir. İfade başarılı bir şekilde değerlendirildiğinde, bir [IDebugExpressionEvaluationCompleteEvent2](../../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md) gönderilmelidir [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) aracılığıyla sağlanan olarak olay geri çağırma [Ekle ](../../../extensibility/debugger/reference/idebugprogram2-attach.md) veya [ekleme](../../../extensibility/debugger/reference/idebugengine2-attach.md).

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu yöntem için basit bir uygulama gösterilmektedir `CExpression` uygulayan nesne [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md) arabirimi.

```cpp
HRESULT CExpression::EvaluateAsync(EVALFLAGS dwFlags,
                                   IDebugEventCallback2* pExprCallback)
{
    // Set the aborted state to FALSE
    // in case the user tries to redo the evaluation after aborting.
    m_bAborted = FALSE;
    // Post the WM_EVAL_EXPR message in the message queue of the current thread.
    // This starts the expression evaluation on a background thread.
    PostThreadMessage(GetCurrentThreadId(), WM_EVAL_EXPR, 0, (LPARAM) this);
    return S_OK;
}
```

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md)
- [IDebugExpressionEvaluationCompleteEvent2](../../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md)
- [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)
