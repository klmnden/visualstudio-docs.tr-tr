---
title: IActiveScriptAuthorProcedure::ParseProcedureText | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptAuthorProcedure.ParseProcedureText
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptAuthorProcedure::ParseProcedureText
ms.assetid: cb6c29c5-c749-48d7-a6a8-ccbf0f9119ec
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c513b105a483d0f80510dff9c91fa2c3f09e0523
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62955165"
---
# <a name="iactivescriptauthorprocedureparseproceduretext"></a>IActiveScriptAuthorProcedure::ParseProcedureText
Bir kod yordam ayrıştırır, komut dosyası altyapısı yazma kod yordam metin ekler ve oluşturur bir `IScriptEntry` kod yordama karşılık gelen nesne.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT ParseProcedureText(  
   LPCOLESTR   pszCode,  
   LPCOLESTR   pszFormalParams,  
   LPCOLESTR   pszProcedureName,  
   LPCOLESTR   pszItemName,  
   LPCOLESTR   pszDelimiter,  
   DWORD       dwCookie,  
   DWORD       dwFlags,  
   IDispatch   *pdispFor  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszCode`  
 [in] Ayrıştırılacak komut metni.  
  
 `pszFormalParams`  
 [in] Yordam için biçimsel parametre adları adresi. Parametre adları, komut dosyası altyapısı geliştirme için uygun sınırlayıcılar tarafından ayrılmalıdır. Adlar parantez içine alınmalıdır değil.  
  
 `pszProcedureName`  
 [in] Ayrıştırılacak yordam adı adresi.  
  
 `pszItemName`  
 [in] Öğe adı içeren arabellek adresi ile ilişkili `IScriptEntry` nesne.  
  
 `pszDelimiter`  
 [in] Sonlandırma, betik bloğu sınırlayıcısı adresi. Zaman `pszCode` ayrıştırılır metin akışından ana bilgisayar genellikle bir sınırlayıcı (örneğin, iki tek tırnak işareti) betik bloğunun sonu algılamak için kullanır. Betik bloğunun sonunu işaretlemek için sınırlayıcı varsa bu parametre NULL olarak ayarlayın.  
  
 `dwCookie`  
 [in] Yeni ile ilişkili uygulama tanımlı bir değer `IScriptEntry` nesne.  
  
 `dwFlags`  
 [in] Kullanılmıyor.  
  
 `pdispFor`  
 [in] Kullanılmıyor.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Geçerli [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] altyapısı, bu yöntem uygulamıyor.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptAuthorProcedure Arabirimi](../../winscript/reference/iactivescriptauthorprocedure-interface.md)