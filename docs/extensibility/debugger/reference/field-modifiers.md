---
title: FIELD_MODIFIERS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- FIELD_MODIFIERS
helpviewer_keywords:
- FIELD_MODIFIERS enumeration
ms.assetid: 1e44681c-1f03-41a9-9c04-b79f231b0822
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b22559af26a0a5f6c8af68726a5ba336e1bcfb4a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56689635"
---
# <a name="fieldmodifiers"></a>FIELD_MODIFIERS
Alan türü için değiştiriciler belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_FIELD_MODIFIERS {
    FIELD_MOD_NONE             = 0x00000000,

    // Modifier of the field
    FIELD_MOD_ACCESS_NONE      = 0x00000001,
    FIELD_MOD_ACCESS_PUBLIC    = 0x00000002,
    FIELD_MOD_ACCESS_PROTECTED = 0x00000004,
    FIELD_MOD_ACCESS_PRIVATE   = 0x00000008,

    // Storage modifier of the field
    FIELD_MOD_NOMODIFIERS      = 0x00000010,
    FIELD_MOD_STATIC           = 0x00000020,
    FIELD_MOD_CONSTANT         = 0x00000040,
    FIELD_MOD_TRANSIENT        = 0x00000080,
    FIELD_MOD_VOLATILE         = 0x00000100,
    FIELD_MOD_ABSTRACT         = 0x00000200,
    FIELD_MOD_NATIVE           = 0x00000400,
    FIELD_MOD_SYNCHRONIZED     = 0x00000800,
    FIELD_MOD_VIRTUAL          = 0x00001000,
    FIELD_MOD_INTERFACE        = 0x00002000,
    FIELD_MOD_FINAL            = 0x00004000,
    FIELD_MOD_SENTINEL         = 0x00008000,
    FIELD_MOD_INNERCLASS       = 0x00010000,
    FIELD_TYPE_OPTIONAL        = 0x00020000,
    FIELD_MOD_BYREF            = 0x00040000,
    FIELD_MOD_HIDDEN           = 0x00080000,
    FIELD_MOD_MARSHALASOBJECT  = 0x00100000,
    FIELD_MOD_SPECIAL_NAME     = 0x00200000,
    FIELD_MOD_HIDEBYSIG        = 0x00400000,

    FIELD_MOD_WRITEONLY        = 0x80000000,
    FIELD_MOD_ACCESS_MASK      = 0x000000ff,
    FIELD_MOD_MASK             = 0xffffff00,
    FIELD_MOD_ALL              = 0x7fffffff
};
typedef DWORD FIELD_MODIFIERS;
```

```csharp
public enum enum_FIELD_MODIFIERS {
    FIELD_MOD_NONE             = 0x00000000,

    // Modifier of the field
    FIELD_MOD_ACCESS_NONE      = 0x00000001,
    FIELD_MOD_ACCESS_PUBLIC    = 0x00000002,
    FIELD_MOD_ACCESS_PROTECTED = 0x00000004,
    FIELD_MOD_ACCESS_PRIVATE   = 0x00000008,

    // Storage modifier of the field
    FIELD_MOD_NOMODIFIERS      = 0x00000010,
    FIELD_MOD_STATIC           = 0x00000020,
    FIELD_MOD_CONSTANT         = 0x00000040,
    FIELD_MOD_TRANSIENT        = 0x00000080,
    FIELD_MOD_VOLATILE         = 0x00000100,
    FIELD_MOD_ABSTRACT         = 0x00000200,
    FIELD_MOD_NATIVE           = 0x00000400,
    FIELD_MOD_SYNCHRONIZED     = 0x00000800,
    FIELD_MOD_VIRTUAL          = 0x00001000,
    FIELD_MOD_INTERFACE        = 0x00002000,
    FIELD_MOD_FINAL            = 0x00004000,
    FIELD_MOD_SENTINEL         = 0x00008000,
    FIELD_MOD_INNERCLASS       = 0x00010000,
    FIELD_TYPE_OPTIONAL        = 0x00020000,
    FIELD_MOD_BYREF            = 0x00040000,
    FIELD_MOD_HIDDEN           = 0x00080000,
    FIELD_MOD_MARSHALASOBJECT  = 0x00100000,
    FIELD_MOD_SPECIAL_NAME     = 0x00200000,
    FIELD_MOD_HIDEBYSIG        = 0x00400000,

    FIELD_MOD_WRITEONLY        = 0x80000000,
    FIELD_MOD_ACCESS_MASK      = 0x000000ff,
    FIELD_MOD_MASK             = 0xffffff00,
    FIELD_MOD_ALL              = 0x7fffffff
};
```

## <a name="members"></a>Üyeler
Alan erişilemez FIELD_MOD_ACCESS_TYPE gösterir.

FIELD_MOD_ACCESS_PUBLIC alan genel erişimi olduğunu gösterir.

FIELD_MOD_ACCESS_PROTECTED alan Korumalı Erişim olduğunu gösterir.

FIELD_MOD_ACCESS_PRIVATE alan özel erişimi olduğunu gösterir.

FIELD_MOD_NOMODIFIERS, alanın hiç değiştiricilere sahip olduğunu gösterir.

FIELD_MOD_STATIC alan statik olduğunu gösterir.

FIELD_MOD_CONSTANT alan bir sabit olduğunu gösterir.

FIELD_MOD_TRANSIENT alan geçici olduğunu gösterir.

FIELD_MOD_VOLATILE alan geçici olduğunu gösterir.

FIELD_MOD_ABSTRACT alan soyut olduğunu gösterir.

FIELD_MOD_NATIVE alanının yerel olup olmadığını gösterir.

Alan eşitlenir FIELD_MOD_SYNCHRONIZED gösterir.

FIELD_MOD_VIRTUAL alan sanal olduğunu gösterir.

FIELD_MOD_INTERFACE alanının bir arabirim olup olmadığını gösterir.

FIELD_MOD_FINAL alanın son olduğunu gösterir.

FIELD_MOD_SENTINEL alan bir sentinel olduğunu gösterir.

FIELD_MOD_INNERCLASS alan bir iç sınıf olduğunu gösterir.

FIELD_TYPE_OPTIONAL alan isteğe bağlı olduğunu gösterir.

FIELD_MOD_BYREF alanın başvuru bağımsız değişkeni olduğunu gösterir. Bu, özellikle yöntem bağımsız olur.

FIELD_MOD_HIDDEN alanı gizli veya başka bir bağlamda sunulan olduğunu gösterir. Örneğin, [!INCLUDE[vbprvb](../../../code-quality/includes/vbprvb_md.md)] statik yerel öğeler.

FIELD_MOD_MARSHALASOBJECT alan bir nesne ile temsil ettiğini gösteren bir `IUnknown` arabirimi.

Alan özel bir ad gibi bulunduğunu FIELD_MOD_SPECIAL_NAME belirtir `.ctor` bir oluşturucu için ([!INCLUDE[vbprvb](../../../code-quality/includes/vbprvb_md.md)] yalnızca).

Alanın bulunduğu FIELD_MOD_HIDEBYSIG gösterir `Overloads` uygulanmış anahtar sözcüğü ([!INCLUDE[vbprvb](../../../code-quality/includes/vbprvb_md.md)] yalnızca).

Alanın salt yazılır FIELD_MOD_WRITEONLY gösterir. Bu değer yer almayan `FIELD_MOD_ALL`gibi yalnızca bu tür salt yazılır alanlar İşlev değerlendirmesi için kullanılır. Bir kullanıcı için açıkça kaldırmasını `FIELD_MOD_WRITEONLY` alanları.

FIELD_MOD_ACCESS_MASK bir alan erişim maskesi belirtir.

Alan değiştiricilerini için bir maske FIELD_MOD_MASK gösterir.

## <a name="remarks"></a>Açıklamalar
İçin kullanılan `dwModifiers` üyesi [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md) yapısı.

Bu değerleri de geçirilen [EnumFields](../../../extensibility/debugger/reference/idebugcontainerfield-enumfields.md) belirli alanlar için filtre uygulamak için yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md)
- [EnumFields](../../../extensibility/debugger/reference/idebugcontainerfield-enumfields.md)
