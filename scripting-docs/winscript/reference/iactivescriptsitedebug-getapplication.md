---
title: IActiveScriptSiteDebug::GetApplication | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSiteDebug.GetApplication
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSiteDebug::GetApplication
ms.assetid: 4400f1b1-3108-4a71-b1f1-43586fe1227c
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 75560ead40809c77e4768f8318d754a512e5d7ba
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992643"
---
# <a name="iactivescriptsitedebuggetapplication"></a>IActiveScriptSiteDebug::GetApplication
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
 [Iactivescriptsitedebug arabirimi](../../winscript/reference/iactivescriptsitedebug-interface.md)   
 [IProcessDebugManager::GetDefaultApplication](../../winscript/reference/iprocessdebugmanager-getdefaultapplication.md)