---
title: IActiveScriptAuthor::GetScriptletTextAttributes | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptAuthor.GetScriptletTextAttributes
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptAuthor::GetScriptletTextAttributes
ms.assetid: 082edfce-6c5b-4e5e-b942-31b423a4fa1d
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: cb8f1b5aac6df8d8659fa323f3f1efcb7721d97f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62955068"
---
# <a name="iactivescriptauthorgetscriptlettextattributes"></a>IActiveScriptAuthor::GetScriptletTextAttributes
Bir kod oluşturma metni özniteliklerini döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetScriptletTextAttributes(  
   LPCOLESTR pszCode,  
   ULONG cch,  
   LPCOLESTR pszDelimiter,  
   DWORD dwFlags,  
   SOURCE_TEXT_ATTR *pattr  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszCode`  
 ['de size_is (`cch`)] kod oluşturma yöntemi metni. Bu dize null sonlandırılmış olmak zorunda değil.  
  
 `cch`  
 [in] İçin kullanılan boyutu `pszCode` ve `pattr` parametreleri.  
  
 `pszDelimiter`  
 [in] Resimli bitiş sınırlayıcısı adresi. Zaman `pszCode` ayrıştırılır metin akışından ana bilgisayar genellikle bir sınırlayıcı (örneğin, iki tek tırnak işareti) ayrıldığında son algılamak için kullanır. Sınırlayıcı scriptlet sonuna tanımlamak için kullanılıyorsa, bu parametre NULL olarak ayarlayın.  
  
 `dwFlags`  
 [in] Kod oluşturma metni özniteliklerle ilişkili bayraklar. Aşağıdaki değerlerin bir birleşimi olabilir.  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|GETATTRTYPE_DEPSCAN|0x0001|SOURCETEXT_ATTR_IDENTIFIER özniteliğine sahip tanımlayıcılar tanımlamak ve SOURCETEXT_ATTR_MEMBERLOOKUP özniteliğine sahip bir nokta işleçleri tanımlayın.|  
|GETATTRFLAG_THIS|0x0100|SOURCETEXT_ATTR_THIS özniteliğine sahip geçerli bir nesneyi tanımlar.|  
|GETATTRFLAG_HUMANTEXT|0x8000|SOURCETEXT_ATTR_HUMANTEXT özniteliğine sahip dizesi içerik ve yorum metnini tanımlayın.|  
  
 `pattr`  
 [out içinde size_is (`cch`)] kod oluşturma kodu için renk bilgisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptauthor arabirimi](../../winscript/reference/iactivescriptauthor-interface.md)   
 [IActiveScriptAuthor::GetScriptTextAttributes](../../winscript/reference/iactivescriptauthor-getscripttextattributes.md)   
 [SOURCE_TEXT_ATTR Sabit Listesi](../../winscript/reference/source-text-attr-enumeration.md)