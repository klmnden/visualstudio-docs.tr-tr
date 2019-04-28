---
title: IActiveScriptSiteDebug32::GetApplication | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 533d770d-06a4-4693-873e-255c9c6f0df0
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
ms.openlocfilehash: c71e33445db7745f71e374c586d079a9665776b2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992489"
---
# <a name="iactivescriptsitedebug32getapplication"></a>IActiveScriptSiteDebug32::GetApplication
Bu betik sitesiyle ilişkili hata ayıklama uygulama nesnesi döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetApplication(  
   IDebugApplication**  ppda  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppda`  
 [out] Betik site ile ilişkili hata ayıklama uygulama nesnesi için işaretçi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_NOTIMPL`|Hata ayıklama konağı doğrudan desteklemez.|  
  
## <a name="remarks"></a>Açıklamalar  
 `GetApplication` Yöntemi ait olduğu her betik uygulama nesnesi tanımlamak bir akıllı ana bilgisayar için bir yol sağlar. Komut dosyası motorları içeren uygulamasını almak ve için başvurmadan için bu yöntemi çağıran girişiminde `IProcessDebugManager::GetDefaultApplication` bu başarısız olursa.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptsitedebug32 arabirimi](../../winscript/reference/iactivescriptsitedebug32-interface.md)   
 [IProcessDebugManager::GetDefaultApplication](../../winscript/reference/iprocessdebugmanager-getdefaultapplication.md)