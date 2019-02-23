---
title: BP_ERROR_RESOLUTION_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_ERROR_RESOLUTION_INFO
helpviewer_keywords:
- BP_ERROR_RESOLUTION_INFO structure
ms.assetid: a6b83242-5728-4716-80f3-840c96d59c6c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7d89a871abf6a62dec712ce9d9ae486496c775b8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56691208"
---
# <a name="bperrorresolutioninfo"></a>BP_ERROR_RESOLUTION_INFO
Konum, program ve iş parçacığı gibi bir hata kesme noktası çözünürlüğü açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_ERROR_RESOLUTION_INFO {
    BPERESI_FIELDS         dwFields;
    BP_RESOLUTION_LOCATION bpResLocation;
    IDebugProgram2*        pProgram;
    IDebugThread2*         pThread;
    BSTR                   bstrMessage;
    BP_ERROR_TYPE          dwType;
} BP_ERROR_RESOLUTION_INFO;
```

```csharp
public struct BP_ERROR_RESOLUTION_INFO {
    public uint                   dwFields;
    public BP_RESOLUTION_LOCATION bpResLocation;
    public IDebugProgram2         pProgram;
    public IDebugThread2          pThread;
    public string                 bstrMessage;
    public uint                   dwType;
};
```

## <a name="members"></a>Üyeler
`dwFields` Değerleri birleşimi [BPERESI_FIELDS](../../../extensibility/debugger/reference/bperesi-fields.md) bu yapının alanları doldurulmalıdır belirten sabit listesi.

`bpResLocation` [BP_RESOLUTION_LOCATION](../../../extensibility/debugger/reference/bp-resolution-location.md) UNION, kesme noktası çözünürlüğü konumu belirtir.

`pProgram` [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) kesme noktası hatanın gerçekleştiği uygulama temsil eden nesne.

`pThread` [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) kesme Notası hatası oluşturulan uygulama çalışan iş parçacığı temsil eden nesne.

`bstrMessage` Bu hata resolution kaynaklanan uyarı veya hata iletisi içeren bir dize.

`dwType` Bir değer [BP_ERROR_TYPE](../../../extensibility/debugger/reference/bp-error-type.md) kesme noktası hata türünü belirten sabit listesi.

## <a name="remarks"></a>Açıklamalar
Bu yapı döndürüldüğü [GetResolutionInfo](../../../extensibility/debugger/reference/idebugerrorbreakpointresolution2-getresolutioninfo.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [GetResolutionInfo](../../../extensibility/debugger/reference/idebugerrorbreakpointresolution2-getresolutioninfo.md)
- [BPRESI_FIELDS](../../../extensibility/debugger/reference/bpresi-fields.md)
- [BP_RESOLUTION_LOCATION](../../../extensibility/debugger/reference/bp-resolution-location.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [BP_ERROR_TYPE](../../../extensibility/debugger/reference/bp-error-type.md)
