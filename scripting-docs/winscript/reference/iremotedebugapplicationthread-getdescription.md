---
title: IRemoteDebugApplicationThread::GetDescription | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IRemoteDebugApplicationThread.GetDescription
apilocation:
- pdm.dll
helpviewer_keywords:
- IRemoteDebugApplicationThread::GetDescription
ms.assetid: 69842e9e-7c1c-4841-a6b2-31505fe85738
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c60e12eef269da46aea317611cb06223d0811ddc
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62788202"
---
# <a name="iremotedebugapplicationthreadgetdescription"></a>IRemoteDebugApplicationThread::GetDescription
Açıklama ve bu iş parçacığı durumunu alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetDescription(  
   BSTR*  pbstrDescription,  
   BSTR*  pbstrState  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pbstrDescription`  
 [out] Bu iş parçacığının açıklaması.  
  
 `pbstrState`  
 [out] İş parçacığı durumu açıklaması.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, açıklama ve bu iş parçacığı durumunu alır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IRemoteDebugApplicationThread Arabirimi](../../winscript/reference/iremotedebugapplicationthread-interface.md)