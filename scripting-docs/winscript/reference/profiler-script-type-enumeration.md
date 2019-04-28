---
title: Profıler_scrıpt_type sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- PROFILER_SCRIPT_TYPE
apilocation:
- scrobj.dll
ms.assetid: 3ab6633a-6241-44f0-b837-14336f70c71e
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ca90a566db422d75fefc44267ffe10504bb872ce
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62816791"
---
# <a name="profilerscripttype-enumeration"></a>PROFILER_SCRIPT_TYPE Numaralandırması
Betik türünü belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef enum {  
    PROFILER_SCRIPT_TYPE_USER,  
    PROFILER_SCRIPT_TYPE_DYNAMIC,  
    PROFILER_SCRIPT_TYPE_NATIVE,  
    PROFILER_SCRIPT_TYPE_DOM  
} PROFILER_SCRIPT_TYPE;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Açıklama|  
|------------|-----------------|  
|PROFILER_SCRIPT_TYPE_USER|Kullanıcı tarafından yazılan kodu belirtir.|  
|PROFILER_SCRIPT_TYPE_DYNAMIC|Yürütme sırasında dinamik olarak oluşturulan kodu belirtir.|  
|PROFILER_SCRIPT_TYPE_NATIVE|Yerel işlevleri ve komut dosyası altyapısı tarafından tanımlanan nesneleri için betik türünü belirtir.|  
|PROFILER_SCRIPT_TYPE_DOM|Bir çağrı, Internet Explorer gibi bir çağrı belge nesne modeli (DOM) içine belirtir `document.getElementById` yöntemi.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin komut dosyası Profiler sabitleri, numaralandırmaları ve yapıları](../../winscript/reference/active-script-profiler-constants-enumerations-and-structures.md)   
 [IActiveScriptProfilerCallback::ScriptCompiled](../../winscript/reference/iactivescriptprofilercallback-scriptcompiled.md)   
 [IActiveScriptProfilerCallback2::OnFunctionEnterByName](../../winscript/reference/iactivescriptprofilercallback2-onfunctionenterbyname.md)   
 [IActiveScriptProfilerCallback2::OnFunctionExitByName](../../winscript/reference/iactivescriptprofilercallback2-onfunctionexitbyname.md)