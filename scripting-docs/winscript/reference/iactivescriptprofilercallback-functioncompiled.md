---
title: IActiveScriptProfilerCallback::FunctionCompiled | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptProfilerCallback.FunctionCompiled
apilocation:
- scrobj.dll
ms.assetid: a7e9ef17-3891-4731-9d08-c37bc489be61
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4bd032914605c61b13a0a56a42e510c2af252f7e
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54091409"
---
# <a name="iactivescriptprofilercallbackfunctioncompiled"></a>IActiveScriptProfilerCallback::FunctionCompiled
Profil oluşturucu komut dosyası motoru nesne bir komut dosyası derlenirken bir işlevle karşılaştığında bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT FunctionCompiled(  
    [in] PROFILER_TOKEN functionId,  
    [in] PROFILER_TOKEN scriptId,  
    [in] [string] const WCHAR *pwszFunctionName,  
    [in] [string] const WCHAR *pwszFunctionNameHint,  
    [in] IUnknown *pIDebugDocumentContext);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `functionId`  
 [in] İşlev benzersiz kimliği. Bu kimlik, komut dosyası altyapısı tarafından atanır.  
  
 `scriptId`  
 [in] İşlev parçasıdır betik benzersiz kimliği.  
  
 `pwszFunctionName`  
 [in] Anonim bir işlev adı işlevi ya da null.  
  
 `pwszFunctionNameHint`  
 [in] Çıkarsanan adı işlev veya komut dosyası altyapısı herhangi adını çıkarsamak değil yoksa null.  
  
 `pIDebugDocumentContext`  
 [in] Mevcut ise, işaretçi bir `IUnknown` profil oluşturucu için faydalanacaksa arabirimi bir [Idebugdocumentcontext arabirimi](../../winscript/reference/idebugdocumentcontext-interface.md) işaretçi. Aksi takdirde null.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu yöntemin dönüş değerini komut dosyası altyapısı tarafından göz ardı edilir.  
  
## <a name="remarks"></a>Açıklamalar  
 Yalnızca bu ana bilgisayar tarafından destekleniyorsa komut dosyası altyapısı belge bağlamı sağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptProfilerCallback Arabirimi](../../winscript/reference/iactivescriptprofilercallback-interface.md)