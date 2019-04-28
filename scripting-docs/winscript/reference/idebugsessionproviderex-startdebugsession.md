---
title: IDebugSessionProviderEx:StartDebugSession | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugSessionProviderEx:StartDebugSession
apilocation:
- scrobj.dll
ms.assetid: 247337ca-476c-4aa7-8500-d84fd1d98176
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fb120a9acca91014d7b8213a3ed0bd1ab575e118
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62934692"
---
# <a name="idebugsessionproviderexstartdebugsession"></a>IDebugSessionProviderEx:StartDebugSession
Belirtilen uygulama ile bir hata ayıklama oturumu başlatır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT StartDebugSession(  
   IRemoteDebugApplication*  pda  
   BOOL  fQuery  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pda`  
 [in] Hata ayıklama uygulamayı belirtir.  
  
 `fQuery`  
 [in] TRUE, sorgu gösterir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, belirtilen uygulama ile bir hata ayıklama oturumu başlatır. Hata ayıklayıcı çağırmalıdır `IRemoteDebugApplication::ConnectDebugger` bu çağrısından önce.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugsessionproviderex arabirimi](../../winscript/reference/idebugsessionproviderex-interface.md)   
 [IRemoteDebugApplication::ConnectDebugger](../../winscript/reference/iremotedebugapplication-connectdebugger.md)