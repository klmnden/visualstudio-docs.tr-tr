---
title: IProcessDebugManager::AddApplication | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IProcessDebugManager.AddApplication
apilocation:
- pdm.dll
helpviewer_keywords:
- IProcessDebugManager::AddApplication
ms.assetid: 73828299-11eb-4c58-ad70-f80f2d0eede8
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 206baa92ae8d2803b2b07f4966565755a1785d61
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62944981"
---
# <a name="iprocessdebugmanageraddapplication"></a>IProcessDebugManager::AddApplication
Çalışan uygulamalar bir uygulama makinesi ayıklama manager'ın listesine ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT AddApplication(  
   IDebugApplication*  pda,  
   DWORD*              pdwAppCookie  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pda`  
 [in] Çalışan uygulamalar listesine eklemek için hata ayıklama uygulama.  
  
 `pdwAppCookie`  
 [out] Uygulamayı hata ayıklama Makine Yöneticisi'nden kaldırmak için kullanılan tanımlama bilgisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, çalışan bir uygulama ekler Makine Hata Ayıklama Yöneticisi'nde uygulama listesi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iprocessdebugmanager arabirimi](../../winscript/reference/iprocessdebugmanager-interface.md)   
 [IProcessDebugManager::RemoveApplication](../../winscript/reference/iprocessdebugmanager-removeapplication.md)