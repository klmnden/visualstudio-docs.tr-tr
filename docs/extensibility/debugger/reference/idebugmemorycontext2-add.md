---
title: IDebugMemoryContext2::Add | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMemoryContext2::Add
helpviewer_keywords:
- IDebugMemoryContext2::Add method
- Add method
ms.assetid: 3c47e646-ce9e-4dd3-8f1a-6dbd3827d407
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 4c1a486318899173cb6ab6b30cfd427bc6f0b360
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66210540"
---
# <a name="idebugmemorycontext2add"></a>IDebugMemoryContext2::Add
Belirtilen değer için geçerli bağlam ekler ve yeni bir bağlam döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Add( 
   UINT64                 dwCount,
   IDebugMemoryContext2** ppMemCxt
);
```

```csharp
int Add(
   ulong                    dwCount,
   out IDebugMemoryContext2 ppMemCxt
);
```

## <a name="parameters"></a>Parametreler
`dwCount`\
[in] Geçerli bağlama eklemek için değer.

`ppMemCxt`\
[out] Yeni bir [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir bellek bağlamı bir adresi olduğundan bir adrese bir değeri ekleyerek yeni bir bağlam arabirimi gerektiren yeni bir adres üretir.

 Bu bağlamla ilişkilendirilen bellek alanını elde edilen adresi dışında olsa bile, bu yöntem her zaman yeni bir bağlam üretmesi gerekir. Yeni bağlam için ayrılan bellek yok ise veya tek özel durumu olan `ppMemCxt` (Bu bir hatadır) null bir değerdir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)