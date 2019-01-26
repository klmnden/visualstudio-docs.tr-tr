---
title: IDebugExceptionEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugExceptionEvent2
helpviewer_keywords:
- IDebugExceptionEvent2 interface
ms.assetid: 53d32e59-a84b-4710-833e-c5ab08100516
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1ac5c3aceb9519d66c185f78bdde37861467ecdf
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54983880"
---
# <a name="idebugexceptionevent2"></a>IDebugExceptionEvent2
Programın şu anda yürütülmekte olan bir özel durum oluştuğunda hata ayıklama altyapısı (DE) Bu arabirim oturum hata ayıklama Yöneticisi (SDM) gönderir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugExceptionEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirim için bir özel durum hata ayıklaması yapılan programa oluştu rapor DE uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 KODU oluşturur ve bu olay bir özel durum rapor nesnesine gönderir. Olay kullanılarak gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugExceptionEvent2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md)|Bu olay harekete geçirilen özel durum hakkında ayrıntılı bilgiler alır.|  
|[GetExceptionDescription](../../../extensibility/debugger/reference/idebugexceptionevent2-getexceptiondescription.md)|Bu olay harekete geçirilen özel durum için okunabilir bir açıklamasını alır.|  
|[CanPassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md)|Hata ayıklama altyapısı (DE) yürütme devam ettiğinde ayıklanan programa bu özel durum geçirme seçeneğiniz destekleyip desteklemediğini belirler.|  
|[PassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-passtodebuggee.md)|Özel durum yürütme devam ettiğinde ayıklanan programa geçirilmelidir olup olmadığını ya da özel durum atılmalı belirtir.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="remarks"></a>Açıklamalar  
 Bu özel durum olayı bir ilk şans veya ikinci şans özel durum için bir çağrı tarafından belirlendiyse, görmek için DE denetler olay göndermeden önce [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md). İlk fırsat özel durum olarak belirlendiyse `IDebugExceptionEvent2` olay SDM için gönderilir. Değilse DE uygulamaya özel durumu işlemek üzere bir fırsat sunar. Hiçbir özel durum işleyicisi sağlanır ve özel durum ikinci şans özel durum belirlendiyse `IDebugExceptionEvent2` olay SDM için gönderilir. Aksi takdirde DE programın yürütülmesini sürdürür ve işletim sistemi ya da çalışma zamanı özel durumu işler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)