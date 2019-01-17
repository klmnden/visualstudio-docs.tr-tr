---
title: Idebugapplicationthread arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 262174d0daecd2c37bafbecee13532ba62e9967f
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54347794"
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