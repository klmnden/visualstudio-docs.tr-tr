---
title: CODE_PATH | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CODE_PATH
helpviewer_keywords:
- CODE_PATH structure
ms.assetid: 2d4b2890-4c9d-47e1-83c0-df9c6436427f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 516122ee8aaaa0ed18537369eeeffb05be3ebf1c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66327220"
---
# <a name="codepath"></a>CODE_PATH
Bir yöntem veya işlev çağrısı açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct tagCODE_PATH { 
    BSTR                bstrName;
    IDebugCodeContext2* pCode;
} CODE_PATH;
```

```csharp
public struct CODE_PATH {
    public string            bstrName;
    public IDebugCodeContext pCode;
}
```

## <a name="members"></a>Üyeler
`bstrName`\
Kod yolu adı.

`pCode`\
[IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) bir işleve için kodu nerede tanımlayan nesne.

## <a name="remarks"></a>Açıklamalar
Bu yapı, bir işlevin Adımlama uygulamak için kullanılır. [EnumCodePaths](../../../extensibility/debugger/reference/idebugprogram2-enumcodepaths.md) tüm çağrıları ayıklanan programın geçerli konumu döndürür. Bu yapı, böyle bir çağrısını temsil eder.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)
- [EnumCodePaths](../../../extensibility/debugger/reference/idebugprogram2-enumcodepaths.md)
