---
title: IDebugBreakpointRequest2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugBreakpointRequest2
helpviewer_keywords:
- IDebugBreakpointRequest2 interface
ms.assetid: 01ac4013-96f9-4235-b289-f55f9e99558f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e61b89fb889a2e274c482e083610b97a19f57f5c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55001991"
---
# <a name="idebugbreakpointrequest2"></a>IDebugBreakpointRequest2
Bu arabirim, oluşturma ve herhangi bir türde kesme noktası bağlama için gereken bilgileri temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugBreakpointRequest2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Oturum hata ayıklama Yöneticisi (SDM), genellikle bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Hata ayıklama altyapısı (DE) Bu arabirim yapılan bir çağrıyla alır [CreatePendingBreakpoint](../../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md) bir bekleyen kesme noktası oluşturmak için. Bir çağrı [GetBreakpointRequest](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-getbreakpointrequest.md) bu arabirimi DE alabilirsiniz.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugBreakpointRequest2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetLocationType](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getlocationtype.md)|Bu kesme noktası istek kesme noktası konumu türünü alır.|  
|[GetRequestInfo](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getrequestinfo.md)|Bu kesme noktası istek tanımlayan kesme noktası isteği bilgilerini alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Sonra program ayıklanan yüklendi, çağrı [bağlama](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md) program istenen konuma bir bekleyen kesme noktasının bağlar.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [CreatePendingBreakpoint](../../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md)   
 [GetBreakpointRequest](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-getbreakpointrequest.md)   
 [Bind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)