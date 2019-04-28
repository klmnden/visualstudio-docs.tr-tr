---
title: IActiveScriptSite::OnScriptTerminate | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSite.OnScriptTerminate
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSite_OnScriptTerminate
ms.assetid: 3301ddf4-5929-404c-81d3-1a720e589008
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 664f974b26a2cae0d1e16d37dc3bc66e95993d6f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992650"
---
# <a name="iactivescriptsiteonscriptterminate"></a>IActiveScriptSite::OnScriptTerminate
Konak betik yürütme tamamlandığını bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OnScriptTerminate(  
    VARIANT *pvarResult,   // address of script results  
    EXCEPINFO *pexcepinfo  // address of structure with exception information  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pvarResult`  
 [in] Komut dosyası sonucu içeren değişkenin adresini veya `NULL` betik sonuç oluşturduysa.  
  
 `pexcepinfo`  
 [in] Adresi bir `EXCEPINFO` betik sonlandırıldı, oluşturulan özel durum bilgilerini içeren yapısı veya `NULL` hiçbir özel durum oluşturulduysa.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` başarılı olursa.  
  
## <a name="remarks"></a>Açıklamalar  
 Komut dosyası altyapısı çağırmadan önce bu yöntemi çağıran [IActiveScriptSite::OnStateChange](../../winscript/reference/iactivescriptsite-onstatechange.md) yöntemiyle SCRIPTSTATE_INITIALIZED bayrağı ayarlanmış tamamlandı. Bu yöntem, konağa tamamlanma durumunu ve sonuçlarını döndürmek için kullanılabilir. Ana bilgisayar tarafından tanımlanan ömrü olayları konaktan indirme üzerinde alan birçok betik dili gerektiğini unutmayın. Bu durumda, bu yöntem hiçbir zaman çağrılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSite](../../winscript/reference/iactivescriptsite.md)