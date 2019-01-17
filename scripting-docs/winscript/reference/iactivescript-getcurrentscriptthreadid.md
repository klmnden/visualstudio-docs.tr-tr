---
title: IActiveScript::GetCurrentScriptThreadID | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.GetCurrentScriptThreadID
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_GetCurrentScriptThreadID
ms.assetid: b09e8b48-4209-480e-8b71-e99ee9ae2e17
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bac3b5755328e643c26c8f3746af6648d8ac06aa
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345805"
---
# <a name="iactivescriptgetcurrentscriptthreadid"></a>IActiveScript::GetCurrentScriptThreadID
Şu anda çalışan bir iş parçacığı için bir komut dosyası altyapısı-tanımlı tanımlayıcı alır. Tanımlayıcı betik iş parçacığı yürütme denetimi yöntemleri yapılan sonraki çağrılar gibi kullanılabilir [IActiveScript::InterruptScriptThread](../../winscript/reference/iactivescript-interruptscriptthread.md) yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetCurrentScriptThreadID(  
    SCRIPTTHREADID *pstidThread  // receives scripting thread identifier  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstidThread`  
 [out] Geçerli iş parçacığıyla ilişkilendirilmiş komut iş parçacığı tanıtıcısını alan bir değişkenin adresidir. Bu tanımlayıcının yorumu komut dosyası altyapısı için kalır, ancak Windows iş parçacığı tanıtıcısını yalnızca bir kopyasını olabilir. Win32 iş parçacığı sonlanır, bu tanımlayıcıyı atanmamış olur ve daha sonra başka bir iş parçacığına atanabilir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` başarılı olursa veya `E_POINTER` durumunda geçersiz işaretçi belirtildi.  
  
## <a name="remarks"></a>Açıklamalar  
 Temel olmayan belirtme ana bilgisayar nesneleri veya çok kaynaklanan olmadan, bu yöntem temel olmayan iş parçacığından çağrılabilir [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md) arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)