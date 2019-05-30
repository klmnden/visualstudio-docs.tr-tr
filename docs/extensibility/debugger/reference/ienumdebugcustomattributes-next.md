---
title: IEnumDebugCustomAttributes::Next | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumCustomAttributes::Next
helpviewer_keywords:
- IEnumDebugCustomAttributes::Next
ms.assetid: e36f856b-2619-42d1-b73e-4f2390fc22bd
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 01d3f7f1459cf15525cfe6a1025a99e2eb41f8c0
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66333097"
---
# <a name="ienumdebugcustomattributesnext"></a>IEnumDebugCustomAttributes::Next
Özel özniteliklerin bir numaralandırma dizisinde belirtilen bir sayı alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Next ( 
   ULONG      celt,
   CODE_PATH* rgelt,
   ULONG*     pceltFetched
);
```

```csharp
int Next(
   uint                        celt,
   out IDebugCustomAttribute[] rgelt,
   ref uint                    pceltFetched
);
```

## <a name="parameters"></a>Parametreler
`celt`\
[in] Alınacak öğelerin sayısı. Ayrıca en büyük boyutunu belirtir `rgelt` dizisi.

`rgelt`\
[out] Bir dizi [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md) doldurulacak nesne.

`pceltFetched`\
[out] Gerçekte döndürülen öğe sayısını döndürür `rgelt`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` istenen öğelerin sayısından daha az döndürülebilen; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md)
- [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md)