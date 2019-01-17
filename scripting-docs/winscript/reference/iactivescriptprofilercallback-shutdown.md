---
title: IActiveScriptProfilerCallback::Shutdown | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptProfilerCallback.Shutdown
apilocation:
- scrobj.dll
ms.assetid: 1281bf3c-d7d8-4ff5-9d8a-d1761fdb262e
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bbe5acd75ecf4f004d835490579b1f35c1bf675c
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346299"
---
# <a name="iactivescriptprofilercallbackshutdown"></a>IActiveScriptProfilerCallback::Shutdown
Profil oluşturma, bir komut dosyası altyapısına durdurulur zaman profil oluşturucu nesnesini bildirmek için çağırılır. Bu şekilde profil oluşturucu nesnesini gerekirse, temizleme yordamları çağırabilirsiniz. Komut dosyası altyapısı kapatılıyor veya çağrı zaman bu yöntem ayrıca komut dosyası altyapısı tarafından çağrılır [IActiveScriptProfilerCallback::Initialize](../../winscript/reference/iactivescriptprofilercallback-initialize.md) başarısız olur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Shutdown(  
    [in] HRESULT hrReason);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `hrReason`  
 [in] Kapatma açıklaması. Komut dosyası altyapısı kapatma olmadığını `S_OK` geçirilir. Çağrı [IActiveScriptProfilerCallback::Initialize](../../winscript/reference/iactivescriptprofilercallback-initialize.md) hata HRESULT döndürür, HRESULT geçirilir. Aksi takdirde, bu değer hizmetinden alınan [IActiveScriptProfilerControl::StopProfiling](../../winscript/reference/iactivescriptprofilercontrol-stopprofiling.md).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu yöntemin dönüş değerini komut dosyası altyapısı tarafından göz ardı edilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptProfilerCallback Arabirimi](../../winscript/reference/iactivescriptprofilercallback-interface.md)