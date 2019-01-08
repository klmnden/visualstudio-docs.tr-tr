---
title: Profıler_scrıpt_type sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: ac387af4601ff822982c10e61f9813b2db7e8047
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086916"
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