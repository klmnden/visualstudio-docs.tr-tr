---
title: IScriptNode::GetParent | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptNode.GetParent
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptNode::GetParent
ms.assetid: 0fb813f6-ab94-46b2-b0cf-ef5d1cd38ae4
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1c990b5ba5c3d03d319e0eeced282c92cfbb5281
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58151017"
---
# <a name="iscriptnodegetparent"></a>IScriptNode::GetParent
Döndürür `IScriptNode` bir nesnenin üst nesnesi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetParent(  
   IScriptNode       **ppsnParent  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppsnParent`  
 [out] Bir işaretçiye alan değişkenin adresini `IScriptNode` üst örneğinin arabirimi.  
  
 Sınıf uyguluyorsa `IScriptEntry` veya `IScriptScriptlet`e `IScriptNode` nesne döndürülür.  
  
 Sınıf uyguluyorsa `IScriptNode` (temsil eden bir Web sayfası), NULL döndürülür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IScriptNode Arabirimi](../../winscript/reference/iscriptnode-interface.md)