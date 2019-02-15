---
title: FIELD_INFO_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- FIELD_INFO_FIELDS
helpviewer_keywords:
- FIELD_INFO_FIELDS enumeration
ms.assetid: a69487d2-e701-4165-804a-8a011df9a3bd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cab1d06c868f0236d1d24c186af705e9adab717e
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56317478"
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

## <a name="members"></a>Üyeler
FIF_FULLNAME  
Başlat/kullanım `bstrFullName` alanındaki [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md) yapısı.

FIF_NAME  
Başlat/kullanım `bstrName` alanındaki `FIELD_INFO` yapısı.

FIF_TYPE  
Başlat/kullanım `bstrType` alanındaki `FIELD_INFO` yapısı.

FIF_MODIFIERS  
Başlat/kullanım `bstrModifiers` alanındaki `FIELD_INFO` yapısı.

## <a name="remarks"></a>Açıklamalar
Bu değerleri de bağımsız değişken olarak geçirilen [GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md) hangi alanları belirlemek için yöntemi [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md) yapısı olan başlatılacak.

Bu değerleri de kullanılan `dwFields` üyesi `FIELD_INFO` yapısı hangi alanların kullanılan ve geçerli olduğunu belirtmek için.

Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)  
[FIELD_INFO](../../../extensibility/debugger/reference/field-info.md)  
[IDebugField](../../../extensibility/debugger/reference/idebugfield.md)  
[GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md)
