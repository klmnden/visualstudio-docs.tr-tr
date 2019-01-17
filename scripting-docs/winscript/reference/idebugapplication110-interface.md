---
title: Idebugapplication110 arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: b13208d6a507ea4ed3157606f358b6b0168180cf
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349562"
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