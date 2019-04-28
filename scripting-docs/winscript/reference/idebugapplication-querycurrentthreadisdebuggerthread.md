---
title: IDebugApplication::QueryCurrentThreadIsDebuggerThread | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.QueryCurrentThreadIsDebuggerThread
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::QueryCurrentThreadIsDebuggerThread
ms.assetid: e22ad8a4-a8be-423d-80f2-28256a7448ed
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2ed53bcdb5e0d613a757c0c60f4791b0c59e3476
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62990812"
---
# <a name="idebugapplicationquerycurrentthreadisdebuggerthread"></a>IDebugApplication::QueryCurrentThreadIsDebuggerThread
Geçerli çalışan iş parçacığı hata ayıklayıcı iş parçacığı olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT QueryCurrentThreadIsDebuggerThread();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu ve geçerli çalışan iş parçacığı hata ayıklayıcı iş parçacığıdır.|  
|`S_FALSE`|Geçerli çalışan iş parçacığı hata ayıklayıcı iş parçacığı değil.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, geçerli çalışan iş parçacığı hata ayıklayıcı iş parçacığı olup olmadığını belirler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplication Arabirimi](../../winscript/reference/idebugapplication-interface.md)