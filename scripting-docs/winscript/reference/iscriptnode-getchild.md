---
title: IScriptNode::GetChild | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 55cd6cf5233e850e4109128e322d3fc5bd0b1355
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086599"
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