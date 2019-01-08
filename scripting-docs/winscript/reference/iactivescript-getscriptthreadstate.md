---
title: IActiveScript::GetScriptThreadState | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.GetScriptThreadState
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_GetScriptThreadState
ms.assetid: 7cac94d0-436e-4c29-895b-0c4afa0b3ccc
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2b191f1b70aa522cba0a04e0781ada69a8fe5ca5
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097532"
---
# <a name="iactivescriptgetscriptthreadstate"></a>IActiveScript::GetScriptThreadState
Bir betik iş parçacığı geçerli durumunu alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetScriptThreadState(  
    SCRIPTTHREADID stidThread,    // identifier of script thread  
    SCRIPTTHREADSTATE *pstsState  // receives state flag  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `stidThread`  
 [in] Kendisi için durumu istenen iş parçacığı tanıtıcısı veya aşağıdaki özel iş parçacığı tanımlayıcılarından birini:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|SCRIPTTHREADID_BASE|Temel; iş parçacığı diğer bir deyişle, iş parçacığı, komut dosyası altyapısı örneği.|  
|SCRIPTTHREADID_CURRENT|Şu anda yürütülen iş parçacığı.|  
  
 `pstsState`  
 [out] Belirtilen iş parçacığı durumu alan değişkenin adresi. Durum tarafından tanımlanan adlandırılan sabit değerlerden biri tarafından belirtilen [SCRIPTTHREADSTATE numaralandırması](../../winscript/reference/scriptthreadstate-enumeration.md) sabit listesi. Bu parametre, geçerli iş parçacığı tanımlamaz, durumu herhangi bir zamanda değişebilir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı henüz yüklenen başlatıldı veya).|  
  
## <a name="remarks"></a>Açıklamalar  
 Temel olmayan belirtme ana bilgisayar nesneleri veya çok kaynaklanan olmadan, bu yöntem temel olmayan iş parçacığından çağrılabilir [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md) arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)