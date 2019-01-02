---
title: IDebugProcess2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcess2
helpviewer_keywords:
- IDebugProcess2 interface
ms.assetid: 99f6cd06-4076-45ee-b2ae-fa2ad627fd18
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d2a17c5c9f4121725ebfb9ca5a01f6209408c9a1
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53879802"
---
# <a name="idebugprocess2"></a>IDebugProcess2
Bu arabirim bir bağlantı noktası üzerinde çalışan bir işlemi temsil eder. Yerel bağlantı noktası, bağlantı noktası ise, `IDebugProcess2` genellikle yerel makinedeki fiziksel bir işlemi temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProcess2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirim, programlar, grup olarak yönetmek için özel bağlantı noktası sağlayıcısı tarafından uygulanır. Bu arabirim bağlantı sağlayıcı tarafından uygulanmalıdır.  
  
 Hata ayıklama altyapısı aracılığıyla bir programın tanıtımından destekliyorsa, ayrıca bu arabirimi uygulayan [LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md).  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim, bu işlemde tanıtılan programlar bir grup ile etkileşim kurmak için öncelikle oturum hata ayıklama Yöneticisi tarafından (SDM) adı verilir.  
  
 Çağrı [GetProcess](../../../extensibility/debugger/reference/idebugprogram2-getprocess.md) veya [GetProcess](../../../extensibility/debugger/reference/idebugport2-getprocess.md) bu arabirimi alınamıyor. Bu arabirim, ayrıca çağırarak döndürülür `IDebugEngineLaunch2::LaunchSuspended`.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProcess2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md)|İşlemin bir açıklamasını alır.|  
|[EnumPrograms](../../../extensibility/debugger/reference/idebugprocess2-enumprograms.md)|Bu işlemde yer alan program numaralandırır.|  
|[GetName](../../../extensibility/debugger/reference/idebugprocess2-getname.md)|Başlık, kolay ad veya işlemin dosya adını alır.|  
|[GetServer](../../../extensibility/debugger/reference/idebugprocess2-getserver.md)|Bu işlem üzerinde çalıştığı bir makine sunucusu örneğini alır.|  
|[Terminate](../../../extensibility/debugger/reference/idebugprocess2-terminate.md)|İşlemi sonlandırır.|  
|[Attach](../../../extensibility/debugger/reference/idebugprocess2-attach.md)|İşlemine ekler.|  
|[CanDetach](../../../extensibility/debugger/reference/idebugprocess2-candetach.md)|SDM bir işlem ayırabilirsiniz belirler.|  
|[Detach](../../../extensibility/debugger/reference/idebugprocess2-detach.md)|Hata ayıklayıcı işlemden ayırır.|  
|[GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md)|Sistem işlemi tanımlayıcısını alır.|  
|[GetProcessId](../../../extensibility/debugger/reference/idebugprocess2-getprocessid.md)|Bu işlem için bir genel benzersiz tanımlayıcısını alır.|  
|[GetAttachedSessionName](../../../extensibility/debugger/reference/idebugprocess2-getattachedsessionname.md)<br /><br /> [KULLANIM DIŞI]|İşlem hata ayıklama oturumu adını alır.<br /><br /> [KULLANIM DIŞI. GEREKEN HER ZAMAN DÖNÜŞ `E_NOTIMPL`.]|  
|[EnumThreads](../../../extensibility/debugger/reference/idebugprocess2-enumthreads.md)|İşlemde çalışan iş parçacıklarının numaralandırır.|  
|[CauseBreak](../../../extensibility/debugger/reference/idebugprocess2-causebreak.md)|Bu işlem durdurma kodu çalıştıran sonraki program isteklerine.|  
|[GetPort](../../../extensibility/debugger/reference/idebugprocess2-getport.md)|Bu işlemin çalıştığı bağlantı noktasını alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir `IDebugProcess2` birini veya daha fazlasını içeren [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) arabirimleri.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [GetProcess](../../../extensibility/debugger/reference/idebugport2-getprocess.md)   
 [LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md)   
 [GetProcess](../../../extensibility/debugger/reference/idebugprogram2-getprocess.md)   
 [Sonraki](../../../extensibility/debugger/reference/ienumdebugprocesses2-next.md)   
 [Olay](../../../extensibility/debugger/reference/idebugportevents2-event.md)   
 [IDebugEngineLaunch2](../../../extensibility/debugger/reference/idebugenginelaunch2.md)   
 [Olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)