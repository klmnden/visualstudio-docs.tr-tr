---
title: IDebugModule2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugModule2
helpviewer_keywords:
- IDebugModule2 interface
ms.assetid: 24c2a126-f4ab-4891-8509-8ef99b994c08
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4ea20dac16cdffbac24cbca68c1a337a250ea8cc
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54922775"
---
# <a name="idebugmodule2"></a>IDebugModule2
Bu arabirim bir modülü temsil eder — diğer bir deyişle, bir yürütülebilir bir program ölçü — bir DLL gibi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugModule2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE) bir modülü temsil eder ve bu modülle ilgili bilgileri erişim sağlamak için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bir çağrı [GetModule](../../../extensibility/debugger/reference/idebugmoduleloadevent2-getmodule.md) bu arabirimi döndürür. DE gönderir [IDebugModuleLoadEvent2](../../../extensibility/debugger/reference/idebugmoduleloadevent2.md) arabirimini kullanarak oturum hata ayıklama Yöneticisi için (SDM) [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) yöntemi.  
  
 Bu arabirim, ayrıca döndürülebilir bir [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yapısı (bir çağrı tarafından döndürülen [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)).  
  
 [Sonraki](../../../extensibility/debugger/reference/ienumdebugmodules2-next.md) Ayrıca bu arabirim döndürür ([EnumModules](../../../extensibility/debugger/reference/idebugprogram2-enummodules.md) döndürür [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md) arabirimi).  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugModule2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md)|Alır [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) , bu modül açıklar.|  
|[ReloadSymbols_Deprecated](../../../extensibility/debugger/reference/idebugmodule2-reloadsymbols-deprecated.md)|ARTIK KULLANILMIYOR. KULLANMAYIN. Bu modüle ilişkin simgeleri yeniden yükler.|  
  
## <a name="remarks"></a>Açıklamalar  
 Modül bilgilerini görüntülenebilir **modülleri** IDE bir pencerenin.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md)   
 [GetModule](../../../extensibility/debugger/reference/idebugmoduleloadevent2-getmodule.md)   
 [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md)   
 [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md)