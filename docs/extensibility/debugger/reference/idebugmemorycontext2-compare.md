---
title: IDebugMemoryContext2::Compare | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMemoryContext2::Compare
helpviewer_keywords:
- IDebugMemoryContext2::Compare method
- Compare method
ms.assetid: c51b5128-848e-4d8e-b2e9-1161339763c3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: f04000d3e2675f766ae343836320aa7433ade87d
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66211990"
---
# <a name="idebugmemorycontext2compare"></a>IDebugMemoryContext2::Compare
Eşleşen ilk bağlamıyla dizinini döndüren karşılaştırma bayrakları tarafından belirtildiği şekilde belirtilen dizideki her bağlam için bellek bağlam karşılaştırır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Compare( 
   CONTEXT_COMPARE        compare,
   IDebugMemoryContext2** rgpMemoryContextSet,
   DWORD                  dwMemoryContextSetLen,
   DWORD*                 pdwMemoryContext
);
```

```csharp
int Compare(
   enum_CONTEXT_COMPARE   compare,
   IDebugMemoryContext2[] rgpMemoryContextSet,
   uint                   dwMemoryContextSetLen,
   out uint               pdwMemoryContext
);
```

## <a name="parameters"></a>Parametreler
`compare`\
[in] Bir değer [CONTEXT_COMPARE](../../../extensibility/debugger/reference/context-compare.md) karşılaştırma türünü belirleyen sabit listesi.

`rgpMemoryContextSet`\
[in] İçin yapılan başvuruların dizisi [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) Karşılaştırılacak nesne.

`dwMemoryContextSetLen`\
[in] Bağlamlarda sayısını `rgpMemoryContextSet` dizisi.

`pdwMemoryContext`\
[out] Karşılaştırmayı ilk bellek bağlam dizinini döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_COMPARE_CANNOT_COMPARE` varsa iki bağlamları karşılaştırılamaz.

## <a name="remarks"></a>Açıklamalar
 Karşılaştırma tüm türleri desteklemek hata ayıklama altyapısı (DE) yok, ancak en az desteklemelidir `CONTEXT_EQUAL`, `CONTEXT_LESS_THAN`, `CONTEXT_GREATER_THAN` ve `CONTEXT_SAME_SCOPE`.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)
- [CONTEXT_COMPARE](../../../extensibility/debugger/reference/context-compare.md)