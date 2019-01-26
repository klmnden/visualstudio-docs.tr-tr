---
title: IDebugProgramDestroyEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgramDestroyEvent2
helpviewer_keywords:
- IDebugProgramDestroyEvent2
ms.assetid: ddf127ca-c4a5-4071-90ca-68faf2f57dbd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 986c434ba3797ff71cc16f524caf88b38055a503
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54985425"
---
# <a name="idebugprogramdestroyevent2"></a>IDebugProgramDestroyEvent2
Bir program tamamlanana kadar çalıştırdığınızda bu arabirimi hata ayıklama altyapısı (DE) oturum hata ayıklama Yöneticisi (SDM) gönderilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProgramDestroyEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 DE veya özel bağlantı noktası sağlayıcısı bir program sonlandırıldı ve artık hata ayıklaması için kullanılabilir bir rapor için bu arabirimi uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 DE veya özel bağlantı noktası sağlayıcısı oluşturur ve bu olay bir programın sonlandırılması rapor nesnesine gönderir. Kullanarak DE bu olay gönderen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi. Özel bağlantı noktası sağlayıcısı kullanarak bu olay gönderir [IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md) arabirimi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemini aşağıdaki tabloda gösterilmektedir `IDebugProgramDestroyEvent2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetExitCode](../../../extensibility/debugger/reference/idebugprogramdestroyevent2-getexitcode.md)|Programın çıkış kodunu alır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)