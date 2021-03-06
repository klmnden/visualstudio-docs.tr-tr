---
title: Idebugapplicationthreadevents110 arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationThreadEvents110 Interface
ms.assetid: 91a98b0e-7c81-4118-af75-82f75fd4f25a
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b2cdde46484f95aa57404ebe6b6cb4c86ef458c9
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63440501"
---
# <a name="idebugapplicationthreadevents110-interface"></a>IDebugApplicationThreadEvents110 Arabirimi
Daha fazla iş parçacığı olaylar ekler. Bu olaylar yalnızca büyük/küçük harf yereldir. Diğer bir deyişle, yalnızca süreci içinde abone olursanız hata ayıklama, kullanarak [IConnectionPoint](http://go.microsoft.com/fwlink/?LinkId=232738) önerilerde bulunabilir ve PDM uygulama iş parçacığı nesneleri üzerinde yöntemleri eşlemesindeki (uygulayan nesneler [Idebugapplicationthread Arabirim](../../winscript/reference/idebugapplicationthread-interface.md)). Nereden geldiğini iş parçacığı üzerinde oluşur.  
  
> [!IMPORTANT]
> Bu arabirim PDM v11.0 ve sonraki sürümler tarafından uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="methods"></a>Yöntemler  
 `IDebugActivationThreadEvents110` Arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugApplicationThreadEvents110 ::OnBeginThreadRequest](../../winscript/reference/idebugapplicationthreadevents110-onbeginthreadrequest.md)|Çağrı akışına PDM'ın iş parçacığı kullanarak geçiş başladı.|  
|[IDebugApplicationThreadEvents110::OnResumeFromBreakPoint](../../winscript/reference/idebugapplicationthreadevents110-onresumefrombreakpoint.md)|İş parçacığı bir kesme noktasından sürdürme ve bir kez daha etkin olacaktır.|  
|[IDebugApplicationThreadEvents110::OnSuspendForBreakPoint](../../winscript/reference/idebugapplicationthreadevents110-onsuspendforbreakpoint.md)|İş parçacığı, bir kesme noktası için askıya alma ve tam olarak yakında askıya alınacak iş parçacığını gerektiren çağrılarını işleyebilir.|  
|[IDebugApplicationThreadEvents110::OnThreadRequestComplete](../../winscript/reference/idebugapplicationthreadevents110-onthreadrequestcomplete.md)|Çağrı akışına PDM'ın iş parçacığı kullanarak geçişi tamamlandı.|