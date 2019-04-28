---
title: IDebugPendingBreakpoint2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPendingBreakpoint2
helpviewer_keywords:
- IDebugPendingBreakpoint2 interface
ms.assetid: d416b095-917e-475e-b796-ec0a03ffb8da
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 816fad53554675e7f29cef838d4ea24e154dca8c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62871940"
---
# <a name="idebugpendingbreakpoint2"></a>IDebugPendingBreakpoint2
Bu arabirim, bir kod konuma bağlamak hazır bir kesme noktası temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugPendingBreakpoint2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE), kesme noktaları desteğini bir parçası olarak bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir çağrı [CreatePendingBreakpoint](../../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md) bir bekleyen kesme noktasından oluşturur bir [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md) arabirimi. Bir çağrı [bağlama](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md) oluşturur bir `IDebugBreakpoint2` programı ilişkili bir kesme noktası temsil eden arabirim.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPendingBreakpoint2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[CanBind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-canbind.md)|Bu bekleyen kesme noktasının bir kod konumuna bağlayabilirsiniz olup olmadığını belirler.|
|[Bind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)|Bu bekleyen kesme noktasının bir veya daha fazla kod konumlara bağlar.|
|[GetState](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-getstate.md)|Bekleyen kesme noktası bu durumu alır.|
|[GetBreakpointRequest](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-getbreakpointrequest.md)|Bu bekleyen kesme noktası oluşturmak için kullanılan bir kesme noktası istek alır.|
|[Virtualize](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-virtualize.md)|Bu sanallaştırılmış bekleyen kesme noktasının durumunu değiştirir.|
|[Enable](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enable.md)|Bu etkin bekleyen kesme noktasının durumunu değiştirir.|
|[SetCondition](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-setcondition.md)|Bu kesme noktası ilişkilendirilmiş olan koşul değiştirir veya ayarlar.|
|[SetPassCount](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-setpasscount.md)|Bu kesme noktası ilişkili parola sayısı değiştirir veya ayarlar.|
|[EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md)|Bu bekleyen kesme noktasından bağlı tüm kesme noktalarını numaralandırır.|
|[EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md)|Bu bekleyen kesme noktasından sonuçlanan tüm hata kesme noktalarını numaralandırır.|
|[Delete](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-delete.md)|Bu bekleyen kesme noktasının ve ondan bağlı tüm kesme noktalarını siler.|

## <a name="remarks"></a>Açıklamalar
 `IDebugPendingBreakpoint2` bir kesme noktası için bir veya daha çok programlar uygulanabilir kodu bağlamak için gereken tüm gerekli bilgileri sağlayıcısı olarak düşünülebilir.

 Bir bekleyen kesme noktasının potansiyel olarak birden fazla bağlı Kesme noktasının üretebilir. Örneğin, bir kesme noktası C++ stili şablonunda, şablon benzersiz her örneği için ilişkili bir kesme noktası üretebilir.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [CreatePendingBreakpoint](../../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md)
- [GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointboundevent2-getpendingbreakpoint.md)
- [GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getpendingbreakpoint.md)
- [GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugerrorbreakpoint2-getpendingbreakpoint.md)