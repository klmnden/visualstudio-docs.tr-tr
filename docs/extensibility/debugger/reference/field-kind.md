---
title: FIELD_KIND | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- FIELD_KIND
helpviewer_keywords:
- FIELD_KIND enumeration
ms.assetid: fd522b9c-52e2-42fa-939d-343347d5c3b1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 46b965def820771b0bab883c1bdd9bf90d18414e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62924438"
---
# <a name="fieldkind"></a>FIELD_KIND
Yer alan türünü belirten bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesne.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_FIELD_KIND {
    FIELD_KIND_NONE       = 0x00000000,

    // Type of field
    FIELD_KIND_TYPE       = 0x00000001,
    FIELD_KIND_SYMBOL     = 0x00000002,

    // Storage type of the field
    FIELD_TYPE_PRIMITIVE  = 0x00000010,
    FIELD_TYPE_STRUCT     = 0x00000020,
    FIELD_TYPE_CLASS      = 0x00000040,
    FIELD_TYPE_INTERFACE  = 0x00000080,
    FIELD_TYPE_UNION      = 0x00000100,
    FIELD_TYPE_ARRAY      = 0x00000200,
    FIELD_TYPE_METHOD     = 0x00000400,
    FIELD_TYPE_BLOCK      = 0x00000800,
    FIELD_TYPE_POINTER    = 0x00001000,
    FIELD_TYPE_ENUM       = 0x00002000,
    FIELD_TYPE_LABEL      = 0x00004000,
    FIELD_TYPE_TYPEDEF    = 0x00008000,
    FIELD_TYPE_BITFIELD   = 0x00010000,
    FIELD_TYPE_NAMESPACE  = 0x00020000,
    FIELD_TYPE_MODULE     = 0x00040000,
    FIELD_TYPE_DYNAMIC    = 0x00080000,
    FIELD_TYPE_PROP       = 0x00100000,
    FIELD_TYPE_INNERCLASS = 0x00200000,
    FIELD_TYPE_REFERENCE  = 0x00400000,
    FIELD_TYPE_EXTENDED   = 0x00800000,

    // Specific information about symbols
    FIELD_SYM_MEMBER      = 0x01000000,
    FIELD_SYM_LOCAL       = 0x02000000,
    FIELD_SYM_PARAM       = 0x04000000,
    FIELD_SYM_THIS        = 0x08000000,
    FIELD_SYM_GLOBAL      = 0x10000000,
    FIELD_SYM_PROP_GETTER = 0x20000000,
    FIELD_SYM_PROP_SETTER = 0x40000000,
    FIELD_SYM_EXTENDED    = 0x80000000,

    FIELD_KIND_MASK       = 0x0000000f,
    FIELD_TYPE_MASK       = 0x00fffff0,
    FIELD_SYM_MASK        = 0xff000000,

    FIELD_KIND_ALL        = 0xffffffff
};
typedef DWORD FIELD_KIND;
```

```csharp
public enum enum_FIELD_KIND {
    FIELD_KIND_NONE       = 0x00000000,

    // Type of field
    FIELD_KIND_TYPE       = 0x00000001,
    FIELD_KIND_SYMBOL     = 0x00000002,

    // Storage type of the field
    FIELD_TYPE_PRIMITIVE  = 0x00000010,
    FIELD_TYPE_STRUCT     = 0x00000020,
    FIELD_TYPE_CLASS      = 0x00000040,
    FIELD_TYPE_INTERFACE  = 0x00000080,
    FIELD_TYPE_UNION      = 0x00000100,
    FIELD_TYPE_ARRAY      = 0x00000200,
    FIELD_TYPE_METHOD     = 0x00000400,
    FIELD_TYPE_BLOCK      = 0x00000800,
    FIELD_TYPE_POINTER    = 0x00001000,
    FIELD_TYPE_ENUM       = 0x00002000,
    FIELD_TYPE_LABEL      = 0x00004000,
    FIELD_TYPE_TYPEDEF    = 0x00008000,
    FIELD_TYPE_BITFIELD   = 0x00010000,
    FIELD_TYPE_NAMESPACE  = 0x00020000,
    FIELD_TYPE_MODULE     = 0x00040000,
    FIELD_TYPE_DYNAMIC    = 0x00080000,
    FIELD_TYPE_PROP       = 0x00100000,
    FIELD_TYPE_INNERCLASS = 0x00200000,
    FIELD_TYPE_REFERENCE  = 0x00400000,
    FIELD_TYPE_EXTENDED   = 0x00800000,

    // Specific information about symbols
    FIELD_SYM_MEMBER      = 0x01000000,
    FIELD_SYM_LOCAL       = 0x02000000,
    FIELD_SYM_PARAM       = 0x04000000,
    FIELD_SYM_THIS        = 0x08000000,
    FIELD_SYM_GLOBAL      = 0x10000000,
    FIELD_SYM_PROP_GETTER = 0x20000000,
    FIELD_SYM_PROP_SETTER = 0x40000000,
    FIELD_SYM_EXTENDED    = 0x80000000,

    FIELD_KIND_MASK       = 0x0000000f,
    FIELD_TYPE_MASK       = 0x00fffff0,
    FIELD_SYM_MASK        = 0xff000000,

    FIELD_KIND_ALL        = 0xffffffff
};
```

## <a name="members"></a>Üyeler
FIELD_KIND_TYPE alanı yalnızca bir tür olduğunu gösterir.

FIELD_KIND_SYMBOL alan türü, adı ve diğer bilgilerle birlikte bir sembol belirtir.

FIELD_TYPE_PRIMITIVE alanın bir temel veri türü olduğunu gösterir.

FIELD_TYPE_STRUCT alan bir yapı olduğunu gösterir.

FIELD_TYPE_CLASS alanın bir sınıf olduğunu gösterir.

FIELD_TYPE_INTERFACE alanının bir arabirim olup olmadığını gösterir.

FIELD_TYPE_UNION alanın bir birleşim olduğunu gösterir.

FIELD_TYPE_ARRAY alan bir dizi olduğunu gösterir.

FIELD_TYPE_METHOD alan bir yöntem olduğunu gösterir.

FIELD_TYPE_BLOCK alan bir bloğu gösterir.

FIELD_TYPE_POINTER alan bir işaretçi olduğunu gösterir.

FIELD_TYPE_ENUM alan listelenmiş veri türü olduğunu gösterir.

FIELD_TYPE_LABEL alan bir etiketi gösterilir.

FIELD_TYPE_TYPEDEF alan bir tür tanımı olduğunu gösterir.

FIELD_TYPE_BITFIELD alan bir bit alanı olduğunu gösterir.

FIELD_TYPE_NAMESPACE alan bir ad alanı olduğunu gösterir.

FIELD_TYPE_MODULE alan bir modül olduğunu gösterir.

FIELD_TYPE_DYNAMIC alan dinamik olduğunu gösterir.

FIELD_TYPE_PROP alanın bir özellik olduğunu gösterir.

FIELD_TYPE_INNERCLASS alan bir iç sınıf olduğunu gösterir.

FIELD_TYPE_REFERENCE alanın başvuru olduğunu gösterir.

Ayrılmış FIELD_TYPE_EXTENDED gelecekte kullanım için.

FIELD_SYM_MEMBER alanın üyesi olduğunu gösterir.

FIELD_SYM_LOCAL alanının yerel olup olmadığını gösterir.

FIELD_SYM_PARAMETER alanın bir parametre olduğunu gösterir.

FIELD_SYM_THIS alan "Bu" işaretçiyi olduğunu gösterir.

FIELD_SYM_GLOBAL alan genel olduğunu gösterir.

Alan özellikleri alır FIELD_SYM_PROP_GETTER gösterir.

Alan özelliklerini ayarlar FIELD_SYM_PROP_SETTER gösterir.

Ayrılmış FIELD_SYM_EXTENDED gelecekte kullanım için.

Alan türleri için bir maske FIELD_KIND_MASK gösterir.

Alan türleri için bir maske FIELD_TYPE_MASK gösterir.

Sembol bilgisi için bir maske FIELD_SYM_MASK gösterir.

## <a name="remarks"></a>Açıklamalar
Çağrısından döndürülen [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) yöntemi.

Bu alanın türünü bağlı olarak [QueryInterface](/cpp/atl/queryinterface) üzerinde çağrılabilir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabiriminin daha belirli bir form arabirimi. Örneğin, varsa [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) döndürür `FIELD_TYPE_METHOD`, ardından çağırabilirsiniz `QueryInterface` miyim üzerinde`DebugField` almak için [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md) arabirimi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [FIELD_MODIFIERS](../../../extensibility/debugger/reference/field-modifiers.md)
- [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
