---
title: IActiveScriptAuthor::GetLanguageFlags | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptAuthor.GetLanguageFlags
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptAuthor::GetLanguageFlags
ms.assetid: eb244452-62f7-4a73-b48f-1aa05cbcc32d
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d9f1a68db05ac0d909108ce77587ae4b071c9a2b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62935477"
---
# <a name="iactivescriptauthorgetlanguageflags"></a>IActiveScriptAuthor::GetLanguageFlags
Dil bilgileri döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetLanguageFlags(  
   DWORD              *pgrfasa  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pgrfasa`  
 [out] Dil bilgileri içeren bayrakları. Aşağıdaki değerlerin bir birleşimi olabilir:  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|fasaPreferInternalHandler|0x0001|Dil altyapısı yerine uygulama yazma betik tarafından betik olay işleyicisi oluşturmayı tercih eder.|  
|fasaSupportInternalHandler|0x0002|Dil altyapısı yazma betiği tarafından oluşturulan betiği olay işleyicileri destekler.|  
|fasaCaseSensitive|0x0004|Büyük küçük harfe duyarlı komut dosyası dilidir.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Uygulamanızın altyapısı yazma betiği olay işleyicileri yönetiyorsa çağırmalıdır `CreateChildHandler` gelen bir `IScriptEntry` nesne. Bu, oluşturur bir `IScriptScriptlet` olay işleyicisine karşılık gelen nesne. Altyapısı, komut girişine de bir olay işleyicisi ekler. Olay işleyicisi belirtilen imza bilgilerini içeren boş bir işlevdir.  
  
 Uygulamanızın olay işleyicileri yönetiyorsa çağırmalıdır `CreateChildHandler` gelen bir `IScriptNode` bir olay işleyicisi scriptlet temsil eden nesne. Bu, oluşturur bir `IScriptScriptlet` olay işleyicisine kod oluşturma yöntemiyle ilişkili nesne. Uygulama, bir olay olarak boş bir işlevi eklemek de sahip mevcut veya yeni bir işleyici `IScriptEntry` nesne.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptAuthor Arabirimi](../../winscript/reference/iactivescriptauthor-interface.md)