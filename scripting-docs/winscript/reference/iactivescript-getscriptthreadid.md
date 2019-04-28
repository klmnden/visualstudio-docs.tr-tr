---
title: IActiveScript::GetScriptThreadID | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.GetScriptThreadID
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_GetScriptThreadID
ms.assetid: 2595d76e-30b5-429f-88b4-1d026645dd9b
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d329e08e6a17d9edcdf26e14b468c3c56f036c00
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62935698"
---
# <a name="iactivescriptgetscriptthreadid"></a>IActiveScript::GetScriptThreadID
Belirli Win32 iş parçacığı ile ilişkili iş parçacığı için bir komut dosyası altyapısı-tanımlı tanımlayıcı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetScriptThreadID(  
    DWORD dwWin32ThreadID,       // Win32 thread identifier.  
    SCRIPTTHREADID *pstidThread  // Receives scripting thread. identifier  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwWin32ThreadID` ,  
 [in] Geçerli işlemde çalışan bir Win32 iş parçacığı tanıtıcısı iş parçacığı. Kullanım [IActiveScript::GetCurrentScriptThreadID](../../winscript/reference/iactivescript-getcurrentscriptthreadid.md) şu anda yürütülen iş parçacığının iş parçacığı tanıtıcısını almak için işlevi.  
  
 `pstidThread` ,  
 [out] Belirli Win32 iş parçacığı ile ilişkili komut dosyası iş parçacığı tanıtıcısını alan bir değişkenin adresidir. Bu tanımlayıcının yorumu komut dosyası altyapısı için kalır, ancak Windows iş parçacığı tanıtıcısını yalnızca bir kopyasını olabilir. Win32 iş parçacığı sona ererse, bu tanımlayıcıyı atanmamış haline gelir ve bundan sonra başka bir iş parçacığına atanabilir unutmayın.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı henüz yüklenen başlatıldı veya) ve bu nedenle başarısız oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Alınan tanımlayıcı komut iş parçacığı yürütme denetimi yöntemlerine yapılan sonraki çağrılar gibi kullanılabilir [IActiveScript::InterruptScriptThread](../../winscript/reference/iactivescript-interruptscriptthread.md) yöntemi.  
  
 Temel olmayan belirtme ana bilgisayar nesneleri veya çok kaynaklanan olmadan, bu yöntem temel olmayan iş parçacığından çağrılabilir [IActiveScript::InterruptScriptThread](../../winscript/reference/iactivescript-interruptscriptthread.md) arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)