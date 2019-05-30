---
title: DEBUGREF_INFO_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DEBUGREF_INFO_FLAGS
helpviewer_keywords:
- DEBUGREF_INFO_FLAGS enumeration
ms.assetid: 1b043327-302a-4f6d-b51d-f94f9d7c7f9d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 1adab87ed09ca2ff16d837da084d8cc0b76956fe
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66318364"
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

## <a name="fields"></a>Alanlar
`DEBUGREF_INFO_NAME`\
Başlat/kullanım `bstrName` yapısında alan.

`DEBUGREF_INFO_TYPE`\
Başlat/kullanım `bstrType` yapısında alan.

`DEBUGREF_INFO_VALUE`\
Başlat/kullanım `bstrValue` yapısında alan.

`DEBUGREF_INFO_ATTRIB`\
Başlat/kullanım `dwAttrib` yapısında alan.

`DEBUGREF_INFO_REFTYPE`\
Başlat/kullanım `dwRefType` yapısında alan.

`DEBUGREF_INFO_REF`\
Başlat/kullanım `pReference` yapısında alan.

`DEBUGREF_INFO_VALUE_AUTOEXPAND`\
Değer alanı otomatik olarak genişletilmiş değeri varsa, bu nesne türü içermelidir.

`DEBUGREF_INFO_NONE`\
Bayrak belirlendiğini gösterir.

`DEBUGREF_INFO_ALL`\
Maske bayrakları belirtir.

## <a name="remarks"></a>Açıklamalar
Bu bayraklar geçirilen [EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md) ve [GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md) hangi alanları göstermek için yöntemlerini [DEBUG_REFERENCE_INFO](../../../extensibility/debugger/reference/debug-reference-info.md) yapısı olan başlatılacak.

İçin kullanılan `dwFields` üyesi `DEBUG_REFERENCE_INFO` yapısı yapısı döndürüldüğünde hangi alanların kullanılan ve geçerli olduğunu belirtmek için.

Bu değerler, bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [DEBUG_REFERENCE_INFO](../../../extensibility/debugger/reference/debug-reference-info.md)
- [EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md)
- [GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md)
