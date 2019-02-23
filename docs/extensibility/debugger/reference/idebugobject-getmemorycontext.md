---
title: IDebugObject::GetMemoryContext | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject::GetMemoryContext
helpviewer_keywords:
- IDebugObject::GetMemoryContext method
ms.assetid: 6760a0d3-a898-4e81-b68f-c45c584b225b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e47fd5a7a8285db6c9cdf923699eb4b8f79b451a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56722973"
---
# <a name="idebugobjectgetmemorycontext"></a>IDebugObject::GetMemoryContext
Nesne değeri adresini temsil eden bellek bağlamını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetMemoryContext( 
   IDebugMemoryContext2** pContext
);
```

```csharp
int GetMemoryContext(
   ref IDebugMemoryContext2 pContext
);
```

#### <a name="parameters"></a>Parametreler
 `pContext`

 [out] Döndürür bir [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) nesnenin değerini adresini temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu tarafından temsil edilen değeri adresini döndürülen bellek bağlam belirten [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) nesne.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)