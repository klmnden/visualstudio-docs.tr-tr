---
title: IActiveScriptProfilerCallback::Shutdown | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 091ccc30f16081fdca8f10778efec208ef5ccb16
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62993429"
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