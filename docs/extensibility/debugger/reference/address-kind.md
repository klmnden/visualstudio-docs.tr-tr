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
ms.openlocfilehash: 71888e4e0b339b9b9b94946e8d9c49f8ffb1f84c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56696826"
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

## <a name="terms"></a>Koşulları
Tarafından temsil edilen ADDRESS_KIND_NATIVE bir yerel adres [NATIVE_ADDRESS](../../../extensibility/debugger/reference/native-address.md) yapısı.

ADDRESS_KIND_UNMANAGED_THIS_RELATIVE yönetilmeyen adres için göreli bir `this` (`Me` Visual Basic'te) işaretçi tarafından temsil edilen ve [UNMANAGED_ADDRESS_THIS_RELATIVE](../../../extensibility/debugger/reference/unmanaged-address-this-relative.md) yapısı.

Tarafından temsil edilen ADDRESS_KIND_UNMANAGED_PHYSICAL yönetilmeyen bir fiziksel adresi [UNMANAGED_ADDRESS_PHYSICAL](../../../extensibility/debugger/reference/unmanaged-address-physical.md) yapısı.

Tarafından temsil edilen bir sınıfın ADDRESS_KIND_METHOD A yöntemi [METADATA_ADDRESS_METHOD](../../../extensibility/debugger/reference/metadata-address-method.md) yapısı.

Tarafından temsil edilen bir sınıfın ADDRESS_KIND_FIELD bir alan [METADATA_ADDRESS_FIELD](../../../extensibility/debugger/reference/metadata-address-field.md) yapısı.

ADDRESS_KIND_LOCAL adresi için yerel bir değişkendir ve tarafından temsil edilen [METADATA_ADDRESS_LOCAL](../../../extensibility/debugger/reference/metadata-address-local.md) yapısı.

Tarafından temsil edilen ADDRESS_KIND_PARAM bir yöntem veya işlev parametresi [METADATA_ADDRESS_PARAM](../../../extensibility/debugger/reference/metadata-address-param.md) yapısı.

ADDRESS_KIND_ARRAYELEM tarafından temsil edilen bir dizi öğesine [METADATA_ADDRESS_ARRAYELEM](../../../extensibility/debugger/reference/metadata-address-arrayelem.md) yapısı.

Tarafından temsil edilen ADDRESS_KIND_RETVAL bir dönüş değeri [METADATA_ADDRESS_RETVAL](../../../extensibility/debugger/reference/metadata-address-retval.md) yapısı.

## <a name="remarks"></a>Açıklamalar
[GetAddress](../../../extensibility/debugger/reference/idebugaddress-getaddress.md) yöntemi döndürür [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) olası yapıları bir birleşimini içeren yapı [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md) yapısı. `dwKind` Alanını `DEBUG_ADDRESS_UNION` yapısı ayrı tutma `ADDRESS_KIND` değerini ve nasıl birleşim alanın yorumlanması gerektiğini açıklar.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetAddress](../../../extensibility/debugger/reference/idebugaddress-getaddress.md)
- [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)
- [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)
