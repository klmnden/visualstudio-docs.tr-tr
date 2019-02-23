---
title: IDebugExpressionEvaluator2::SetIDebugIDECallback | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugExpressionEvaluator2::SetIDebugIDECallback
- SetIDebugIDECallback
ms.assetid: f01c40ad-ef4b-477b-8304-602c6972bc88
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1ac5027421ff73e00ee34d9928be6525187a6ae8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56679300"
---
# <a name="idebugexpressionevaluator2setidebugidecallback"></a>IDebugExpressionEvaluator2::SetIDebugIDECallback
İfade değerlendiricisi için bir geri çağırma işlemini başlatma sırasında geçirilecek bir hata ayıklama altyapısı sağlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetIDebugIDECallback (
   IDebugIDECallback * pCallback
);
```

```csharp
int SetIDebugIDECallback (
   IDebugIDECallback pCallback
);
```

#### <a name="parameters"></a>Parametreler
 `pCallback`

 [in] Geri çağırma arabirimi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugExpressionEvaluator2](../../../extensibility/debugger/reference/idebugexpressionevaluator2.md)