---
title: Idebugapplicationthread arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationThread interface
ms.assetid: f869c328-4409-4b74-a6c3-9e63fc58c63d
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a464085eddbea4f5d29c684c0f1dabc6f853b6d1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62822232"
---
# <a name="idebugapplicationthread-interface"></a>IDebugApplicationThread Arabirimi
Dil altyapıları ve ana iş parçacığı eşitleme sağlamak ve iş parçacığına özgü hata ayıklama durum bilgilerini korumak için sağlar. Bu arabirim genişletir `IRemoteDebugApplicationThread` iş parçacığı olmayan uzaktan erişim sağlamak için arabirim.  
  
 Devralınan yöntemleri yanı sıra `IRemoteDebugApplicationThread`, `IDebugApplicationThread` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugApplicationThread::SynchronousCallIntoThread](../../winscript/reference/idebugapplicationthread-synchronouscallintothread.md)|Çağıran uygulama iş parçacığında kodu çalıştırmak bir mekanizma sağlar.|  
|[IDebugApplicationThread::QueryIsCurrentThread](../../winscript/reference/idebugapplicationthread-queryiscurrentthread.md)|Bu iş parçacığı şu anda çalışan iş parçacığının olup olmadığını belirler.|  
|[IDebugApplicationThread::QueryIsDebuggerThread](../../winscript/reference/idebugapplicationthread-queryisdebuggerthread.md)|Bu iş parçacığı hata ayıklayıcı iş parçacığı olup olmadığını belirler.|  
|[IDebugApplicationThread::SetDescription](../../winscript/reference/idebugapplicationthread-setdescription.md)|Bu iş parçacığının açıklaması ayarlar.|  
|[IDebugApplicationThread::SetStateString](../../winscript/reference/idebugapplicationthread-setstatestring.md)|İş parçacığı durumu açıklaması ayarlar.|