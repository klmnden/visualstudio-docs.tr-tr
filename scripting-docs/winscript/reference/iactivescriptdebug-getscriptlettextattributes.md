---
title: IActiveScriptDebug::GetScriptletTextAttributes | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptDebug.GetScriptletTextAttributes
apilocation:
- jscript.dll
helpviewer_keywords:
- IActiveScriptDebug::GetScriptletTextAttributes
ms.assetid: b3990d86-5fdf-4c9f-9678-3f4b808c7ca8
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 781282b5c825954ada4fbb35daa2a97b379c3f13
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157600"
---
# <a name="iactivescriptdebuggetscriptlettextattributes"></a>IActiveScriptDebug::GetScriptletTextAttributes
Rastgele bir kod oluşturma için metin öznitelikleri döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetScriptletTextAttributes(  
   LPCOLESTR          pstrCode,  
   ULONG              uNumCodeChars,  
   LPCOLESTR          pstrDelimiter,  
   DWORD              dwFlags,  
   SOURCE_TEXT_ATTR*  pattr  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrCode`  
 [in] Kod oluşturma yöntemi metni. Bu dize null sonlandırılmış olması gerekmez.  
  
 `uNumCodeChars`  
 [in] Kod oluşturma yöntemi metni karakter sayısı.  
  
 `pstrDelimiter`  
 [in] Resimli bitiş sınırlayıcısı adresi. Zaman `pstrCode` ayrıştırılır metin akışından ayrıldığında son algılamak için tırnak işaretleri ("), iki tek gibi ana bilgisayar genellikle bir ayırıcı kullanır. Bu parametre, bazı koşullu ilkel bir ön işleme sağlamak komut dosyası altyapısı verme konak kullanılan sınırlayıcıyı belirtir (örneğin, tek tırnak işaretini ['] ayırıcı olarak kullanılacak iki tek tırnak işaretleri yerine). Tam olarak nasıl (ve ise) bu bilgileri komut dosyası altyapısına bağlıdır komut dosyası altyapısı kullanır. Ana bilgisayar kod oluşturma sonunu işaretlemek için sınırlayıcı kullanmadıysanız, bu parametre NULL olarak ayarlayın.  
  
 `dwFlags`  
 [in] Kod oluşturma yöntemiyle ilişkili bayraklar. Bu değerleri bir birleşimi olabilir:  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|GETATTRTYPE_DEPSCAN|0x0001|Tanımlayıcıları ve nokta işleçleri SOURCETEXT_ATTR_IDENTIFIER ve SOURCETEXT_ATTR_MEMBERLOOKUP bayraklarıyla sırasıyla tanımlanacağını belirtir.|  
|GETATTRFLAG_THIS|0x0100|Geçerli nesne tanımlayıcısı SOURCETEXT_ATTR_THIS bayrağıyla tanımlanması gerektiğini gösterir.|  
|GETATTRFLAG_HUMANTEXT|0x8000|Dize içerik ve açıklama metni SOURCETEXT_ATTR_HUMANTEXT bayrağıyla tanımlanması gerektiğini gösterir.|  
  
 `pattr`  
 [out içinde] Döndürülen öznitelikleri içeren arabellek.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Uygulayan bir akıllı ana bilgisayar `IDebugDocumentText` arabirimi çağrıları için temsilci seçmek için bu yöntemi kullanabilirsiniz `IDebugDocumentText::GetText` yöntemi.  
  
 Kod parçacıklarını ifadeleri olma eğilimindedir ve bir betik bloğu değerinden farklı bir sözdizimi olabilir çünkü bu çağrı sağlanır. Bunlar aynı sözdizimini varsa, bu yöntemin uygulanmasını uygulanması için aynı `GetScriptTextAttributes` yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptdebug arabirimi](../../winscript/reference/iactivescriptdebug-interface.md)   
 [IActiveScriptDebug::GetScriptTextAttributes](../../winscript/reference/iactivescriptdebug-getscripttextattributes.md)   
 [Idebugdocumenttext arabirimi](../../winscript/reference/idebugdocumenttext-interface.md)   
 [IDebugDocumentText::GetText](../../winscript/reference/idebugdocumenttext-gettext.md)   
 [SOURCE_TEXT_ATTR Sabit Listesi](../../winscript/reference/source-text-attr-enumeration.md)