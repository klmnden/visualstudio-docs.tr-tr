---
title: IDebugThread2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugThread2
helpviewer_keywords:
- IDebugThread2 interface
ms.assetid: 221b4b1b-4a26-466e-bc29-5eff800fab13
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: df63bc6484905249adc1756ce701b3ee91f45015
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66319974"
---
# <a name="idebugthread2"></a>IDebugThread2
Bu arabirim bir programda çalıştıran bir iş parçacığını temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugThread2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE), tek bir programda yürütme iş parçacığı temsil etmek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrı [GetThread](../../../extensibility/debugger/reference/idebugstackframe2-getthread.md) şu anda etkin iş parçacığı temsil eden bu arabirimi elde edilir.

 Bu arabirim, ayrıca bir kesme noktası istek oluşturulurken kullanılır (bkz [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)).

 Bu arabirim, ayrıca bağlı veya hata bir kesme noktası çözülürken döndürülür (bkz [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md) ve [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md)).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugThread2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)|Bu iş parçacığı için yığın çerçevesi bir listesini alır.|
|[GetName](../../../extensibility/debugger/reference/idebugthread2-getname.md)|İş parçacığının adını alır.|
|[SetThreadName](../../../extensibility/debugger/reference/idebugthread2-setthreadname.md)|İş parçacığının adını ayarlar.|
|[GetProgram](../../../extensibility/debugger/reference/idebugthread2-getprogram.md)|Bir iş parçacığı çalıştığı program alır.|
|[CanSetNextStatement](../../../extensibility/debugger/reference/idebugthread2-cansetnextstatement.md)|Sonraki deyimi belirli bir yığın çerçevesi ve kod bağlamına ayarlayıp ayarlayamayacağını belirler.|
|[SetNextStatement](../../../extensibility/debugger/reference/idebugthread2-setnextstatement.md)|Sonraki deyimi belirli bir yığın çerçevesi ve kod bağlamı ayarlar.|
|[GetThreadId](../../../extensibility/debugger/reference/idebugthread2-getthreadid.md)|Sistem iş parçacığı tanımlayıcısını alır.|
|[Suspend](../../../extensibility/debugger/reference/idebugthread2-suspend.md)|Bir iş parçacığını askıya alır.|
|[Resume](../../../extensibility/debugger/reference/idebugthread2-resume.md)|Bir iş parçacığını sürdürür.|
|[GetThreadProperties](../../../extensibility/debugger/reference/idebugthread2-getthreadproperties.md)|Bir iş parçacığı tanımlayan özellikleri alır.|
|[GetLogicalThread](../../../extensibility/debugger/reference/idebugthread2-getlogicalthread.md)|Bu fiziksel iş parçacığıyla ilişkilendirilmiş mantıksal iş parçacığı alır.|

## <a name="remarks"></a>Açıklamalar
 Birden çok programlarda, birden fazla fiziksel tek bir iş parçacığı çalıştırılabildiği `IDebugThread2` birden fazla programından aynı fiziksel iş parçacığını temsil edebilir.

 Bir kesme noktası veya özel durum oluştuğunda bir olay çağırarak gönderilen [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md). Bu yöntemin bağımsız değişkenlerden biri olan bir `IDebugThread2` geçerli iş parçacığını temsil eden arabirim. [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md) elde etmek için kullanılan [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md) geçerli yığın çerçevesi için arabirim.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)
- [GetThread](../../../extensibility/debugger/reference/idebugstackframe2-getthread.md)
- [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)
- [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md)
- [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md)