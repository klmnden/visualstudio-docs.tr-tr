---
title: IDebugApplicationThread::SetStateString | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplicationThread.SetStateString
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplicationThread::SetStateString
ms.assetid: a59001d5-ea00-4fd0-bb20-0b592d9c795d
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bf832c14156d0d00f8bc7243537c3cb543019f2c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62822133"
---
# <a name="idebugapplicationthreadsetstatestring"></a>IDebugApplicationThread::SetStateString
İş parçacığı durumu açıklaması ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetStateString(  
   LPCOLESTR  pstrState  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrState`  
 [in] İş parçacığı durumu açıklaması.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem iş parçacığı durumu açıklaması ayarlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationThread Arabirimi](../../winscript/reference/idebugapplicationthread-interface.md)