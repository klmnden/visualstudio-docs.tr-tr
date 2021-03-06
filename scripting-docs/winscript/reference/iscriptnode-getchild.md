---
title: IScriptNode::GetChild | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptNode.GetChild
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptNode::GetChild
ms.assetid: 8cb3f8b0-958b-40bb-a91a-49a788661861
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 78b5c84c6ed9b3de9593f0d6ff02df93a0e9ba77
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62787136"
---
# <a name="iscriptnodegetchild"></a>IScriptNode::GetChild
Belirtilen dizin düğümünde en alt öğesini döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetChild(  
   ULONG              isn,  
   IScriptNode        **ppsn  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `isn`  
 [in] Üst alt dizini.  
  
 `ppsn`  
 [out] Bir işaretçiye alan değişkenin adresini `IScriptNode` alt örneğinin arabirimi.  
  
 İçin `IScriptNode` bir Web sayfasını temsil eden nesneleri, bu parametre bir betik bloğu içeren bir nesne döndürür.  
  
 İçin `IScriptEntry` belirten bir betik bloğu nesneler bu parametre, bir işlevi belirtir bir nesne döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 İçin `IScriptEntry` bir işlev nesnesi belirtin nesneleri ve `IScriptScriptlet` nesneler, bu yöntem başarısız olmadığı için alt giriş yok.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IScriptNode Arabirimi](../../winscript/reference/iscriptnode-interface.md)