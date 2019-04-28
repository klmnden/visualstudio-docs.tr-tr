---
title: IActiveScriptProfilerCallback2::OnFunctionExitByName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptProfilerCallback2::OnFunctionExitByName
ms.assetid: a6ddead4-e66d-4789-b778-84e5c343f908
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 87f0b7e7a3cea4e3e59fb43ef9ddc2d4934552e6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62993351"
---
# <a name="iactivescriptprofilercallback2onfunctionexitbyname"></a>IActiveScriptProfilerCallback2::OnFunctionExitByName
Profil oluşturucu komut dosyası motoru nesne çalışan bir belge nesne modeli (DOM) işlev çağrısı tamamlandı bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OnFunctionExitByName(  
    [in] [string] const WCHAR *pwszFunctionName,  
    [in] PROFILER_SCRIPT_TYPE scriptType);  
  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pwszFunctionName`  
 [in] Komut dosyası altyapısı çalışması sona işlevinin adı.  
  
 `scriptType`  
 [in] İşlev türü. Geçerli değerler açıklamaları için bkz. [profıler_scrıpt_type numaralandırması](../../winscript/reference/profiler-script-type-enumeration.md).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu yöntemin dönüş değerini komut dosyası altyapısı tarafından göz ardı edilir.  
  
## <a name="remarks"></a>Açıklamalar  
 DOM için komut dosyası altyapısının bu yöntemi çağırmak yerine aramaları [IActiveScriptProfilerCallback::OnFunctionExit](../../winscript/reference/iactivescriptprofilercallback-onfunctionexit.md). Bu çok sayıda benzersiz yöntemleri ve özellikleri sayısında kaynaklanır  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptProfilerCallback2::OnFunctionEnterByName](../../winscript/reference/iactivescriptprofilercallback2-onfunctionenterbyname.md)   
 [IActiveScriptProfilerCallback2 Arabirimi](../../winscript/reference/iactivescriptprofilercallback2-interface.md)