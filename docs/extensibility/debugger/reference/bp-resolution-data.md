---
title: BP_RESOLUTION_DATA | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BP_RESOLUTION_DATA
helpviewer_keywords:
- BP_RESOLUTION_DATA structure
ms.assetid: 9e0b9000-6a84-47b9-b07a-367a75764389
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8b2d887c10721693468ed907175399074f890588
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56317269"
---
# <a name="bpresolutiondata"></a>BP_RESOLUTION_DATA
Veri kesme noktası bağlamanın sonucunu açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_RESOLUTION_DATA {
    BSTR              bstrDataExpr;
    BSTR              bstrFunc;
    BSTR              bstrImage;
    BP_RES_DATA_FLAGS dwFlags;
} BP_RESOLUTION_DATA;
```

```csharp
public struct BP_RESOLUTION_DATA {
    public string bstrDataExpr;
    public string bstrFunc;
    public string bstrImage;
    public uint   dwFlags;
};
```

## <a name="members"></a>Üyeler
`bstrDataExpr`  
Bağlı veri ifadesi.

`bstrFunc`  
İşlevin adını veri kesme noktası de (varsa) bağlıdır.

`bstrImage`  
Veri kesme noktası, bağlı (örneğin, MyModule.dll) modülünün adı.

`dwFlags`  
Bir değer [BP_RES_DATA_FLAGS](../../../extensibility/debugger/reference/bp-res-data-flags.md) veri kesme noktası nasıl uygulandığını açıklayan sabit listesi,.

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
