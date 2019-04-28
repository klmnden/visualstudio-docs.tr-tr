---
title: IDebugApplicationNode::Attach | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplicationNode.Attach
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplicationNode::Attach
ms.assetid: f4aad4ae-5bb0-4b5e-8f70-912a677f8f7a
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c41d06c116c7c15ad308ce2ace837ea01d90ab1d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62990480"
---
# <a name="idebugapplicationnodeattach"></a>IDebugApplicationNode::Attach
Bu uygulama düğümü belirtilen projeyi ağacına ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Attach(  
   IDebugApplicationNode*  pdanParent  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pdanParent`  
 [in] Proje ağacında bu uygulama düğümü eklenecek olduğu.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bu uygulama düğümü projeye ekler. ağaç, kullanarak `pdanParent` üst öğe olarak. Varsa `pdanParent` olduğu `NULL`, bu uygulama düğümü üst düzey düğüm olacaktır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationNode::Detach](../../winscript/reference/idebugapplicationnode-detach.md)   
 [IDebugApplicationNode Arabirimi](../../winscript/reference/idebugapplicationnode-interface.md)