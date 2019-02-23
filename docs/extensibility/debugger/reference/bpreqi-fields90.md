---
title: BPREQI_FIELDS90 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- BPREQI_FIELDS90 enumeration
ms.assetid: bf6f7efc-39f2-46a2-906d-c3647bf89995
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: be07e034b4059ae7ade40a5a248c01bc4a8237b8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56695940"
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

#### <a name="parameters"></a>Parametreler
BPREQI90_BPLOCATION başlatmak veya kullanım `bpLocation` (kesme noktası konumu) alanının [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) veya [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) yapısı.

BPREQI90_LANGUAGE başlatmak veya kullanım `guidLanguage` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI90_PROGRAM başlatmak veya kullanım `pProgram` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI90_PROGRAMNAME başlatmak veya kullanım `bstrProgramName` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI90_THREAD başlatmak veya kullanım `pThread` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI90_THREADNAME başlatmak veya kullanım `bstrThreadName` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI90_PASSCOUNT başlatmak veya kullanım `bpPassCount` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI90_CONDITION başlatmak veya kullanım `bpCondition` (kesme noktası koşulu) alanının `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI90_FLAGS başlatmak veya kullanım `dwFlags` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI90_ALLOLDFIELDS başlatmak veya tüm alanları için kullanın, `BP_REQUEST_INFO` yapısı.

BPREQI90_VENDOR başlatmak veya kullanım `guidVendor` alanını `BP_REQUEST_INFO2` yapısı.

BPREQI90_CONSTRAINT başlatmak veya kullanım `bstrConstraint` alanını `BP_REQUEST_INFO2` yapısı.

BPREQI90_TRACEPOINT başlatmak veya kullanım `bstrTracepoint` alanını `BP_REQUEST_INFO2` yapısı.

BPREQI90_MACROTRACEPOINT başlatmak veya kullanım `bstrMacroTracepoint` alanını `BP_REQUEST_INFO2` yapısı. Bu alan BPREQI_ALLFIELDS içermez.

BPREQI90_ALLFIELDS belirtir, tüm alanları `BP_REQUEST_INFO2` yapısı.

## <a name="requirements"></a>Gereksinimler
Üst bilgi: Msdbg90.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
