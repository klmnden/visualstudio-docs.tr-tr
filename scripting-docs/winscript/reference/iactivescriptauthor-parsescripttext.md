---
title: IActiveScriptAuthor::ParseScriptText | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptAuthor.ParseScriptText
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptAuthor::ParseScriptText
ms.assetid: ebe212e8-6789-423d-ad22-92be984dc7ad
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fe6870f3b19c5727fdbea0418b8373b990cb671a
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58144725"
---
# <a name="iactivescriptauthorparsescripttext"></a>IActiveScriptAuthor::ParseScriptText
Betik metin ayrıştırır, komut dosyası altyapısı yazma metin ekler ve oluşturur bir `IScriptEntry` betik bloğu için karşılık gelen nesne.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT ParseScriptText(  
   LPCOLESTR pszCode,  
   LPCOLESTR pszItemName,  
   LPCOLESTR pszDelimiter,  
   DWORD dwCookie,  
   DWORD dwFlags  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszCode`  
 [in] Ayrıştırılacak komut metni.  
  
 `pszItemName`  
 [in] Betik bloğu ile ilişkili öğe adı içeren arabellek adresi.  
  
 `pszDelimiter`  
 [in] Sonlandırma, betik bloğu sınırlayıcısı adresi. Zaman `pszCode` ayrıştırılır metin akışından ana bilgisayar genellikle bir sınırlayıcı (örneğin, iki tek tırnak işareti) betik bloğunun sonu algılamak için kullanır. Betik bloğunun sonu tanımlamak için sınırlayıcı varsa bu parametre NULL olarak ayarlayın.  
  
 `dwCookie`  
 [in] Yeni ile ilişkili uygulama tanımlı bir değer `IScriptEntry` nesne.  
  
 `dwFlags`  
 [in] Kullanılmıyor.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptAuthor Arabirimi](../../winscript/reference/iactivescriptauthor-interface.md)