---
title: METADATA_ADDRESS_RETVAL | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- METADATA_ADDRESS_RETVAL
helpviewer_keywords:
- METADATA_ADDRESS_RETVAL structure
ms.assetid: 5b0ec0fb-84b3-4ce7-8e24-becf3d881d7d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: b4453030f01e99dcb82c344f003e217e7b1c55b6
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66333708"
---
# <a name="metadataaddressretval"></a>METADATA_ADDRESS_RETVAL
Bu yapı bir yöntemi veya işlev dönüş değeri temsil eder.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _tagMETADATA_ADDRESS_RETVAL {
   _mdToken tokMethod;
   DWORD    dwCorType;
   DWORD    dwSigSize;
   BYTE     rgSig[10];
} METADATA_ADDRESS_RETVAL;
```

```csharp
public struct METADATA_ADDRESS_RETVAL {
   public int    tokMethod;
   public uint   dwCorType;
   public uint   dwSigSize;
   public byte[] rgSig;
}
```

## <a name="members"></a>Üyeler
 `tokMethod`\
 Bu dönüş değeri yöntemi için kimliği.

 `dwCorType`\
 Dönüş değeri temel türü. Bir değer budur `CorElementType` tanımlanan numaralandırma [!INCLUDE[dnprdnshort](../../../code-quality/includes/dnprdnshort_md.md)] SDK corhdr.h dosyası.

 `dwSigSize`\
 Dönüş değeri imza boyutu (depolanan gibi `rgSig`).

 `rgSig`\
 Dönüş değeri imzası oluşturan bir bayt dizisi.

## <a name="remarks"></a>Açıklamalar
 Bu yapı, birleşim içinde parçasıdır [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md) ne zaman yapısı `dwKind` alanını `DEBUG_ADDRESS_UNION` yapısı ayarlandığında `ADDRESS_KIND_RETVAL` (arasında bir değer [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md) sabit listesi).

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)
- [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)