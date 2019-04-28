---
title: IActiveScriptAuthor::GetRoot | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptAuthor.GetRoot
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptAuthor::GetRoot
ms.assetid: 8e55a0c0-dd35-43d5-bf6f-e2f59c1e88d1
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6cdb3246ccae2eabb34696162f67e82a60374550
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62955113"
---
# <a name="iactivescriptauthorgetroot"></a>IActiveScriptAuthor::GetRoot
Döndürür `IScriptNode` yazarın betiği ağacının kökü.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetRoot(  
   IScriptNode        **ppsp  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppsp`  
 [out] Bir işaretçiye alan değişkenin adresini `IScriptNode` arabirimi kök düğüm.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptauthor arabirimi](../../winscript/reference/iactivescriptauthor-interface.md)   
 [IScriptNode Arabirimi](../../winscript/reference/iscriptnode-interface.md)