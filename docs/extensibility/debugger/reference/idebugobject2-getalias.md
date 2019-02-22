---
title: IDebugObject2::GetAlias | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject2::GetAlias
helpviewer_keywords:
- IDebugObject2::GetAlias method
ms.assetid: aa6824d5-c932-42ba-8713-950e7d1fb42f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7d08d9108ed4a433bcbcb17d6d4587532542b303
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56719853"
---
# <a name="idebugobject2getalias"></a>IDebugObject2::GetAlias
Bu nesneyle ilişkilendirilmiş diğer ada varsa alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetAlias(
   IDebugAlias** ppAlias
);
```

```csharp
int GetAlias(
   out IDebugAlias ppAlias
);
```

#### <a name="parameters"></a>Parametreler
 `ppAlias`

 [out] Döndürür bir [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md) bu nesne için bir diğer ad temsil eden nesne; Aksi takdirde, null değeri döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir nesne için bir diğer ad çağrısı ile oluşturulan [CreateAlias](../../../extensibility/debugger/reference/idebugobject2-createalias.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)
- [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md)