---
title: DISASSEMBLY_STREAM_SCOPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DISASSEMBLY_STREAM_SCOPE
helpviewer_keywords:
- DISASSEMBLY_STREAM_SCOPE enumeration
ms.assetid: 43e2b364-cbbe-4755-a7e6-a03f3054c965
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 724e32f83cfec31c2bacdab661407983af87efe6
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66318250"
---
# <a name="disassemblystreamscope"></a>DISASSEMBLY_STREAM_SCOPE
Ayrıştırılmış kod akışın kapsamını belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_DISASSEMBLY_STREAM_SCOPE {
    DSS_HUGE     = 0x10000000,
    DSS_FUNCTION = 0x0001,
    DSS_MODULE   = (DSS_HUGE) | 0x0002,
    DSS_ALL      = (DSS_HUGE) | 0x0003
};
typedef DWORD DISASSEMBLY_STREAM_SCOPE;
```

```csharp
public enum enum_DISASSEMBLY_STREAM_SCOPE {
    DSS_HUGE     = 0x10000000,
    DSS_FUNCTION = 0x0001,
    DSS_MODULE   = (DSS_HUGE) | 0x0002,
    DSS_ALL      = (DSS_HUGE) | 0x0003
};
```

## <a name="fields"></a>Alanlar
`DSS_HUGE`\
Kod bağlamı derlemesini açma işlemlerini uygulama istemci genellikle tek bir çağrıda almak daha daha fazla çıkış karşılaşırsınız belirtir.

`DSS_FUNCTION`\
Kod kapsamında yer alan işlevi çözülürken olduğunu belirtir. Ayrıştırılmış kod akış tarafından döndürülen bir işlevi temsil ettiğini belirtir [GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md) yöntemi.

`DSS_MODULE`\
Tarafından döndürülen `IDebugDisassemblyStream2::GetScope` yöntemi Ayrıştırılmış kod akış bir modülü temsil ettiğini belirtir.

`DSS_ALL`\
Tüm adres için ayrıştırılmış kodu belirtir.

## <a name="remarks"></a>Açıklamalar
Bağımsız değişken olarak geçirilen [GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md) yöntemi ve tarafından döndürülen [GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md) yöntemi.

Bu değerler, bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md)
- [GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md)
