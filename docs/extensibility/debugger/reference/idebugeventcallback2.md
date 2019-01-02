---
title: IDebugEventCallback2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugEventCallback2
helpviewer_keywords:
- IDebugEventCallback2
ms.assetid: 2c935ee0-2e22-4be0-a852-73736f33c8c9
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: ce30279cb58704ab712245ad69bcda197d0e7fc3
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53852764"
---
# <a name="idebugeventcallback2"></a>IDebugEventCallback2
Bu arabirim, hata ayıklama altyapısı (DE) oturum hata ayıklama Yöneticisi (SDM) hata ayıklama olayları göndermek için kullanılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugEventCallback2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] bir hata ayıklama altyapısı olaylarını almak için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 SDM çağırdığında bir hata ayıklama altyapısı genellikle bu arabirimin aldığı [iliştirme](../../../extensibility/debugger/reference/idebugprogram2-attach.md), [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md), veya [LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md). Hata ayıklama altyapısı, çağırarak SDM için olaylar gönderir [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md).  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugEventCallback2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)|SDM olaylarına hata ayıklama bildirim gönderir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Ancak [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) ve [EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) , aldıkları belirtin bir `IDebugEventCallback2` arabirim, bu durumda değildir ve arabirim işaretçisi, null değeri her zaman olur. Bunun yerine, hata ayıklama altyapısı kullanmalısınız `IDebugEventCallback2` çağrısında alınan arabirimi [iliştirme](../../../extensibility/debugger/reference/idebugprogram2-attach.md), [Ekle](../../../extensibility/debugger/reference/idebugengine2-attach.md), veya [LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md).  
  
 Bir paket uyguluyorsa [IDebugEventCallback](../../../extensibility/debugger/reference/idebugeventcallback2.md) yönetilen kodda kesinlikle önerilir, <xref:System.Runtime.InteropServices.Marshal.ReleaseComObject%2A> çağrılabilir geçirilen çeşitli arabirimlerindeki [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md).  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md)   
 [Ekleme](../../../extensibility/debugger/reference/idebugprogram2-attach.md)   
 [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)