---
title: BPREQI_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BPREQI_FIELDS
helpviewer_keywords:
- BPREQI_FIELDS enumeration
ms.assetid: 679e771e-4a79-484e-af37-f962ef4aa245
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 25b95e2934de9d09ef9541162b05920a04f645bd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62924763"
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

## <a name="members"></a>Üyeler
BPREQI_BPLOCATION başlatma/kullanım `bpLocation` (kesme noktası konumu) alanının [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) veya [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) yapısı.

BPREQI_LANGUAGE başlatma/kullanım `guidLanguage` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI_PROGRAM başlatma/kullanım `pProgram` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI_PROGRAMNAME başlatma/kullanım `bstrProgramName` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI_THREAD başlatma/kullanım `pThread` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI_THREADNAME başlatma/kullanım `bstrThreadName` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI_PASSCOUNT başlatma/kullanım `bpPassCount` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI_CONDITION başlatma/kullanım `bpCondition` (kesme noktası koşulu) alanının `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI_FLAGS başlatma/kullanım `dwFlags` alanını `BP_REQUEST_INFO` veya `BP_REQUEST_INFO2` yapısı.

BPREQI_ALLOLDFIELDS Başlat/tüm kullanım alanları, `BP_REQUEST_INFO` yapısı.

BPREQI_VENDOR başlatma/kullanım `guidVendor` alanını `BP_REQUEST_INFO2` yapısı.

BPREQI_CONSTRAINT başlatma/kullanım `bstrConstraint` alanını `BP_REQUEST_INFO2` yapısı.

BPREQI_TRACEPOINT başlatma/kullanım `bstrTracepoint` alanını `BP_REQUEST_INFO2` yapısı.

BPREQI_ALLFIELDS belirtir, tüm alanları `BP_REQUEST_INFO2` yapısı.

## <a name="remarks"></a>Açıklamalar
Bağımsız değişken olarak geçirilen [GetRequestInfo](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getrequestinfo.md) ve [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) hangi alanları belirlemek için yöntemleri [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) ve [BP_REQUEST_INFO2 ](../../../extensibility/debugger/reference/bp-request-info2.md) yapıları, başlatılacak.

Bu bayraklar Ayrıca hangi alanları göstermek için kullanılan `BP_REQUEST_INFO` ve `BP_REQUEST_INFO2` yapıları, kullanılan ve geçerli her yapı döndürüldüğünde.

Bu değerler, bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetRequestInfo](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getrequestinfo.md)
- [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)
- [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)
