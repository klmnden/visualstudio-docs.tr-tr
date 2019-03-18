---
title: IScriptNode::Alive | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptNode.Alive
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptNode::Alive
ms.assetid: d2755c83-e9b9-4c0a-acb7-25b554fc9fe8
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: da0a55d26b5ab643670ba7ed51e576eeb89d8b98
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58159224"
---
# <a name="iscriptnodealive"></a>IScriptNode::Alive
Bir nesne hala etkin olup olmadığını belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Alive();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Betik olarak hala etkin düğümüdür.|  
  
## <a name="remarks"></a>Açıklamalar  
 Nesne etkin değilse, Bileşen Nesne Modeli (COM) sıralama proxy bu yöntem çağrıları için bir hata döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IScriptNode Arabirimi](../../winscript/reference/iscriptnode-interface.md)