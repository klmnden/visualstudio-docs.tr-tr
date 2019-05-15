---
title: ADDRESS_KIND | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ADDRESS_KIND
helpviewer_keywords:
- ADDRESS_KIND enumeration
ms.assetid: 3a12fbec-7088-4cf9-8f6f-ad8ddec6009a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 0325642e9bcd1e1bc79365650a62938c3250c81e
ms.sourcegitcommit: 77b4ca625674658d5c5766e684fa0e2a07cad4da
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65615388"
---
# <a name="addresskind"></a>ADDRESS_KIND
Adresleri türlerini belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_ADDRESS_KIND {
    ADDRESS_KIND_NATIVE                  = 0x0001,
    ADDRESS_KIND_UNMANAGED_THIS_RELATIVE = 0x0002,
    ADDRESS_KIND_UNMANAGED_PHYSICAL      = 0x0005,
    ADDRESS_KIND_METADATA_METHOD         = 0x0010,
    ADDRESS_KIND_METADATA_FIELD          = 0x0011,
    ADDRESS_KIND_METADATA_LOCAL          = 0x0012,
    ADDRESS_KIND_METADATA_PARAM          = 0x0013,
    ADDRESS_KIND_METADATA_ARRAYELEM      = 0x0014,
    ADDRESS_KIND_METADATA_RETVAL         = 0x0015,
};
typedef DWORD ADDRESS_KIND;
```

```csharp
public enum enum_ADDRESS_KIND {
    ADDRESS_KIND_NATIVE                  = 0x0001,
    ADDRESS_KIND_UNMANAGED_THIS_RELATIVE = 0x0002,
    ADDRESS_KIND_UNMANAGED_PHYSICAL      = 0x0005,
    ADDRESS_KIND_METADATA_METHOD         = 0x0010,
    ADDRESS_KIND_METADATA_FIELD          = 0x0011,
    ADDRESS_KIND_METADATA_LOCAL          = 0x0012,
    ADDRESS_KIND_METADATA_PARAM          = 0x0013,
    ADDRESS_KIND_METADATA_ARRAYELEM      = 0x0014,
    ADDRESS_KIND_METADATA_RETVAL         = 0x0015,
};
```

## <a name="fields"></a>Alanlar
`ADDRESS_KIND_NATIVE`\
Tarafından temsil edilen bir yerel adres [NATIVE_ADDRESS](../../../extensibility/debugger/reference/native-address.md) yapısı.

`ADDRESS_KIND_UNMANAGED_THIS_RELATIVE`\
Yönetilmeyen bir adresi göreli bir `this` (`Me` Visual Basic'te) işaretçi tarafından temsil edilen ve [UNMANAGED_ADDRESS_THIS_RELATIVE](../../../extensibility/debugger/reference/unmanaged-address-this-relative.md) yapısı.

`ADDRESS_KIND_UNMANAGED_PHYSICAL`\
Tarafından temsil edilen bir yönetilmeyen bir fiziksel adresi [UNMANAGED_ADDRESS_PHYSICAL](../../../extensibility/debugger/reference/unmanaged-address-physical.md) yapısı.

`ADDRESS_KIND_METHOD`\
Bir sınıf tarafından temsil edilen bir yöntem [METADATA_ADDRESS_METHOD](../../../extensibility/debugger/reference/metadata-address-method.md) yapısı.

`ADDRESS_KIND_FIELD`\
Tarafından temsil edilen bir sınıfının bir alanı [METADATA_ADDRESS_FIELD](../../../extensibility/debugger/reference/metadata-address-field.md) yapısı.

`ADDRESS_KIND_LOCAL`\
Adresi için bir yerel değişken ve tarafından temsil edilen [METADATA_ADDRESS_LOCAL](../../../extensibility/debugger/reference/metadata-address-local.md) yapısı.

`ADDRESS_KIND_PARAM`\
Tarafından temsil edilen bir yöntem veya işlev parametresi [METADATA_ADDRESS_PARAM](../../../extensibility/debugger/reference/metadata-address-param.md) yapısı.

`ADDRESS_KIND_ARRAYELEM`\
Tarafından temsil edilen bir dizi öğesine [METADATA_ADDRESS_ARRAYELEM](../../../extensibility/debugger/reference/metadata-address-arrayelem.md) yapısı.

`ADDRESS_KIND_RETVAL`\
Tarafından temsil edilen bir dönüş değeri [METADATA_ADDRESS_RETVAL](../../../extensibility/debugger/reference/metadata-address-retval.md) yapısı.

## <a name="remarks"></a>Açıklamalar
[GetAddress](../../../extensibility/debugger/reference/idebugaddress-getaddress.md) yöntemi döndürür [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) olası yapıları bir birleşimini içeren yapı [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md) yapısı. `dwKind` Alanını `DEBUG_ADDRESS_UNION` yapısı ayrı tutma `ADDRESS_KIND` değerini ve nasıl birleşim alanın yorumlanması gerektiğini açıklar.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetAddress](../../../extensibility/debugger/reference/idebugaddress-getaddress.md)
- [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)
- [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)
