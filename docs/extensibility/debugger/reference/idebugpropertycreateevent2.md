---
title: IDebugPropertyCreateEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPropertyCreateEvent2
helpviewer_keywords:
- IDebugPropertyCreateEvent2 interface
ms.assetid: 33b3082b-a42e-488a-a1e4-dadf506f922c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: edbd781fbaba285b56afca027aed657ee7585f3f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55003155"
---
# <a name="idebugpropertycreateevent2"></a>IDebugPropertyCreateEvent2
Belirli bir belge ile ilişkili olan bir özellik oluşturduğunda, bu arabirim hata ayıklama altyapısı (DE) tarafından oturum hata ayıklama Yöneticisi (SDM) gönderilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPropertyCreateEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 DE özellik oluşturulduğunu bildirmek için bu arabirimi uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi. Bu arabirim, yüklenen veya oluşturulan bir komut dosyasıyla ilişkili bir özelliği DE oluşturduysa ve bu betik IDE içinde görünmesi gereken uygulanır.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 DE oluşturur ve bu olay nesneyi bir özelliği oluşturulan rapora gönderir. Olay kullanılarak gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemini aşağıdaki tabloda gösterilmektedir `IDebugPropertyCreateEvent2` arabirimi.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetDebugProperty](../../../extensibility/debugger/reference/idebugpropertycreateevent2-getdebugproperty.md)|Yeni özelliği alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir özellik, belirli bir belge veya ilişkili komut dosyası varsa, DE bu olay için SDM güncelleştirmek için gönderebilirsiniz **betik belgelerini** penceresiyle belgenin adı. SDM çağıracak [GetExtendedInfo](../../../extensibility/debugger/reference/idebugproperty2-getextendedinfo.md) bağımsız değişkeniyle `guidDocument` almak için bir `VARIANT` içeren bir [IUnknown](/cpp/atl/iunknown) işaretçi. SDM çağıracak [QueryInterface](/cpp/atl/queryinterface) almak için bu işaretçinin [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md) güncelleştirmek için kullanılan arabirimi **betik belgelerini** penceresi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)