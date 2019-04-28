---
title: IRemoteDebugApplicationThread::GetState | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IRemoteDebugApplicationThread.GetState
apilocation:
- pdm.dll
helpviewer_keywords:
- IRemoteDebugApplicationThread::GetState
ms.assetid: 44503a78-efa9-4fbf-98be-a5dcfa329c5a
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6534f57c92776dcd3cde9083335becbd66002a32
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62788123"
---
# <a name="iremotedebugapplicationthreadgetstate"></a>IRemoteDebugApplicationThread::GetState
Bu iş parçacığı durumunu alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetState(  
   DWORD*  pState  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pState`  
 [out] Aşağıdaki iş parçacığı durumu bayrakların birleşimi:  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|THREAD_STATE_RUNNING|0x00000001|İş parçacığı çalışıyor.|  
|THREAD_STATE_SUSPENDED|0x00000002|İş parçacığını askıya alınır.|  
|THREAD_BLOCKED|0x00000004|İş parçacığı engellenir.|  
|THREAD_OUT_OF_CONTEXT|0x00000008|İçeriğe erişim dışı iş parçacığıdır.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bu iş parçacığı durumunu alır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IRemoteDebugApplicationThread Arabirimi](../../winscript/reference/iremotedebugapplicationthread-interface.md)