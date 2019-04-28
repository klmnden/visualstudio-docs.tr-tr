---
title: IDebugApplicationThread::QueryIsCurrentThread | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplicationThread.QueryIsCurrentThread
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplicationThread::QueryIsCurrentThread
ms.assetid: 1580d3aa-3be8-4779-ac7b-41ab5c9edede
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7d8871d197d662d179fa4d1ed8d420c48ecc5ab3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62974572"
---
# <a name="idebugapplicationthreadqueryiscurrentthread"></a>IDebugApplicationThread::QueryIsCurrentThread
Bu iş parçacığı şu anda çalışan iş parçacığının olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT QueryIsCurrentThread();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu ve şu anda çalışan iş parçacığının budur.|  
|`S_FALSE`|Bu, şu anda çalışan iş parçacığı değildir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bu iş parçacığı şu anda çalışan iş parçacığının olup olmadığını belirler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationThread Arabirimi](../../winscript/reference/idebugapplicationthread-interface.md)