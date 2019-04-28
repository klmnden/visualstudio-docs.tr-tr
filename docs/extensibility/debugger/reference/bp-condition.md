---
title: BP_CONDITION | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_CONDITION
helpviewer_keywords:
- BP_CONDITION structure
ms.assetid: 407f87a3-2878-429b-8c65-b68feb36622a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9c37699e965698b4f5700bc1994ba25c8c0bbbd5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62889139"
---
# <a name="bpcondition"></a>BP_CONDITION
Altında bir kesme noktası harekete koşullar açıklanmaktadır.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_CONDITION {
    IDebugThread2* pThread;
    BP_COND_STYLE  styleCondition;
    BSTR           bstrContext;
    BSTR           bstrCondition;
    UINT           nRadix;
} BP_CONDITION;
```

```csharp
public struct BP_CONDITION {
    public IDebugThread2 pThread;
    public uint          styleCondition;
    public string        bstrContext;
    public string        bstrCondition;
    public uint          nRadix;
};
```

## <a name="members"></a>Üyeler
`pThread` [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) etkin iş parçacığı için kesme noktasını içeren uygulamayı temsil eden nesne.

`styleCondition` Bir değer [BP_COND_STYLE](../../../extensibility/debugger/reference/bp-cond-style.md) bu kesme noktası koşulu stilini açıklayan sabit listesi.

`bstrContext` Kesme noktası konumu.

`bstrCondition` Kesme noktası tetikleyicisinin tetikleme koşulunu.

`nRadix` Sayısal yedeklenmesine değerlendirmede kullanılacak sayı tabanı.

## <a name="remarks"></a>Açıklamalar
Bu yapı üyesidir [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) ve [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) yapıları.

Bu yapı ayrıca bir parametre olarak geçirilen [SetCondition](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setcondition.md) ve [SetCondition](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-setcondition.md) yöntemleri.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)
- [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)
- [SetCondition](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setcondition.md)
- [SetCondition](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-setcondition.md)
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [BP_COND_STYLE](../../../extensibility/debugger/reference/bp-cond-style.md)
