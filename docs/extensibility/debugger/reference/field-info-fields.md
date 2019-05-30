---
title: FIELD_INFO_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- FIELD_INFO_FIELDS
helpviewer_keywords:
- FIELD_INFO_FIELDS enumeration
ms.assetid: a69487d2-e701-4165-804a-8a011df9a3bd
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 01853df78bfe731ea4b7159f7b3ebe352f3c5eaa
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66337680"
---
# <a name="fieldinfofields"></a>FIELD_INFO_FIELDS
Hangi bilgilerin hakkında alınacağını belirtir bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesne.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_FIELD_INFO_FIELDS { 
    FIF_FULLNAME  = 0x0001,
    FIF_NAME      = 0x0002,
    FIF_TYPE      = 0x0004,
    FIF_MODIFIERS = 0x0008,
    FIF_ALL       = 0xffffffff,
    FIF_NONE      = 0x0000
};
typedef DWORD FIELD_INFO_FIELDS;
```

```csharp
public enum enum_FIELD_INFO_FIELDS {
    FIF_FULLNAME  = 0x0001,
    FIF_NAME      = 0x0002,
    FIF_TYPE      = 0x0004,
    FIF_MODIFIERS = 0x0008,
    FIF_ALL       = 0xffffffff,
    FIF_NONE      = 0x0000
};
```

## <a name="fields"></a>Alanlar
`FIF_FULLNAME`\
Başlat/kullanım `bstrFullName` alanındaki [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md) yapısı.

`FIF_NAME`\
Başlat/kullanım `bstrName` alanındaki `FIELD_INFO` yapısı.

`FIF_TYPE`\
Başlat/kullanım `bstrType` alanındaki `FIELD_INFO` yapısı.

`FIF_MODIFIERS`\
Başlat/kullanım `bstrModifiers` alanındaki `FIELD_INFO` yapısı.

## <a name="remarks"></a>Açıklamalar
Bu değerleri de bağımsız değişken olarak geçirilen [GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md) hangi alanları belirlemek için yöntemi [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md) yapısı olan başlatılacak.

Bu değerleri de kullanılan `dwFields` üyesi `FIELD_INFO` yapısı hangi alanların kullanılan ve geçerli olduğunu belirtmek için.

Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md)
