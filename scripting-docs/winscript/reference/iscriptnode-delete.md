---
title: IScriptNode::Delete | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptNode.Delete
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptNode::Delete
ms.assetid: 6765ff80-a9a8-40a3-a669-7fcc284c87af
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 41bf932b242865b1deac4c61db400f973bd0b00c
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58145011"
---
# <a name="iscriptnodedelete"></a>IScriptNode::Delete
Bu nesne ağacının siler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Delete();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Sonra `Delete` yöntemi çağrıldığında [IScriptNode::Alive](../../winscript/reference/iscriptnode-alive.md) yöntemini gösterir betik düğüm etkin değil.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IScriptNode Arabirimi](../../winscript/reference/iscriptnode-interface.md)