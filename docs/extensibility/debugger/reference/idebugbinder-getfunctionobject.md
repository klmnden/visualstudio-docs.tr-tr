---
title: IDebugBinder::GetFunctionObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBinder::GetFunctionObject
helpviewer_keywords:
- IDebugBinder::GetFunctionObject method
ms.assetid: 8fb789df-8f30-420d-8ca5-bb496a6738f1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b69af018a1b5b1ddf743784f4736d7c2ac24d45f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62923688"
---
# <a name="idebugbindergetfunctionobject"></a>IDebugBinder::GetFunctionObject
Bu yöntem alır bir [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) işlev parametreleri oluşturmak için kullanılan nesne.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetFunctionObject( 
   IDebugFunctionObject **ppFunction
);
```

```csharp
int GetFunctionObject(
   out IDebugFunctionObject ppFunction
);
```

#### <a name="parameters"></a>Parametreler
 `ppFunction`

 [out] Döndürür [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) işlev parametreleri oluşturmak için kullanılan arabirim.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)
- [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)