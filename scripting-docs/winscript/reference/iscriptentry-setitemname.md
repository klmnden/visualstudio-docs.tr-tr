---
title: IScriptEntry::SetItemName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 20af0975a4175d10b110ac5e3cef9e0055f4ce1b
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097766"
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