---
title: Idebugapplication110 arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplication110 Interface
ms.assetid: ae943133-eb65-4ddc-a29f-9280a82dd8d6
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3c040df103bac464e4f440f23674da966063f0ae
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58149675"
---
# <a name="idebugapplication110-interface"></a>IDebugApplication110 Arabirimi
`IDebugApplication110` Arabirimi işlevselliğini genişleten [Idebugapplication arabirimi](../../winscript/reference/idebugapplication-interface.md). Uygulaması QueryInterface çağırarak bu arabirimin örneğini alabilirsiniz [Idebugapplication arabirimi](../../winscript/reference/idebugapplication-interface.md).  
  
> [!IMPORTANT]
>  Bu arabirim PDM v11.0 ve sonraki sürümler tarafından uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="methods"></a>Yöntemler  
 `IDebugApplication110` Arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugApplication110::SynchronousCallInMainThread](../../winscript/reference/idebugapplication110-synchronouscallinmainthread.md)|Ana iş parçacığında zaman uyumlu bir çağrı yapar.|  
|[IDebugApplication110::AsynchronousCallInMainThread](../../winscript/reference/idebugapplication110-asynchronouscallinmainthread.md)|Ana iş parçacığında zaman uyumsuz bir çağrı yapar.|  
|[IDebugApplication110::CallableWaitForHandles](../../winscript/reference/idebugapplication110-callablewaitforhandles.md)|İzin verirken sinyal belirtilen tutamaçlardan birini bekler bu iş parçacığına yayımlanacak çağrıları iş parçacıkları arası. Bu yöntem, hata ayıklayıcı iş parçacığında çağrılmalıdır.|