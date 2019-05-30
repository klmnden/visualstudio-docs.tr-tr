---
title: BP_REQUEST_INFO2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_REQUEST_INFO2
helpviewer_keywords:
- BP_REQUEST_INFO2 structure
ms.assetid: 008c87f7-a76e-43d3-8904-11b225d6a9a5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 8f9c601cf1620d002bd86b8bc110d28bdb533e61
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66352954"
---
# <a name="bprequestinfo2"></a>BP_REQUEST_INFO2
Satıcı GUID, kısıtlama ve İzleme noktası gibi bir kesme noktası uygulamak için gereken bilgileri içerir.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_REQUEST_INFO2 {
    BPREQI_FIELDS   dwFields;
    GUID            guidLanguage;
    BP_LOCATION     bpLocation;
    IDebugProgram2* pProgram;
    BSTR            bstrProgramName;
    IDebugThread2*  pThread;
    BSTR            bstrThreadName;
    BP_CONDITION    bpCondition;
    BP_PASSCOUNT    bpPassCount;
    BP_FLAGS        dwFlags;
    GUID            guidVendor;
    BSTR            bstrConstraint;
    BSTR            bstrTracepoint;
} BP_REQUEST_INFO2;
```

```csharp
public struct BP_REQUEST_INFO2 {
    public uint           dwFields;
    public Guid           guidLanguage;
    public BP_LOCATION    bpLocation;
    public IDebugProgram2 pProgram;
    public string         bstrProgramName;
    public IDebugThread2  pThread;
    public string         bstrThreadName;
    public BP_CONDITION   bpCondition;
    public BP_PASSCOUNT   bpPassCount;
    public uint           dwFlags;
    public Guid           guidVendor;
    public string         bstrConstraint;
    public string         bstrTracepoint;
};
```

## <a name="members"></a>Üyeler
`dwFields`\
Bayraklarının bir birleşimi [BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md) hangi alanların doldurulmuş belirten sabit listesi.

`guidLanguage`\
Dil GUID.

`bpLocation`\
[BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) yapısı kesme noktası konumu türünü belirtir.

`pProgram`\
[IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) kesme noktası oluştuğu uygulamanın temsil eden nesne.

`bstrProgramName`\
Kesme noktası oluştuğu uygulamanın adı.

`pThread`\
[IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) kesme noktası oluştuğu iş parçacığını temsil eden nesne.

`bstrThreadName`\
Kesme noktası oluştuğu iş parçacığı adı.

`bpCondition`\
[BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md) yapısı altında kesme noktası yangın koşullar açıklanmaktadır.

`bpPassCount`\
[BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md) kesme noktası geçişi sayısı bilgilerini içeren yapısı.

`dwFlags`\
Bayraklarının bir birleşimi [BP_FLAGS](../../../extensibility/debugger/reference/bp-flags.md) istenen kesme noktası için bayrakları belirten sabit listesi.

`guidVendor`\
Satıcı GUİD'si. Null değeri olabilir.

`bstrConstraint`\
Kesme noktası kısıtlama adı. Null değeri olabilir.

`bstrTracepoint`\
İzleme noktası adı. Null değeri olabilir.

## <a name="remarks"></a>Açıklamalar
Bu yapı tarafından döndürülen [GetRequestInfo2](../../../extensibility/debugger/reference/idebugbreakpointrequest3-getrequestinfo2.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [GetRequestInfo2](../../../extensibility/debugger/reference/idebugbreakpointrequest3-getrequestinfo2.md)
- [BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md)
- [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)
- [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)
- [BP_FLAGS](../../../extensibility/debugger/reference/bp-flags.md)
