---
title: IDebugApplication::SetName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.SetName
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::SetName
ms.assetid: 7b0ddc58-6f20-4ce3-9bdf-81a6c1d64256
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4ac0b253d5193fc507e2d74a2d9dbcdd893e9fdb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62990758"
---
# <a name="idebugapplicationsetname"></a>IDebugApplication::SetName
Uygulama adını ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetName(  
   LPCOLESTR  pstrName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrName`  
 [in] Uygulamanın adı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem için sağlanan adı yapılan sonraki çağrılar döndürülür `IRemoteDebugApplication::GetName` yöntemi.  
  
 Bu yöntemi çağırmadan önce çağrılmalıdır `IProcessDebugManager::AddApplication` yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplication arabirimi](../../winscript/reference/idebugapplication-interface.md)   
 [IProcessDebugManager::AddApplication](../../winscript/reference/iprocessdebugmanager-addapplication.md)