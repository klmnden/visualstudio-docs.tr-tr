---
title: IActiveScript::GetCurrentScriptThreadID | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 9e1b6e7bae7d78c18e11cd1aac8d0844fb9e90a5
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58152255"
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