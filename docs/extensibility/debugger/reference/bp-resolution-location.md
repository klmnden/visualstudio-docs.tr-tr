---
title: BP_RESOLUTION_LOCATION | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_RESOLUTION_LOCATION
helpviewer_keywords:
- BP_RESOLUTION_LOCATION structure
ms.assetid: 21dc5246-69c1-43e3-855c-9cd4e596c0e6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d6de035568e1c2aebe853d25dc5f769d233da819
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62888987"
---
# <a name="bpresolutionlocation"></a>BP_RESOLUTION_LOCATION
Kesme noktası çözünürlüğü konumu yapısını belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
struct _BP_RESOLUTION_LOCATION {
    BP_TYPE bpType;
    union {
        BP_RESOLUTION_CODE bpresCode;
        BP_RESOLUTION_DATA bpresData;
        int                unused;
    } bpResLocation;
} BP_RESOLUTION_LOCATION;
```

```csharp
public struct BP_RESOLUTION_LOCATION {
    public uint   bpType;
    public IntPtr unionmember1;
    public IntPtr unionmember2;
    public IntPtr unionmember3;
    public uint   unionmember4;
};
```

## <a name="members"></a>Üyeler
`bpType` Bir değer [BP_TYPE](../../../extensibility/debugger/reference/bp-type.md) yorumlama belirten numaralandırma `bpResLocation` birleşim veya `unionmemberX` üyeleri.

`bpResLocation.bpresCode`

 [C++ yalnızca] İçeren [BP_RESOLUTION_CODE](../../../extensibility/debugger/reference/bp-resolution-code.md) , yapı `bpType`  =  `BPT_CODE`.

`bpResLocation.bpresData`

 [C++ yalnızca] İçeren [BP_RESOLUTION_DATA](../../../extensibility/debugger/reference/bp-resolution-data.md) , yapı `bpType`  =  `BPT_DATA`.

`bpResLocation.unused`

 [C++ yalnızca] Bir yer tutucu.

`unionmember1`

 [C# yalnızca] Yorumlama konusunda açıklamalara bakın.

`unionmember2`

 [C# yalnızca] Yorumlama konusunda açıklamalara bakın.

`unionmember3`

 [C# yalnızca] Yorumlama konusunda açıklamalara bakın.

`unionmember4`

 [C# yalnızca] Yorumlama konusunda açıklamalara bakın.

## <a name="remarks"></a>Açıklamalar
Bu yapı üyesidir [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md) ve [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md) yapıları.

 [C# yalnızca] `unionmemberX` Üyeleri aşağıdaki tabloya göre yorumlanır. Sol sütundaki için konum `bpType` boyunca hangi her belirlemek için değer `unionmemberX` üye temsil eder ve sıralama `unionmemberX` uygun şekilde. Bu yapı C# yorumlamak bir yol için örneğe bakın.

|`bpLocationType`|`unionmember1`|`unionmember2`|`unionmember3`|`unionmember4`|
|----------------------|--------------------|--------------------|--------------------|--------------------|
|`BPT_CODE`|[IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)|-|-|-|
|`BPT_DATA`|`string` (veri ifadesi)|`string` (işlev adı)|`string` (görüntü adı)|`enum_BP_RES_DATA_FLAGS`|

## <a name="example"></a>Örnek
Bu örnek nasıl yorumlanacağını gösterir `BP_RESOLUTION_LOCATION` C# yapısı.

```csharp
using System;
using System.Runtime.Interop.Services;
using Microsoft.VisualStudio.Debugger.Interop;

namespace MyPackage
{
    public class MyClass
    {
        public void Interpret(BP_RESOLUTION_LOCATION bprl)
        {
            if (bprl.bpType == (uint)enum_BP_TYPE.BPT_CODE)
            {
                IDebugCodeContext2 pContext = (IDebugCodeContext2)Marshal.GetObjectForIUnknown(bp.unionmember1);
            }
            else if (bprl.bpType == (uint)enum_BP_TYPE.BPT_DATA)
            {
                string dataExpression = Marshal.PtrToStringBSTR(bp.unionmember3);
                string functionName = Marshal.PtrToStringBSTR(bp.unionmember2);
                string imageName = Marshal.PtrToStringBSTR(bp.unionmember3);
                enum_BP_RES_DATA_FLAGS numElements = (enum_BP_RES_DATA_FLAGS)bp.unionmember4;
            }
        }
    }
}
```

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [BP_TYPE](../../../extensibility/debugger/reference/bp-type.md)
- [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md)
- [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md)
- [BP_RESOLUTION_CODE](../../../extensibility/debugger/reference/bp-resolution-code.md)
- [BP_RESOLUTION_DATA](../../../extensibility/debugger/reference/bp-resolution-data.md)
- [BP_RES_DATA_FLAGS](../../../extensibility/debugger/reference/bp-res-data-flags.md)
