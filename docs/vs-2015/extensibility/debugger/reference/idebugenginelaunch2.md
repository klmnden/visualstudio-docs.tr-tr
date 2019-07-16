---
title: IDebugEngineLaunch2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugEngineLaunch2
helpviewer_keywords:
- IDebugEngineLaunch2 interface
ms.assetid: 5eaf2ad8-3fbf-446e-b48b-5327ad3f5255
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ccbe76d800be035bc39caa477955b91bf21c074e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68195681"
---
# <a name="idebugenginelaunch2"></a>IDebugEngineLaunch2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Başlatma ve sonlandırma programlar için hata ayıklama altyapısı (DE) tarafından kullanılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugEngineLaunch2 : IDebugEngine2  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Tamamen özel bir bağlantı noktası tarafından işlenen bir işlem başlatmaya özel gereksinimleriniz varsa, bu arabirim tarafından bir özel DE uygulanır. Bu genellikle DE yorumlayıcıyı parçası olduğunda ve bir betik ayıklanan işlemin durumdur: yorumlayıcı önce başlatılması gerekir ve ardından betiği yüklenen çalışmaya ve. Bir bağlantı noktası yorumlayıcı başlatabilirsiniz, ancak komut dosyası (aynı role DE sahip olduğu) bir özel işlem gerektirebilir. Yalnızca özel bir bağlantı noktası işleyemiyor bir programın tanıtımından benzersiz gereksinimleri varsa, bu arabirim uygulanır.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim SDM sağlayabilirseniz bu arabirim oturum hata ayıklama Yöneticisi (SDM) tarafından çağrılır [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md) (QueryInterface kullanarak) arabirim. Bu arabirim elde edilebilir, DE özel gereksinimleri vardır ve başlatabiliyorsanız bağlantı noktası yerine programını başlatmak için bu arabirimi çağırır SDM bilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugEngineLaunch2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md)|Bir işlem DE yoluyla başlatır.|  
|[ResumeProcess](../../../extensibility/debugger/reference/idebugenginelaunch2-resumeprocess.md)|Sürdürür, yürütme işlemi.|  
|[CanTerminateProcess](../../../extensibility/debugger/reference/idebugenginelaunch2-canterminateprocess.md)|Bir işlemin sona erdirilecek belirler.|  
|[TerminateProcess](../../../extensibility/debugger/reference/idebugenginelaunch2-terminateprocess.md)|Bir işlemi sonlandırır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)
