---
title: IDebugCanStopEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCanStopEvent2
helpviewer_keywords:
- IDebugBreakpointRequest2 interface
ms.assetid: 784bd5b1-4a3f-4455-b313-c4c9a82555a5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 012440e03208fab6bc2cde8814781f7b3a64f79d
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56682108"
---
# <a name="idebugcanstopevent2"></a>IDebugCanStopEvent2
Bu arabirim, geçerli kod konumda durdurmak mi oturum hata ayıklama Yöneticisi (SDM) istemek için kullanılır.

## <a name="syntax"></a>Sözdizimi

```
IDebugCanStopEvent2 : IUknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE) kaynak kod içerisinde ilerlemeye desteklemek için bu arabirimi uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde (SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi).

 Bu arabirim uygulamasını SDM'ın çağrısı iletişim kurması gereken [CanStop](../../../extensibility/debugger/reference/idebugcanstopevent2-canstop.md) hata ayıklama altyapısı. Örneğin, bu işleme iş parçacığı hata ayıklama altyapısının ileti gönderen bir ileti ile yapılabilir veya bu arabirimi uygulayan nesnenin bir başvuru için hata ayıklama altyapısı tutun ve geri yöntemlere geçirilen bayrağı ile hata ayıklama motorunda arama `IDebugCanStopEvent2::CanStop`.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu yöntem DE, yürütme ve DE devam etmek için sorulan her zaman kod içerisinde ilerlemeye DE gönderebilirsiniz. Bu olay ile gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugCanStopEvent2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)|Bu olay nedenini alır.|
|[CanStop](../../../extensibility/debugger/reference/idebugcanstopevent2-canstop.md)|Hata ayıklanan programa veya bu olay (ve durdurma nedenini açıklayan bir olayı gönderme) konumunda Durdur yalnızca yürütme devam belirtir.|
|[GetDocumentContext](../../../extensibility/debugger/reference/idebugcanstopevent2-getdocumentcontext.md)|Bu olay konumunu tanımlayan belge bağlamını alır.|
|[GetCodeContext](../../../extensibility/debugger/reference/idebugcanstopevent2-getcodecontext.md)|Bu olay konumunu tanımlayan kod bağlamı alır.|

## <a name="remarks"></a>Açıklamalar
 Bir işlev ve DE kullanıcı adımlarına bulur hiçbir hata ayıklama bilgisi yok veya hata ayıklama bilgisi var, ancak DE o konumda görüntülenebilen kaynak kodu bilemez, bu arabirim DE gönderir.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugStepCompleteEvent2](../../../extensibility/debugger/reference/idebugstepcompleteevent2.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)