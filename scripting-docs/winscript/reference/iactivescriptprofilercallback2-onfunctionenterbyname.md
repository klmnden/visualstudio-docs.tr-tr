---
title: IActiveScriptProfilerCallback2::OnFunctionEnterByName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptProfilerCallback2::OnFunctionEnterByName
ms.assetid: 24b1593a-97fc-4d70-9b85-ec86fb59f987
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f6fdb4addace1b0bbabdd4303c3943b976763514
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62993273"
---
# <a name="iactivescriptprofilercallback2onfunctionenterbyname"></a>IActiveScriptProfilerCallback2::OnFunctionEnterByName
Belge nesne modeli (DOM) işlev çağrısı yürütmek için komut dosyası altyapısı gidip profil oluşturucu nesne bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OnFunctionEnterByName(  
    [in] [string] const WCHAR *pwszFunctionName,  
    [in] PROFILER_SCRIPT_TYPE scriptType);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pwszFunctionName`  
 [in] Yürütülecek komut dosyası altyapısı geçiyor işlevi adı.  
  
 `scriptType`  
 [in] İşlev türü. Geçerli değerler açıklamaları için bkz. [profıler_scrıpt_type numaralandırması](../../winscript/reference/profiler-script-type-enumeration.md).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu yöntemin dönüş değerini komut dosyası altyapısı tarafından göz ardı edilir.  
  
## <a name="remarks"></a>Açıklamalar  
 DOM için komut dosyası altyapısının bu yöntemi çağırmak yerine aramaları [IActiveScriptProfilerCallback::OnFunctionEnter](../../winscript/reference/iactivescriptprofilercallback-onfunctionenter.md). Bu çok sayıda benzersiz yöntemleri ve özellikleri sayısında kaynaklanır  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptProfilerCallback2::OnFunctionExitByName](../../winscript/reference/iactivescriptprofilercallback2-onfunctionexitbyname.md)   
 [IActiveScriptProfilerCallback2 Arabirimi](../../winscript/reference/iactivescriptprofilercallback2-interface.md)