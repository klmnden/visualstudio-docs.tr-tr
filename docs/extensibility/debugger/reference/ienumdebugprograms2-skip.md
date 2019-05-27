---
title: IEnumDebugPrograms2::Skip | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugPrograms2::Skip
helpviewer_keywords:
- IEnumDebugPrograms2::Skip
ms.assetid: b283858b-b375-4760-bfec-ab37de89958d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: ce355667e6decf446972dd4941cfcf92b4bff5ea
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66210997"
---
# <a name="ienumdebugprograms2skip"></a>IEnumDebugPrograms2::Skip
Belirtilen sayıda öğeyi üzerinden atlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Skip(
   ULONG celt
);
```

```csharp
int Skip(
   uint celt
);
```

## <a name="parameters"></a>Parametreler
`celt`\
[in] Geçilecek öğelerin sayısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa `celt` kalan öğeleri sayısından büyüktür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Varsa `celt` numarasından daha büyük bir değer belirtir, kalan öğeleri numaralandırma sonuna ayarlanır ve `S_FALSE` döndürülür.

## <a name="see-also"></a>Ayrıca bkz.
- [IEnumDebugPrograms2](../../../extensibility/debugger/reference/ienumdebugprograms2.md)