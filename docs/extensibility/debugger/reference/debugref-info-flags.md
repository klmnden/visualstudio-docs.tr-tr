---
title: DEBUGREF_INFO_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DEBUGREF_INFO_FLAGS
helpviewer_keywords:
- DEBUGREF_INFO_FLAGS enumeration
ms.assetid: 1b043327-302a-4f6d-b51d-f94f9d7c7f9d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 50efecb332be0a1cd9d9ff2c92dc97d5096eb44e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56686307"
---
# <a name="debugrefinfoflags"></a>DEBUGREF_INFO_FLAGS
Hangi bilgilerin hakkında bir hata ayıklama başvuru nesnesi alınacağını belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_DEBUGREF_INFO_FLAGS {
    DEBUGREF_INFO_NAME             = 0x00000001,
    DEBUGREF_INFO_TYPE             = 0x00000002,
    DEBUGREF_INFO_VALUE            = 0x00000004,
    DEBUGREF_INFO_ATTRIB           = 0x00000008,
    DEBUGREF_INFO_REFTYPE          = 0x00000010,
    DEBUGREF_INFO_REF              = 0x00000020,
    DEBUGREF_INFO_VALUE_AUTOEXPAND = 0x00010000,
    DEBUGREF_INFO_NONE             = 0x00000000,
    DEBUGREF_INFO_ALL              = 0xffffffff
};
typedef DWORD DEBUGREF_INFO_FLAGS;
```

```csharp
public enum enum_DEBUGREF_INFO_FLAGS {
    DEBUGREF_INFO_NAME             = 0x00000001,
    DEBUGREF_INFO_TYPE             = 0x00000002,
    DEBUGREF_INFO_VALUE            = 0x00000004,
    DEBUGREF_INFO_ATTRIB           = 0x00000008,
    DEBUGREF_INFO_REFTYPE          = 0x00000010,
    DEBUGREF_INFO_REF              = 0x00000020,
    DEBUGREF_INFO_VALUE_AUTOEXPAND = 0x00010000,
    DEBUGREF_INFO_NONE             = 0x00000000,
    DEBUGREF_INFO_ALL              = 0xffffffff
};
```

## <a name="members"></a>Üyeler
DEBUGREF_INFO_NAME başlatma/kullanım `bstrName` yapısında alan.

DEBUGREF_INFO_TYPE başlatma/kullanım `bstrType` yapısında alan.

DEBUGREF_INFO_VALUE başlatma/kullanım `bstrValue` yapısında alan.

DEBUGREF_INFO_ATTRIB başlatma/kullanım `dwAttrib` yapısında alan.

DEBUGREF_INFO_REFTYPE başlatma/kullanım `dwRefType` yapısında alan.

DEBUGREF_INFO_REF başlatma/kullanım `pReference` yapısında alan.

DEBUGREF_INFO_VALUE_AUTOEXPAND değer alanı varsa, bu nesne türü için otomatik olarak genişletilmiş değeri içermelidir.

DEBUGREF_INFO_NONE bayrak ayarlandığını gösterir.

DEBUGREF_INFO_ALL bayrakları maskesi gösterir.

## <a name="remarks"></a>Açıklamalar
Bu bayraklar geçirilen [EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md) ve [GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md) hangi alanları göstermek için yöntemlerini [DEBUG_REFERENCE_INFO](../../../extensibility/debugger/reference/debug-reference-info.md) yapısı olan başlatılacak.

İçin kullanılan `dwFields` üyesi `DEBUG_REFERENCE_INFO` yapısı yapısı döndürüldüğünde hangi alanların kullanılan ve geçerli olduğunu belirtmek için.

Bu değerler, bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [DEBUG_REFERENCE_INFO](../../../extensibility/debugger/reference/debug-reference-info.md)
- [EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md)
- [GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md)
