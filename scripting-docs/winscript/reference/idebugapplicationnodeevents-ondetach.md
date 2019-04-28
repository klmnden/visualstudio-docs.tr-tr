---
title: IDebugApplicationNodeEvents::onDetach | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplicationNodeEvents.onDetach
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugApplicationNodeEvents::onDetach
ms.assetid: ef0cbe40-8c52-4bc9-bed0-9fc508abec6e
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9162175727d439a6370071a5f3c9fa4c7ca88ee5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62945686"
---
# <a name="idebugapplicationnodeeventsondetach"></a>IDebugApplicationNodeEvents::onDetach
Hata ayıklama uygulama düğüm nesnesi bir üst düğümden kullanımdan çıkarılmamış gösteren bir olayını işler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT onDetach();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, hata ayıklama uygulama düğüm nesnesi bir üst düğümden kullanımdan çıkarılmamış gösteren bir olayını işler.  
  
 Uygulayıcılar, `IDebugApplicationNode` arabirimi bu olay Yükselt.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplicationnodeevents arabirimi](../../winscript/reference/idebugapplicationnodeevents-interface.md)   
 [IDebugApplicationNodeEvents::onAttach](../../winscript/reference/idebugapplicationnodeevents-onattach.md)   
 [IDebugApplicationNode Arabirimi](../../winscript/reference/idebugapplicationnode-interface.md)