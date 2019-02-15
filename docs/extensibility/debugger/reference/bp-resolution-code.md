---
title: BP_RESOLUTION_CODE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BP_RESOLUTION_CODE
helpviewer_keywords:
- BP_RESOLUTION_CODE structure
ms.assetid: ac103ec5-771c-4667-92de-b5abb53bbb52
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b792d8b113cf19fbc7f9bf3efb45963c447df564
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318478"
---
# <a name="bpresolutioncode"></a>BP_RESOLUTION_CODE
Bir kod kesme noktası konumu açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_RESOLUTION_CODE {
    IDebugCodeContext2* pCodeContext;
} BP_RESOLUTION_CODE;
```

```csharp
public struct BP_RESOLUTION_CODE {
    public IDebugCodeContext2 pCodeContext;
};
```

## <a name="members"></a>Üyeler
`pCodeContext`  
[IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) kod kesme noktası konumunu tanımlayan nesne.

## <a name="remarks"></a>Açıklamalar
Bu yapı üyesidir [BP_RESOLUTION_LOCATION](../../../extensibility/debugger/reference/bp-resolution-location.md) üyesi kapatma yapısını [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md) yapısı tarafından döndürülen [GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2-getresolutioninfo.md)yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[BP_RESOLUTION_LOCATION](../../../extensibility/debugger/reference/bp-resolution-location.md)  
[BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md)  
[GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2-getresolutioninfo.md)  
[IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)
