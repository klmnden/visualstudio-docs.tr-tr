---
title: IDebugDocumentHost::GetScriptTextAttributes | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHost.GetScriptTextAttributes
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugDocumentHost::GetScriptTextAttributes
ms.assetid: fe459d0d-937f-4176-be81-99d5cca121a1
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6a5e56468e51f6d90e37e90c885b6b9df48d5f6e
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58159003"
---
# <a name="idebugdocumenthostgetscripttextattributes"></a>IDebugDocumentHost::GetScriptTextAttributes
Belge metin bloğu için metin öznitelikleri döndürür.  
  
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
|`E_NOTIMPL`|Konak, yalnızca varsayılan öznitelikleri kullanır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, rastgele bir belgede metin bloğu için metin öznitelikleri döndürür. Döndürülecek konakları için kabul edilebilir `E_NOTIMPL`, bu durumda varsayılan öznitelikler kullanılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugdocumenthost arabirimi](../../winscript/reference/idebugdocumenthost-interface.md)   
 [SOURCE_TEXT_ATTR Sabit Listesi](../../winscript/reference/source-text-attr-enumeration.md)