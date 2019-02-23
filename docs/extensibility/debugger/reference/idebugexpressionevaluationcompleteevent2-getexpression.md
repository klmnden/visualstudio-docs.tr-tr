---
title: IDebugExpressionEvaluationCompleteEvent2::GetExpression | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugExpressionEvaluationCompleteEvent2::GetExpression
helpviewer_keywords:
- IDebugExpressionEvaluationCompleteEvent2::GetExpression
ms.assetid: faf6b2dd-2afd-4852-b21c-7e8d3130e141
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bb413457b9e84d57079d9c5efa3369ddad608934
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56707698"
---
# <a name="idebugexpressionevaluationcompleteevent2getexpression"></a>IDebugExpressionEvaluationCompleteEvent2::GetExpression
Özgün ifadesi alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetExpression( 
   IDebugExpression2** ppExpr
);
```

```csharp
int GetExpression( 
   out IDebugExpression2 ppExpr
);
```

#### <a name="parameters"></a>Parametreler
 `ppExpr`

 [out] Döndürür bir [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md) ayrıştırıldığında küpte ifadeyi temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem çağrısında oluşturulan nesneyi döndürür [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugExpressionEvaluationCompleteEvent2](../../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md)
- [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md)
- [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md)