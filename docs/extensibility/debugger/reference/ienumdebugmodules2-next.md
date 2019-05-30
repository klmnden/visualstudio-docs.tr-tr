---
title: IEnumDebugModules2::Next | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugModules2::Next
helpviewer_keywords:
- IEnumDebugModules2::Next
ms.assetid: 46b7ccad-b07b-4ec0-b3ce-13981ffab7e8
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: e5ce512cde85dd305b2d9efb360d805eddbba40e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350299"
---
# <a name="ienumdebugmodules2next"></a>IEnumDebugModules2::Next
Sabit listesinden alınmış sonraki öğe kümesini döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Next(
   ULONG           celt,
   IDebugModule2** rgelt,
   ULONG*          pceltFetched
);
```

```csharp
int Next(
   uint            celt,
   IDebugModule2[] rgelt,
   ref uint        pceltFetched
);
```

## <a name="parameters"></a>Parametreler
`celt`\
[in] Alınacak öğelerin sayısı. Ayrıca en büyük boyutunu belirtir `rgelt` dizisi.

`rgelt`\
[out içinde] Dizi [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md) doldurulacak öğeleri.

`pceltFetched`\
[out] Gerçekte döndürülen öğe sayısını döndürür `rgelt`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` istenen öğelerin sayısından daha az döndürülebilen; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md)
- [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md)