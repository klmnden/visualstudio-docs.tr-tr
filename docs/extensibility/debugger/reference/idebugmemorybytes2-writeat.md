---
title: IDebugMemoryBytes2::WriteAt | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMemoryBytes2::WriteAt
helpviewer_keywords:
- IDebugMemoryBytes2::WriteAt method
- WriteAt method
ms.assetid: 61cc3704-47fa-4d9b-aa62-bb4585ac8fb1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: ad3e4c14c28f220a28e8d9aa65ddb1b6e6a3af0a
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66210546"
---
# <a name="idebugmemorybytes2writeat"></a>IDebugMemoryBytes2::WriteAt
Bayt bellek, belirtilen adres'ten itibaren belirtilen sayıda yazar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT WriteAt( 
   IDebugMemoryContext2* pStartContext,
   DWORD                 dwCount,
   BYTE*                 rgbMemory
);
```

```csharp
int WriteAt(
   IDebugMemoryContext2 pStartContext,
   uint                 dwCount,
   byte[]               rgbMemory
);
```

## <a name="parameters"></a>Parametreler
`pStartContext`\
[in] [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) nesnesini bayt yazmaya başlamak konumu belirtir.

`dwCount`\
[in] Yazılacak bayt sayısı.

`rgbMemory`\
[in] Yazılacak bayt sayısı. Bu dizi en az olduğu varsayılır `dwCount` bayt cinsinden boyutu.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` tüm baytlar yazılabilir veya bir hata kodu döndürür (genelde `E_FAIL`).

## <a name="remarks"></a>Açıklamalar
 Başlangıç adresi bu tarafından temsil edilen bellek penceresi içinde değilse [IDebugMemoryBytes2](../../../extensibility/debugger/reference/idebugmemorybytes2.md) nesne, hiçbir yazma gerçekleşir ve hata kodunu `E_FAIL` döndürülen — bile yazmak için tutar bellek alanı ile çakışıyor.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugMemoryBytes2](../../../extensibility/debugger/reference/idebugmemorybytes2.md)
- [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)