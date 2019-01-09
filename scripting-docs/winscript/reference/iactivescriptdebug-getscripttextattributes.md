---
title: IActiveScriptDebug::GetScriptTextAttributes | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptDebug.GetScriptTextAttributes
apilocation:
- jscript.dll
helpviewer_keywords:
- IActiveScriptDebug::GetScriptTextAttributes
ms.assetid: 2e8bda34-db0c-4b2e-a17f-82c4e0dbbc8c
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 01218ba46de39dd8351ad82068ca4b34b52b0d46
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097395"
---
# <a name="iactivescriptdebuggetscripttextattributes"></a>IActiveScriptDebug::GetScriptTextAttributes
Rastgele bir betik metin bloğu için metin öznitelikleri döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetScriptTextAttributes(  
   LPCOLESTR          pstrCode,  
   ULONG              uNumCodeChars,  
   LPCOLESTR          pstrDelimiter,  
   DWORD              dwFlags,  
   SOURCE_TEXT_ATTR*  pattr  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrCode`  
 [in] Betik bloğu metin. Bu dize null sonlandırılmış olması gerekmez.  
  
 `uNumCodeChars`  
 [in] Betik bloğu metnindeki karakter sayısı.  
  
 `pstrDelimiter`  
 [in] Sonlandırma, betik bloğu sınırlayıcısı adresi. Zaman `pstrCode` ayrıştırılır metin akışından gibi iki betik bloğunun sonu algılamak için tırnak işaretleri ("), tek bir ana bilgisayar genellikle bir ayırıcı kullanır. Bu parametre, bazı koşullu ilkel bir ön işleme sağlamak komut dosyası altyapısı verme konak kullanılan sınırlayıcıyı belirtir (örneğin, tek tırnak işaretini ['] ayırıcı olarak kullanılacak iki tek tırnak işaretleri yerine). Tam olarak nasıl (ve ise) bu bilgileri komut dosyası altyapısına bağlıdır komut dosyası altyapısı kullanır. Konak, betik bloğunun sonu işaretlemek için sınırlayıcı kullanmadıysanız, bu parametre NULL olarak ayarlayın.  
  
 `dwFlags`  
 [in] Betik bloğu ile ilişkili bayraklar. Bu değerleri bir birleşimi olabilir:  
  
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
  
 Bu yöntem için komut dosyası blokları; `GetScriptletTextAttributes` için kod parçacıklarını yöntemidir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptdebug arabirimi](../../winscript/reference/iactivescriptdebug-interface.md)   
 [IActiveScriptDebug::GetScriptletTextAttributes](../../winscript/reference/iactivescriptdebug-getscriptlettextattributes.md)   
 [Idebugdocumenttext arabirimi](../../winscript/reference/idebugdocumenttext-interface.md)   
 [IDebugDocumentText::GetText](../../winscript/reference/idebugdocumenttext-gettext.md)   
 [SOURCE_TEXT_ATTR Sabit Listesi](../../winscript/reference/source-text-attr-enumeration.md)