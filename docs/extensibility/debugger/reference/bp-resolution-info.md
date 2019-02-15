---
title: BP_RESOLUTION_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BP_RESOLUTION_INFO
helpviewer_keywords:
- BP_RESOLUTION_INFO structure
ms.assetid: ba0c162a-61e8-4a0b-811f-4c1d8a5d82f0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a02eb1407bf9645fd8a1ff3f56c971a24a94417d
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318205"
---
# <a name="bpresolutioninfo"></a>BP_RESOLUTION_INFO
Bir kod kesme noktası ya da veri kesme noktası bağlı Kesme noktasının bilgiler açıklanmaktadır.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_RESOLUTION_INFO {
    BPRESI_FIELDS          dwFields;
    BP_RESOLUTION_LOCATION bpResLocation;
    IDebugProgram2*        pProgram;
    IDebugThread2*         pThread;
} BP_RESOLUTION_INFO;
```

```csharp
public struct BP_RESOLUTION_INFO {
    public uint                   dwFields;
    public BP_RESOLUTION_LOCATION bpResLocation;
    public IDebugProgram2         pProgram;
    public IDebugThread2          pThread;
};
```

## <a name="members"></a>Üyeler
`dwFields`  
Bayrakları koleksiyonunu [BPRESI_FIELDS](../../../extensibility/debugger/reference/bpresi-fields.md) hangi alanların belirten numaralandırma doldurulur.

`bpResLocation`  
[BP_RESOLUTION_LOCATION](../../../extensibility/debugger/reference/bp-resolution-location.md) yapısı, kod veya veri kesme noktası konumunu belirtir.

`pProgram`  
[IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) kesme noktası hatanın gerçekleştiği uygulama temsil eden nesne.

`pThread`  
[IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) kesme Notası hatası içeren uygulamanın çalıştığı iş parçacığını temsil eden nesne.

## <a name="remarks"></a>Açıklamalar
Bu yapı tarafından döndürülen [GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2-getresolutioninfo.md).

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2-getresolutioninfo.md)  
[BPRESI_FIELDS](../../../extensibility/debugger/reference/bpresi-fields.md)  
[BP_RESOLUTION_LOCATION](../../../extensibility/debugger/reference/bp-resolution-location.md)  
[IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)  
[IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
