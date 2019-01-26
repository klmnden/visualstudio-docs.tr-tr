---
title: IDebugOutputStringEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugOutputStringEvent2
helpviewer_keywords:
- IDebugOutputStringEvent2 interface
ms.assetid: 86596fd1-cecc-4813-8add-dc3d70068f9b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3e7f13d75090e2b1a8e0fc22bc1640943e32785c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54971838"
---
# <a name="idebugoutputstringevent2"></a>IDebugOutputStringEvent2
Bu arabirim hata ayıklama altyapısı (DE) tarafından bir dize çıktısı için oturum hata ayıklama Yöneticisi (SDM) gönderilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugOutputStringEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 DE bir dizeye göndermek için bu arabirimi uygulayan **çıkış** IDE bir pencerenin. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 KODU oluşturur ve bu olay göndermek için bir dize nesnesine gönderir **çıkış** penceresi. Olay kullanılarak gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemini aşağıdaki tabloda gösterilmektedir `IDebugOutputStringEvent2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetString](../../../extensibility/debugger/reference/idebugoutputstringevent2-getstring.md)|Annotatable iletisini alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Örneğin, bir dize için Win32 hata ayıklanan programa gönderdiğinde yönetilmeyen kodda çıkış dize gönderilebilir `OutputDebugString` işlevi. Bu dize DE tarafından kesildi ve SDM gönderilen `IDebugOutputStringEvent2` olay.  
  
 Kullanım [IDebugMessageEvent2](../../../extensibility/debugger/reference/idebugmessageevent2.md) kullanıcı yanıt isteyen bir ileti göndermek için.  
  
 Kullanım [IDebugErrorEvent2](../../../extensibility/debugger/reference/idebugerrorevent2.md) yanıt gerektirmeyen bir hata iletisi göndermek için.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugMessageEvent2](../../../extensibility/debugger/reference/idebugmessageevent2.md)   
 [IDebugErrorEvent2](../../../extensibility/debugger/reference/idebugerrorevent2.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)