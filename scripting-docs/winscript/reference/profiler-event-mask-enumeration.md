---
title: Profıler_event_mask sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- PROFILER_EVENT_MASK
apilocation:
- scrobj.dll
ms.assetid: c2168408-f4f6-4600-971d-f15b4edf4ca2
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: da55371c24f6a21acbc9dc789a2c76ef6e7c66b4
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54096674"
---
# <a name="profilereventmask-enumeration"></a>PROFILER_EVENT_MASK Numaralandırması
Profili oluşturulması olay türlerini belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef enum {  
    PROFILER_EVENT_MASK_TRACE_SCRIPT_FUNCTION_CALL = 0x00000001,  
    PROFILER_EVENT_MASK_TRACE_NATIVE_FUNCTION_CALL = 0x00000002,  
    PROFILER_EVENT_MASK_TRACE_DOM_FUNCTION_CALL    = 0x00000004,  
    PROFILER_EVENT_MASK_TRACE_ALL =  
    PROFILER_EVENT_MASK_TRACE_SCRIPT_FUNCTION_CALL |  
    PROFILER_EVENT_MASK_TRACE_NATIVE_FUNCTION_CALL,  
    PROFILER_EVENT_MASK_TRACE_ALL_WITH_DOM = PROFILER_EVENT_MASK_TRACE_ALL |  
    PROFILER_EVENT_MASK_TRACE_DOM_FUNCTION_CALL  
} PROFILER_EVENT_MASK;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Açıklama|  
|------------|-----------------|  
|PROFILER_EVENT_MASK_TRACE_SCRIPT_FUNCTION_CALL|Kullanıcı tarafından yazılan betik ve dinamik kod tanımlanmış profilleri işlevleri.|  
|PROFILER_EVENT_MASK_TRACE_NATIVE_FUNCTION_CALL|Komut dosyası altyapısı tarafından tanımlanmış profilleri yerel işlevleri.|  
|PROFILER_EVENT_MASK_TRACE_ALL|Belge nesne modeli (DOM) içine çağrıları hariç tüm kullanıcı tanımlı ve komut dosyası altyapısı işlevler profiller.|  
|PROFILER_EVENT_MASK_TRACE_DOM_FUNCTION_CALL|DOM'a çağrı profilleri işlevleri|  
|PROFILER_EVENT_MASK_TRACE_ALL_WITH_DOM|DOM çağrılar dahil olmak üzere tüm işlevleri profilleri|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin komut dosyası Profiler sabitleri, numaralandırmaları ve yapıları](../../winscript/reference/active-script-profiler-constants-enumerations-and-structures.md)   
 [IActiveScriptProfilerControl::SetProfilerEventMask](../../winscript/reference/iactivescriptprofilercontrol-setprofilereventmask.md)   
 [IActiveScriptProfilerControl::StartProfiling](../../winscript/reference/iactivescriptprofilercontrol-startprofiling.md)