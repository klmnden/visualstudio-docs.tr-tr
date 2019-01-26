---
title: IDebugBoundBreakpoint2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugBoundBreakpoint2
helpviewer_keywords:
- IDebugBoundBreakpoint2 interface
ms.assetid: df33c52e-ded2-48a0-951d-1f36c8fc922e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d4c3cd8915b74560d1e42125997f9f61240430ed
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54931667"
---
# <a name="idebugboundbreakpoint2"></a>IDebugBoundBreakpoint2
Bu arabirim, bir kod konuma bağlı bir kesme noktasını temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugBoundBreakpoint2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE), kesme noktaları desteğini bir parçası olarak bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bir çağrı [bağlama](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md) bu arabirim oluşturur. Çağrılar [GetBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getbreakpoint.md) ve [sonraki](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-next.md) bu arabirim de edinebilirsiniz.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugBoundBreakpoint2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getpendingbreakpoint.md)|Belirtilen bağlı Kesme noktasının oluşturulduğu bekleyen kesme noktasının alır.|  
|[GetState](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getstate.md)|Bu bağlı Kesme noktasının durumunu alır.|  
|[GetHitCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-gethitcount.md)|Bu bağlı kesme noktası için geçerli isabet sayısını alır.|  
|[GetBreakpointResolution](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getbreakpointresolution.md)|Bu Kesme noktasının açıklayan bir kesme noktası çözünürlüğü alır.|  
|[Enable](../../../extensibility/debugger/reference/idebugboundbreakpoint2-enable.md)|Etkinleştirir veya kesme noktasını devre dışı bırakır.|  
|[SetHitCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-sethitcount.md)|Bu bağlı kesme noktası isabet sayısını ayarlar.|  
|[SetCondition](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setcondition.md)|Bu bağlı Kesme noktasının ile ilişkilendirilmiş olan koşul değiştirir veya ayarlar.|  
|[SetPassCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setpasscount.md)|Veya pass sayısı bu bağlı Kesme noktasının ile ilişkili değişiklik kümeleri.|  
|[Delete](../../../extensibility/debugger/reference/idebugboundbreakpoint2-delete.md)|Kesme noktasını siler.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [GetBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getbreakpoint.md)   
 [Sonraki](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-next.md)   
 [Bind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)