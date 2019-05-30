---
title: FIELD_KIND_EX | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- FIELD_KIND_EX enumeration
ms.assetid: 922c3208-1e94-485f-b70a-3bc96affeff8
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: fd481883c826ff21a82b52bdd82de087b6219b58
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66309011"
---
# <a name="fieldkindex"></a>FIELD_KIND_EX
Ek alanları türlerini numaralandırır, bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesne içerebilir. Bu numaralandırma genişletir [FIELD_KIND](../../../extensibility/debugger/reference/field-kind.md) sabit listesi.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_FIELD_KIND_EX
{
    FIELD_KIND_EX_NONE = 0,
    FIELD_TYPE_EX_METHODVAR = 0x1,
    FIELD_TYPE_EX_CLASSVAR = 0x2
};
typedef DWORD FIELD_KIND_EX;
```

```csharp
public enum enum_FIELD_KIND_EX
{
    FIELD_KIND_EX_NONE = 0,
    FIELD_TYPE_EX_METHODVAR = 0x1,
    FIELD_TYPE_EX_CLASSVAR = 0x2
};
```

## <a name="fields"></a>Alanlar
`FIELD_KIND_EX_NONE`\
Alan genişletilmiş bir türü içermiyor.

`FIELD_TYPE_EX_METHODVAR`\
Alan bir yöntem değişken içerir.

`FIELD_TYPE_EX_CLASSVAR`\
Bir sınıf değişkeni alan içerir.

## <a name="requirements"></a>Gereksinimler
Üst bilgi: Sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetExtendedKind](../../../extensibility/debugger/reference/idebugextendedfield-getextendedkind.md)
