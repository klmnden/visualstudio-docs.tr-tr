---
title: IActiveScriptProfilerCallback::ScriptCompiled | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptProfilerCallback.ScriptCompiled
apilocation:
- scrobj.dll
ms.assetid: 1bb8e9be-cbb1-4a61-b36c-805127a56ac7
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a198667e7dc30969c32b556620b139d52f833543
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58158938"
---
# <a name="iactivescriptprofilercallbackscriptcompiled"></a>IActiveScriptProfilerCallback::ScriptCompiled
Komut dosyası motoru nesne derlenmiş bir komut dosyası profil oluşturucu bildirir. Bu yöntem derlendiğinde her komut için çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT ScriptCompiled(  
    [in] PROFILER_TOKEN scriptId,  
    [in] PROFILER_SCRIPT_TYPE type,  
    [in] IUnknown *pIDebugDocumentContext);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `scriptId`  
 [in] Derlenen kodun benzersiz kimliği. Bu kimlik, komut dosyası altyapısı tarafından atanır.  
  
 `type`  
 [in] Derlenen kodun türü. Değerleri tanımlanan [profıler_scrıpt_type numaralandırması](../../winscript/reference/profiler-script-type-enumeration.md).  
  
 `pIDebugDocumentContext`  
 [in] Mevcut ise, işaretçi bir `IUnknown` profil oluşturucu için faydalanacaksa arabirimi bir [Idebugdocumentcontext arabirimi](../../winscript/reference/idebugdocumentcontext-interface.md) işaretçi. Aksi takdirde, bu null olacaktır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu yöntemin dönüş değerini komut dosyası altyapısı tarafından göz ardı edilir.  
  
## <a name="remarks"></a>Açıklamalar  
 Yalnızca bu ana bilgisayar tarafından destekleniyorsa komut dosyası altyapısı belge bağlamı sağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptProfilerCallback Arabirimi](../../winscript/reference/iactivescriptprofilercallback-interface.md)