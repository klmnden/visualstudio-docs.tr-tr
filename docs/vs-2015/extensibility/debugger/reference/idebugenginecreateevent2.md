---
title: IDebugEngineCreateEvent2 | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugEngineCreateEvent2
helpviewer_keywords:
- IDebugEngineCreateEvent2 interface
ms.assetid: 37c0a841-1c8d-4802-a990-36b54bca3ef7
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 69b8cf3a2bdb4dbdeb964bd53bb39b386cdd1d0a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49185204"
---
# <a name="idebugenginecreateevent2"></a>IDebugEngineCreateEvent2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

DE örneği oluşturulurken hata ayıklama altyapısı (DE) Bu arabirim oturum hata ayıklama Yöneticisi (SDM) gönderir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugEngineCreateEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 DE normal işlemlerini bir parçası olarak bu arabirimi uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde (SDM kullanan `QueryInterface` erişmeye yöntemi `IDebugEvent2` arabirimi).  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 KODU oluşturur ve DE örneği oluşturulduğunda bu olay nesneyi gönderir. Olay kullanılarak gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugEngineCreateEvent2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetEngine](../../../extensibility/debugger/reference/idebugenginecreateevent2-getengine.md)|Yeni oluşturulan hata ayıklama altyapısı (DE) temsil eden nesnesini alır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)

