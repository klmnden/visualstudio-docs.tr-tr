---
title: IActiveScript::SetScriptState | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.SetScriptState
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_SetScriptState
ms.assetid: f2b2700c-0c8d-40db-ad84-dc751c5d9bc2
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 16a13b545ddd482f8aa143d289d46447370e23ac
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62935537"
---
# <a name="iactivescriptsetscriptstate"></a>IActiveScript::SetScriptState
Komut dosyası altyapısı belirli bir duruma koyar. Temel olmayan belirtme ana bilgisayar nesneleri veya çok kaynaklanan olmadan, bu yöntem temel olmayan iş parçacığından çağrılabilir [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md) arabirimi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetScriptState(  
    SCRIPTSTATE ss  // identifier of new state  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ss`  
 [in] Komut dosyası altyapısı verilen durumuna ayarlar. İçinde tanımlanan değerlerden biri olabilir [SCRIPTSTATE numaralandırması](../../winscript/reference/scriptstate-enumeration.md) sabit listesi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_FAIL`|Komut dosyası altyapısı başlatılmış durumuna geçişi desteklemez. Konak gerekir bu komut dosyası altyapısı AT oluşturmak, başlatmak ve aynı etkiyi elde etmek için yeni bir komut dosyası altyapısı yüklenemiyor.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı henüz yüklenen başlatıldı veya) ve bu nedenle başarısız oldu.|  
|`OLESCRIPT_S_PENDING`|Yöntemi başarıyla kuyruğa alındı, ancak durumu henüz değişmedi. Durum değişikliklerini site çağrılacağı geri aracılığıyla [IActiveScriptSite::OnStateChange](../../winscript/reference/iactivescriptsite-onstatechange.md) yöntemi.|  
|`S_FALSE`|Yöntem başarılı oldu, ancak komut zaten belirtilen durumda olan.|  
  
## <a name="remarks"></a>Açıklamalar  
 Komut dosyası motoru durumu bölümü, komut dosyası motoru durumu hakkında daha fazla bilgi için bkz. [Windows betik motorları](../../winscript/windows-script-engines.md) .  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript::Clone](../../winscript/reference/iactivescript-clone.md)   
 [IActiveScript::GetScriptDispatch](../../winscript/reference/iactivescript-getscriptdispatch.md)   
 [IActiveScript::InterruptScriptThread](../../winscript/reference/iactivescript-interruptscriptthread.md)   
 [IActiveScriptParse::ParseScriptText](../../winscript/reference/iactivescriptparse-parsescripttext.md)   
 [IActiveScriptSite::GetItemInfo](../../winscript/reference/iactivescriptsite-getiteminfo.md)