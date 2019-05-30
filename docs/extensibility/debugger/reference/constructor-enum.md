---
title: CONSTRUCTOR_ENUM | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CONSTRUCTOR_ENUM
helpviewer_keywords:
- CONSTRUCTOR_ENUM enumeration
ms.assetid: 6d335b2c-66bc-460c-a4a6-4f3f1b697c2c
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: ea240cf33bab70f1488a2aa90fecd71220b1da25
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66346446"
---
# <a name="constructorenum"></a>CONSTRUCTOR_ENUM
Farklı türlerde oluşturucular seçer.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef enum ConstructorMatchOptions {
    crAll       = 0,
    crNonStatic = 1,
    crStatic    = 2
} CONSTRUCTOR_ENUM;
```

```csharp
public enum ConstructorMatchOptions {
    crAll       = 0,
    crNonStatic = 1,
    crStatic    = 2
};
```

## <a name="fields"></a>Alanlar
`crAll`\
Tüm oluşturucular seçer.

`crNonStatic`\
Statik olmayan oluşturucular seçer.

`crStatic`\
Statik oluşturucular seçer.

## <a name="remarks"></a>Açıklamalar
Bağımsız değişken olarak geçirilen [EnumConstructors](../../../extensibility/debugger/reference/idebugclassfield-enumconstructors.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)
