---
title: BPREQI_FIELDS90 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- BPREQI_FIELDS90 enumeration
ms.assetid: bf6f7efc-39f2-46a2-906d-c3647bf89995
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 3f4d6df181ac15746202ae9f67e7b8874848e8f3
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350541"
---
# <a name="bpreqifields90"></a>BPREQI_FIELDS90
Alınacak bir kesme noktası isteği bilgilerini belirtin. geçerli değerler numaralandırır. Bu numaralandırma genişletir [BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md) sabit listesi.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_BPREQI_FIELDS90
{
    // VS 8.0 values
    BPREQI90_BPLOCATION                = 0x0001,
    BPREQI90_LANGUAGE                  = 0x0002,
    BPREQI90_PROGRAM                   = 0x0004,
    BPREQI90_PROGRAMNAME               = 0x0008,
    BPREQI90_THREAD                    = 0x0010,
    BPREQI90_THREADNAME                = 0x0020,
    BPREQI90_PASSCOUNT                 = 0x0040,
    BPREQI90_CONDITION                 = 0x0080,
    BPREQI90_FLAGS                     = 0x0100,
    BPREQI90_ALLOLDFIELDS              = 0x01ff,
    BPREQI90_VENDOR                    = 0x0200,
    BPREQI90_CONSTRAINT                = 0x0400,
    BPREQI90_TRACEPOINT                = 0x0800,

    // Values added in VS 9.0
    BPREQI90_MACROTRACEPOINT           = 0x1000,

    BPREQI90_ALLFIELDS                 = 0xffff
};
typedef DWORD BPREQI_FIELDS90;
```

```csharp
public enum enum_BPREQI_FIELDS90
{
    // VS 8.0 values
    BPREQI90_BPLOCATION                = 0x0001,
    BPREQI90_LANGUAGE                  = 0x0002,
    BPREQI90_PROGRAM                   = 0x0004,
    BPREQI90_PROGRAMNAME               = 0x0008,
    BPREQI90_THREAD                    = 0x0010,
    BPREQI90_THREADNAME                = 0x0020,
    BPREQI90_PASSCOUNT                 = 0x0040,
    BPREQI90_CONDITION                 = 0x0080,
    BPREQI90_FLAGS                     = 0x0100,
    BPREQI90_ALLOLDFIELDS              = 0x01ff,
    BPREQI90_VENDOR                    = 0x0200,
    BPREQI90_CONSTRAINT                = 0x0400,
    BPREQI90_TRACEPOINT                = 0x0800,

    // Values added in VS 9.0
    BPREQI90_MACROTRACEPOINT           = 0x1000,

    BPREQI90_ALLFIELDS                 = 0xffff
};
```

## <a name="fields"></a>Alanlar
`BPREQI90_BPLOCATION`\
Başlatma veya kullanın `bpLocation` (kesme noktası konumu) alanının [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) veya [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) yapısı.

`BPREQI90_LANGUAGE`\
Başlatma veya kullanın `guidLanguage` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI90_PROGRAM`\
Başlatma veya kullanın `pProgram` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI90_PROGRAMNAME`\
Başlatma veya kullanın `bstrProgramName` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI90_THREAD`\
Başlatma veya kullanın `pThread` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI90_THREADNAME`\
Başlatma veya kullanın `bstrThreadName` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI90_PASSCOUNT`\
Başlatma veya kullanın `bpPassCount` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI90_CONDITION`\
Başlatma veya kullanın `bpCondition` (kesme noktası koşulu) alanının `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI90_FLAGS`\
Başlatma veya kullanın `dwFlags` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI90_ALLOLDFIELDS`\
Başlatma veya tüm alanlar için kullanın, `BP_REQUEST_INFO` yapısı.

`BPREQI90_VENDOR`\
Başlatma veya kullanın `guidVendor` alanını `BP_REQUEST_INFO2` yapısı.

`BPREQI90_CONSTRAINT`\
Başlatma veya kullanın `bstrConstraint` alanını `BP_REQUEST_INFO2` yapısı.

`BPREQI90_TRACEPOINT`\
Başlatma veya kullanın `bstrTracepoint` alanını `BP_REQUEST_INFO2` yapısı.

`BPREQI90_MACROTRACEPOINT`\
Başlatma veya kullanın `bstrMacroTracepoint` alanını `BP_REQUEST_INFO2` yapısı. Bu alan BPREQI_ALLFIELDS içermez.

`BPREQI90_ALLFIELDS`\
Tüm alanlar için belirtir `BP_REQUEST_INFO2` yapısı.

## <a name="requirements"></a>Gereksinimler
Üst bilgi: Msdbg90.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
