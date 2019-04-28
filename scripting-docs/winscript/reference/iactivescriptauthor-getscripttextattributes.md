---
title: IActiveScriptAuthor::GetScriptTextAttributes | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptAuthor.GetScriptTextAttributes
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptAuthor::GetScriptTextAttributes
ms.assetid: a53451de-cc5c-4b53-8e5f-81e196364caf
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 75e0d5edf7cf2f83e814036cec56a1b19a89813e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62955126"
---
# <a name="iactivescriptauthorgetscripttextattributes"></a>IActiveScriptAuthor::GetScriptTextAttributes
Bir betik bloğu için metin öznitelikleri döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetScriptTextAttributes(  
    LPCOLESTR        pszCode,  
    ULONG            cch,  
    LPCOLESTR        pszDelimiter,  
    DWORD            dwFlags,  
    SOURCE_TEXT_ATTR *pattr);  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszCode`  
 ['de size_is (`cch`)] komut dosyası bloğu metni. Bu dize null sonlandırılmış olmak zorunda değil.  
  
 `cch`  
 [in] İçin kullanılan boyutu `pszCode` ve `pattr` parametreleri.  
  
 `pszDelimiter`  
 [in] Komut bitiş sınırlayıcısı adresi. Zaman `pszCode` ayrıştırılır metin akışından ana bilgisayar genellikle bir sınırlayıcı (örneğin, iki tek tırnak işareti) ayrıldığında son algılamak için kullanır. Betik bloğunun sonu tanımlamak için sınırlayıcı varsa bu parametre NULL olarak ayarlayın.  
  
 `dwFlags`  
 [in] Betik bloğundaki metin özniteliklerle ilişkili bayraklar. Aşağıdaki değerlerin bir birleşimi olabilir:  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|GETATTRTYPE_DEPSCAN|0x0001|SOURCETEXT_ATTR_IDENTIFIER özniteliğine sahip tanımlayıcılar tanımlamak ve SOURCETEXT_ATTR_MEMBERLOOKUP özniteliğine sahip bir nokta işleçleri tanımlayın.|  
|GETATTRFLAG_THIS|0x0100|SOURCETEXT_ATTR_THIS özniteliğine sahip geçerli bir nesneyi tanımlar.|  
|GETATTRFLAG_HUMANTEXT|0x8000|SOURCETEXT_ATTR_HUMANTEXT özniteliğine sahip dizesi içerik ve yorum metnini tanımlayın.|  
  
 `pattr`  
 [out içinde size_is (`cch`)] komut dosyası bloğu kod için renk bilgisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptauthor arabirimi](../../winscript/reference/iactivescriptauthor-interface.md)   
 [SOURCE_TEXT_ATTR Sabit Listesi](../../winscript/reference/source-text-attr-enumeration.md)