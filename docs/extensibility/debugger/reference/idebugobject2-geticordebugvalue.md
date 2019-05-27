---
title: IDebugObject2::GetICorDebugValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject2::GetICorDebugValue
helpviewer_keywords:
- IDebugObject2::GetICorDebugValue method
ms.assetid: bcd4355d-3fbe-483f-bb23-a44348323c6a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 7524e3d6d16b071990e61438e09c0e360808c7bc
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66209827"
---
# <a name="idebugobject2geticordebugvalue"></a>IDebugObject2::GetICorDebugValue
Bu nesneyle ilişkili değeri temsil eden bir yönetilen kod nesnesi alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetICorDebugValue(
   IUnknown** ppUnk
);
```

```csharp
int GetICorDebugValue(
   out object ppUnk
);
```

## <a name="parameters"></a>Parametreler
`ppUnk`\
[out] `IUnknown` bu diğer adı temsil eden arabirim. Bu arabirim için sorgulanabilir `ICorDebugValue` arabirimi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 `ICorDebugValue` Bir değeri temsil eden bir ortak dil çalışma zamanı arabirimi nesnedir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)