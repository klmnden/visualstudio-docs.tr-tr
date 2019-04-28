---
title: IActiveScriptProfilerCallback::OnFunctionExit | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptProfilerCallback.OnFunctionExit
apilocation:
- scrobj.dll
ms.assetid: a5d21715-2b0b-423e-8644-f04a9e7cde3d
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9c84b64a12b1a6b61399f70b7209c86dd8d2a9a4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62993338"
---
# <a name="iactivescriptprofilercallbackonfunctionexit"></a>IActiveScriptProfilerCallback::OnFunctionExit
Profil Oluşturucu bir işlev yürütülürken tamamlanmış komut dosyası altyapısı çağrı, nesne bir çağrı belge nesne modeli (DOM) içine değil bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OnFunctionExit(  
    [in] PROFILER_TOKEN scriptId,   
    [in] PROFILER_TOKEN functionId);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `scriptId`  
 [in] İşlev parçasıdır betik benzersiz kimliği. Bu kimlik, komut dosyası altyapısı tarafından atanır.  
  
 `functionId`  
 [in] İşlev benzersiz kimliği. Bu kimlik, komut dosyası altyapısı tarafından atanır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu yöntemin dönüş değerini komut dosyası altyapısı tarafından göz ardı edilir.  
  
## <a name="remarks"></a>Açıklamalar  
 DOM için komut dosyası altyapısı aramaları [IActiveScriptProfilerCallback2::OnFunctionExitByName](../../winscript/reference/iactivescriptprofilercallback2-onfunctionexitbyname.md) yerine `IActiveScriptProfilerCallback::OnFunctionExit`. Bu çok sayıda benzersiz yöntemleri ve özellikleri sayısında kaynaklanır  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptProfilerCallback::OnFunctionEnter](../../winscript/reference/iactivescriptprofilercallback-onfunctionenter.md)   
 [IActiveScriptProfilerCallback Arabirimi](../../winscript/reference/iactivescriptprofilercallback-interface.md)