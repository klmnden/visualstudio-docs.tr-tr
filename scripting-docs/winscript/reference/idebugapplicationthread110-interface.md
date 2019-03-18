---
title: Idebugapplicationthread110 arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationThread110 Interface
ms.assetid: 25bc351f-3451-4387-9302-078f6292ddff
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a40b1a6f194ef0f335d8c6516b101250b0d980fe
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58158415"
---
# <a name="idebugapplicationthread110-interface"></a>IDebugApplicationThread110 Arabirimi
İçin daha fazla işlevsellik sağlayan [Idebugapplicationthread arabirimi](../../winscript/reference/idebugapplicationthread-interface.md) arabirimi.  
  
> [!IMPORTANT]
>  Bu arabirim PDM v11.0 ve sonraki sürümler tarafından uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="methods"></a>Yöntemler  
 `IDebugApplicationThread110` Arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugApplicationThread110::AsynchronousCallIntoThread](../../winscript/reference/idebugapplicationthread110-asynchronouscallintothread.md)|Ana iş parçacığında zaman uyumsuz bir çağrı yapar.|  
|[IDebugApplicationThread110::GetActiveThreadRequestCount](../../winscript/reference/idebugapplicationthread110-getactivethreadrequestcount.md)|Ne kadar iş parçacığı istekleri mekanizmaları geçiş PDM'ın iş parçacığından şu anda işleme sayısı. Genellikle 0 veya 1, ancak bu bir iş parçacığı çağrı işleme başlar ancak iş parçacığı dışında bir zaman uyumlu çağrıyı tetikler veya aksi halde iş parçacığını askıya alır (örneğin, hata ayıklayıcıyı verilen IDebugApplicationEvents olarak olay tetiklemeyi tarafından daha yüksek olması olası iş parçacığı)|  
|[IDebugApplicationThread110::IsSuspendedForBreakPoint](../../winscript/reference/idebugapplicationthread110-issuspendedforbreakpoint.md)|[IDebugApplicationThreadEvents110::OnSuspendForBreakPoint](../../winscript/reference/idebugapplicationthreadevents110-onsuspendforbreakpoint.md) bu iş parçacığı üzerinde çağrılmış var ve henüz tamamlanmadı.|  
|[IDebugApplicationThread110::IsThreadCallable](../../winscript/reference/idebugapplicationthread110-isthreadcallable.md)|Bu iş parçacığı PDM'ın iş parçacığı (örneğin, SynchronousCallInThread) mekanizmaları geçiş kullanarak yapılan çağrılar işleyebilen bir durumda.|