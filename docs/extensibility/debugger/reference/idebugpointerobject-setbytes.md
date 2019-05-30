---
title: IDebugPointerObject::SetBytes | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPointerObject::SetBytes
helpviewer_keywords:
- IDebugPointerObject::SetBytes method
ms.assetid: 8c578b38-38d7-46f3-bb2e-8a730fccd334
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 1e7b3fd72285f6a6c9c4abeca4e6b262d981be8f
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66331546"
---
# <a name="idebugpointerobjectsetbytes"></a>IDebugPointerObject::SetBytes
Art arda bayt dizisinden işaret değeri ayarlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetBytes( 
   DWORD  dwStart,
   DWORD  dwCount,
   BYTE*  pBytes,
   DWORD* pdwBytes
);
```

```csharp
int SetBytes(
   uint     dwStart,
   uint     dwCount,
   byte[]   pBytes,
   out uint pdwBytes
);
```

## <a name="parameters"></a>Parametreler
`dwStart`\
[in] Belirtilen nesnenin başından itibaren bayt cinsinden uzaklık.

`dwCount`\
[in] Ayarlanacak bayt sayısı.

`pBytes`\
[in] Yeni değeri temsil eden bir bayt dizisi. Bu değer, belirtilen uzaklıkta başlayan belirli nesne içinde depolanır.

`pdwBytes`\
[out] Bayt sayısı gerçekte ayarlamak döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem kullanılır bu tarafından temsil edilen işaretçinin [IDebugPointerObject](../../../extensibility/debugger/reference/idebugpointerobject.md) işaret türü basit tür veya basit bir dizi temel türlerin (diğer bir deyişle, basit bir bayt dizisi tarafından temsil edilen bir dizi). Bu `IDebugPointerObject` nesne (onu işaret etmelidir bir bellek adresi) bir null başvuru olamaz.

## <a name="see-also"></a>Ayrıca bkz.
- [GetBytes](../../../extensibility/debugger/reference/idebugpointerobject-getbytes.md)
- [IDebugPointerObject](../../../extensibility/debugger/reference/idebugpointerobject.md)