---
title: IScriptEntry::SetItemName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptEntry.SetItemName
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptEntry::SetItemName
ms.assetid: 9551a7ec-38f8-466a-9722-09367763f380
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d25ac4977f1fca44d63767c372db169f8cb61ea6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62787664"
---
# <a name="iscriptentrysetitemname"></a>IScriptEntry::SetItemName
Tanımlayan öğesi adını ayarlar bir `IScriptEntry` nesne.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetItemName(  
   LPCOLESTR          psz  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `psz`  
 [in] Öğe adı içeren bir arabellek adresi. Öğe adı, ana bilgisayar tarafından girişi tanımlamak için kullanılır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_FAIL`|Yöntem başarılı olmadı.|  
  
## <a name="remarks"></a>Açıklamalar  
 İçin `IScriptEntry` nesneleri, bu yöntemi döndürür `S_OK`.  
  
 İçin `IScriptScriptlet` nesneleri (hangi türetilen `IScriptEntry`), bu yöntemi döndürür `E_FAIL`. İçin `IScriptScriptlet` nesneler, öğe adı tarafından belirlenir [IActiveScriptAuthor::AddScriptlet](../../winscript/reference/iactivescriptauthor-addscriptlet.md) ve değiştirilemez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iscriptentry arabirimi](../../winscript/reference/iscriptentry-interface.md)   
 [IScriptEntry::GetItemName](../../winscript/reference/iscriptentry-getitemname.md)