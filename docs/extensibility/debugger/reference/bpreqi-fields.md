---
title: BPREQI_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BPREQI_FIELDS
helpviewer_keywords:
- BPREQI_FIELDS enumeration
ms.assetid: 679e771e-4a79-484e-af37-f962ef4aa245
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 757b8bfeeed2a7d75f3a0b4203b80b464e5b39fa
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350502"
---
# <a name="bpreqifields"></a>BPREQI_FIELDS
Bir kesme noktası isteği hakkında alınacak bilgileri belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_BPREQI_FIELDS {
    BPREQI_BPLOCATION   = 0x0001,
    BPREQI_LANGUAGE     = 0x0002,
    BPREQI_PROGRAM      = 0x0004,
    BPREQI_PROGRAMNAME  = 0x0008,
    BPREQI_THREAD       = 0x0010,
    BPREQI_THREADNAME   = 0x0020,
    BPREQI_PASSCOUNT    = 0x0040,
    BPREQI_CONDITION    = 0x0080,
    BPREQI_FLAGS        = 0x0100,
    BPREQI_ALLOLDFIELDS = 0x01ff
    BPREQI_VENDOR       = 0x0200,   // BP_REQUEST_INFO2 only
    BPREQI_CONSTRAINT   = 0x0400,   // BP_REQUEST_INFO2 only
    BPREQI_TRACEPOINT   = 0x0800,   // BP_REQUEST_INFO2 only
    BPREQI_ALLFIELDS    = 0x0fff    // BP_REQUEST_INFO2 only
};
typedef DWORD BPREQI_FIELDS;
```

```csharp
public enum enum_BPREQI_FIELDS {
    BPREQI_BPLOCATION   = 0x0001,
    BPREQI_LANGUAGE     = 0x0002,
    BPREQI_PROGRAM      = 0x0004,
    BPREQI_PROGRAMNAME  = 0x0008,
    BPREQI_THREAD       = 0x0010,
    BPREQI_THREADNAME   = 0x0020,
    BPREQI_PASSCOUNT    = 0x0040,
    BPREQI_CONDITION    = 0x0080,
    BPREQI_FLAGS        = 0x0100,
    BPREQI_ALLOLDFIELDS = 0x01ff
    BPREQI_VENDOR       = 0x0200,   // BP_REQUEST_INFO2 only
    BPREQI_CONSTRAINT   = 0x0400,   // BP_REQUEST_INFO2 only
    BPREQI_TRACEPOINT   = 0x0800,   // BP_REQUEST_INFO2 only
    BPREQI_ALLFIELDS    = 0x0fff    // BP_REQUEST_INFO2 only
};
```

## <a name="fields"></a>Alanlar
`BPREQI_BPLOCATION`\
Başlat/kullanım `bpLocation` (kesme noktası konumu) alanının [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) veya [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) yapısı.

`BPREQI_LANGUAGE`\
Başlat/kullanım `guidLanguage` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI_PROGRAM`\
Başlat/kullanım `pProgram` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI_PROGRAMNAME`\
Başlat/kullanım `bstrProgramName` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI_THREAD`\
Başlat/kullanım `pThread` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI_THREADNAME`\
Başlat/kullanım `bstrThreadName` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI_PASSCOUNT`\
Başlat/kullanım `bpPassCount` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI_CONDITION`\
Başlat/kullanım `bpCondition` (kesme noktası koşulu) alanının `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI_FLAGS`\
Başlat/kullanım `dwFlags` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

`BPREQI_ALLOLDFIELDS`\
Başlat/tüm alanlar için kullanım, `BP_REQUEST_INFO` yapısı.

`BPREQI_VENDOR`\
Başlat/kullanım `guidVendor` alanını `BP_REQUEST_INFO2` yapısı.

`BPREQI_CONSTRAINT`\
Başlat/kullanım `bstrConstraint` alanını `BP_REQUEST_INFO2` yapısı.

`BPREQI_TRACEPOINT`\
Başlat/kullanım `bstrTracepoint` alanını `BP_REQUEST_INFO2` yapısı.

`BPREQI_ALLFIELDS`\
Tüm alanlar için belirtir `BP_REQUEST_INFO2` yapısı.

## <a name="remarks"></a>Açıklamalar
Bağımsız değişken olarak geçirilen [GetRequestInfo](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getrequestinfo.md) ve [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) hangi alanları belirlemek için yöntemleri [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) ve [BP_REQUEST_INFO2 ](../../../extensibility/debugger/reference/bp-request-info2.md) yapıları, başlatılacak.

Bu bayraklar Ayrıca hangi alanları göstermek için kullanılan `BP_REQUEST_INFO` ve `BP_REQUEST_INFO2` yapıları, kullanılan ve geçerli her yapı döndürüldüğünde.

Bu değerler, bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetRequestInfo](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getrequestinfo.md)
- [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)
- [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)
