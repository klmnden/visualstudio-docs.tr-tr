---
title: IEnumDebugExpressionContexts::Skip | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IEnumDebugExpressionContexts.Skip
apilocation:
- jscript.dll
helpviewer_keywords:
- IEnumDebugExpressionContexts::Skip
ms.assetid: 3498cbb5-8581-4dcd-b016-e86b049c7831
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5176eb83c4c5bfe517066d8ea7f52b76e121fb26
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62963526"
---
# <a name="ienumdebugexpressioncontextsskip"></a>IEnumDebugExpressionContexts::Skip
Bir numaralandırma sıralı segmentleri belirtilen sayıda atlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Skip(  
   ULONG  celt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `celt`  
 [in] Atlamak için numaralandırma sıralı Segment sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bir numaralandırma sıralı segmentleri belirtilen sayıda atlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumDebugExpressionContexts Arabirimi](../../winscript/reference/ienumdebugexpressioncontexts-interface.md)