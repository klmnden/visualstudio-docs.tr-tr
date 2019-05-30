---
title: METADATA_ADDRESS_LOCAL | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- METADATA_ADDRESS_LOCAL
helpviewer_keywords:
- METADATA_ADDRESS_LOCAL structure
ms.assetid: 635f6bc5-c486-4e0e-83db-36f15e543843
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: f8500d7ad1e03e08fa852afe9b8b77e49562f355
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345629"
---
# <a name="metadataaddresslocal"></a>METADATA_ADDRESS_LOCAL

Bu yapı (genellikle bir işlev veya yöntem), bir kapsamdaki yerel değişkenin adresini temsil eder.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _tagMETADATA_ADDRESS_LOCAL {
    _mdToken  tokMethod;
    IUnknown* pLocal;
    DWORD     dwIndex;
} METADATA_ADDRESS_LOCAL;
```

```csharp
public struct METADATA_ADDRESS_LOCAL {
    public int    tokMethod;
    public object pLocal;
    public uint   dwIndex;
}
```

## <a name="members"></a>Üyeler

`tokMethod`\
Yöntem veya işlev Kimliğini yerel değişken, parçasıdır.

[C++] `_mdToken` olduğu bir `typedef` 32-bit `int`.

`pLocal`\
Belirteci adresi bu yapıyı temsil eder.

`dwIndex`\
Bu yöntem veya işlev ya da başka bir değer (dile özgü) yerel değişken dizini olabilir.

## <a name="remarks"></a>Açıklamalar

Bu yapı, birleşim içinde parçasıdır [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md) ne zaman yapısı `dwKind` alanını `DEBUG_ADDRESS_UNION` yapısı ayarlandığında `ADDRESS_KIND_LOCAL` (arasında bir değer [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md) sabit listesi).

> [!WARNING]
> [C++ yalnızca] Varsa `pLocal` çağırmalısınız sonra null değil `Release` belirteci işaretçinin (`addr` bir alandır [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) yapısı):
>
> ```cpp
> if (addr.dwKind == ADDRESS_KIND_METADATA_LOCAL && addr.addr.addrLocal.pLocal != NULL)
> {
>     addr.addr.addrLocal.pLocal->Release();
> }
> ```

## <a name="requirements"></a>Gereksinimler

Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.

- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)
- [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)
- [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)
