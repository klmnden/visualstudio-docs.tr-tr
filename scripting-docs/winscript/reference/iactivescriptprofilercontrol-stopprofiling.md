---
title: IActiveScriptProfilerControl::StopProfiling | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptProfilerControl.StopProfiling
apilocation:
- scrobj.dll
ms.assetid: 23b46ed6-a398-44c0-bc49-bf122e697cfe
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 750693db9aa809e6b3521f0312cebcf45d8d720d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62993014"
---
# <a name="iactivescriptprofilercontrolstopprofiling"></a>IActiveScriptProfilerControl::StopProfiling
Komut dosyası altyapısına profil oluşturmayı durdurur. Bu yöntemin çağırdığı [IActiveScriptProfilerCallback::Shutdown](../../winscript/reference/iactivescriptprofilercallback-shutdown.md) profil oluşturucu nesnesindeki ve ardından serbest bırakır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT StopProfiling(  
    [in] HRESULT hrShutdownReason);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `hrShutdownReason`  
 [in] Bir parametre olarak geçirilecek HRESULT [IActiveScriptProfilerCallback::Shutdown](../../winscript/reference/iactivescriptprofilercallback-shutdown.md) profil oluşturucu nesnesini yöntemi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 HRESULT döndürür. Olası değerler aşağıdaki gibidir:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`ACTIVPROF_E_PROFILER_ABSENT`|Profil oluşturma etkin değil.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptProfilerControl Arabirimi](../../winscript/reference/iactivescriptprofilercontrol-interface.md)