---
title: FIELD_KIND_EX | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- FIELD_KIND_EX enumeration
ms.assetid: 922c3208-1e94-485f-b70a-3bc96affeff8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 28a880af0a5d691a57e32b22f9f7823cca45827d
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56317789"
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

## <a name="members"></a>Üyeler
FIELD_KIND_EX_NONE  
Alan genişletilmiş bir türü içermiyor.

FIELD_TYPE_EX_METHODVAR  
Alan bir yöntem değişken içerir.

FIELD_TYPE_EX_CLASSVAR  
Bir sınıf değişkeni alan içerir.

## <a name="requirements"></a>Gereksinimler
Üst bilgi: Sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)  
[GetExtendedKind](../../../extensibility/debugger/reference/idebugextendedfield-getextendedkind.md)
