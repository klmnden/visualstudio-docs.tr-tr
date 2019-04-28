---
title: DISASSEMBLY_STREAM_SCOPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DISASSEMBLY_STREAM_SCOPE
helpviewer_keywords:
- DISASSEMBLY_STREAM_SCOPE enumeration
ms.assetid: 43e2b364-cbbe-4755-a7e6-a03f3054c965
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 446b0eec7593457ed2cd384eb9a6bca383094e62
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62924474"
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

## <a name="members"></a>Üyeler
DSS_HUGE kod bağlamı derlemesini açma işlemlerini uygulama bir istemci'den daha fazla çıktı üretir belirten tek bir çağrıda almak genellikle istersiniz.

DSS_FUNCTION, kod kapsamında yer alan işlevi çözülürken olduğunu belirtir. Ayrıştırılmış kod akış tarafından döndürülen bir işlevi temsil ettiğini belirtir [GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md) yöntemi.

Tarafından döndürülen DSS_MODULE olduğunda `IDebugDisassemblyStream2::GetScope` yöntemi Ayrıştırılmış kod akış bir modülü temsil ettiğini belirtir.

Tüm adres için ayrıştırılmış DSS_ALL belirtir.

## <a name="remarks"></a>Açıklamalar
Bağımsız değişken olarak geçirilen [GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md) yöntemi ve tarafından döndürülen [GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md) yöntemi.

Bu değerler, bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md)
- [GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md)
