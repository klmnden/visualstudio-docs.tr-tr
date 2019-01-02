---
title: IDebugMessageEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugMessageEvent2
helpviewer_keywords:
- IDebugMessageEvent2 interface
ms.assetid: a9ff3d00-e9ac-4cd6-bda9-584a4815aff8
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 62ead34f06d474875539ebd4e274cfcd51db4e22
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53860981"
---
# <a name="idebugmessageevent2"></a>IDebugMessageEvent2
Bu arabirim, hata ayıklama altyapısı (DE), kullanıcıdan bir yanıt gerektirir. Visual Studio için bir ileti göndermek için kullanılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugMessageEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Visual Studio için kullanıcı yanıt isteyen bir ileti göndermek için bu arabirimini DE uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi.  
  
 Bu arabirim uygulamasını Visual Studio'nun çağrısı iletişim kurması gereken [SetResponse](../../../extensibility/debugger/reference/idebugmessageevent2-setresponse.md) DE için. Örneğin, bu iş parçacığı işleme DE'ın iletiye gönderilen bir ileti ile yapılabilir veya bu arabirimi uygulayan nesnenin bir başvuru DE tutmak ve yöntemlere geçirilen yanıt için DE bir geri arama `IDebugMessageEvent2::SetResponse`.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 KODU oluşturur ve bir yanıt gerektirir kullanıcıya bir ileti görüntülemek için bu olay nesneyi gönderir. Olay kullanılarak gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugMessageEvent2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetMessage](../../../extensibility/debugger/reference/idebugmessageevent2-getmessage.md)|Görüntülenecek iletiyi alır.|  
|[SetResponse](../../../extensibility/debugger/reference/idebugmessageevent2-setresponse.md)|İleti kutusu gelen yanıt ayarlar.|  
  
## <a name="remarks"></a>Açıklamalar  
 Belirli bir iletiyi kullanıcı belirli bir yanıtı gerektiriyorsa, bu arabirim DE kullanır. Girişimi uzaktan bir programa ekledikten sonra "Erişim engellendi" iletisi DE alır, örneğin, DE bu belirli ileti Visual Studio'da gönderir bir `IDebugMessageEvent2` ileti kutusunun stili olayla `MB_RETRYCANCEL`. Bu, kullanıcının yeniden deneyin veya iliştirme işlemi iptal izin verir.  
  
 DE nasıl bu iletiyi Win32 işlevini kurallarına göre işleneceğini belirtir `MessageBox` (bkz [AfxMessageBox](/cpp/mfc/reference/cstring-formatting-and-message-box-display#afxmessagebox) Ayrıntılar için).  
  
 Kullanım [IDebugErrorEvent2](../../../extensibility/debugger/reference/idebugerrorevent2.md) kullanıcıdan yanıt gerektirmeyen Visual Studio ileti göndermek için arabirim.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)   
 [IDebugErrorEvent2](../../../extensibility/debugger/reference/idebugerrorevent2.md)