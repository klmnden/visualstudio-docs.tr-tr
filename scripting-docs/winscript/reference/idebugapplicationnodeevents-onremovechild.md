---
title: IDebugApplicationNodeEvents::onRemoveChild | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplicationNodeEvents.onRemoveChild
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugApplicationNodeEvents::onRemoveChild
ms.assetid: 2e025d29-b8c0-4793-a2d3-c20d548d6386
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8e59624e5ec6659e0fea3d55fdaddf7949eac18f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62822171"
---
# <a name="idebugapplicationnodeeventsonremovechild"></a>IDebugApplicationNodeEvents::onRemoveChild
Hata ayıklama uygulama düğüm nesnesinden bir alt düğüm kaldırıldığında olayını işler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT onRemoveChild(  
   IDebugApplicationNode*  prddpChild  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `prddpChild`  
 [in] Kaldırılan alt uygulama düğümü.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, hata ayıklama uygulama düğüm nesnesinden bir alt düğüm kaldırıldığında olayını işler.  
  
 Uygulayıcılar, `IDebugApplicationNode` arabirimi bu olay Yükselt.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplicationnodeevents arabirimi](../../winscript/reference/idebugapplicationnodeevents-interface.md)   
 [IDebugApplicationNodeEvents::onAddChild](../../winscript/reference/idebugapplicationnodeevents-onaddchild.md)   
 [IDebugApplicationNode Arabirimi](../../winscript/reference/idebugapplicationnode-interface.md)