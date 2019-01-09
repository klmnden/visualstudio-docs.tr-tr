---
title: IActiveScriptParseProcedureOld::ParseProcedureText | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptParseProcedureOld.ParseProcedureText
apilocation:
- jscript.dll
helpviewer_keywords:
- IActiveScriptParseProcedureOld::ParseProcedureText
ms.assetid: 21a21313-35ce-432d-b9a6-7999065f19ac
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ec100214a43be6e1faf5e229ce6452432065002b
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54093398"
---
# <a name="iactivescriptparseprocedureoldparseproceduretext"></a>IActiveScriptParseProcedureOld::ParseProcedureText
Verilen kod yordamı ayrıştırır ve ad alanı için anonim bir yordam ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT ParseProcedureText(  
   LPCOLESTR    pstrCode,  
   LPCOLESTR    pstrFormalParams,  
   LPCOLESTR    pstrItemName,  
   IUnknown*    punkContext,  
   LPCOLESTR    pstrDelimiter,  
   DWORD_PTR    dwSourceContextCookie,  
   ULONG        ulStartingLineNumber,  
   DWORD        dwFlags,  
   IDispatch**  ppdisp  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrCode`  
 [in] Değerlendirilecek yordamı metin. Bu dizenin yorumu komut dosyası diline bağlıdır.  
  
 `pstrFormalParams`  
 [in] Yordam için biçimsel parametre adları. Parametre adları, komut dosyası altyapısı için uygun sınırlayıcılar ile ayrılmalıdır. Adlar parantez içine alınmalıdır değil.  
  
 `pstrItemName`  
 [in] Yordamı değerlendirilecek bağlamı veren adlandırılmış öğe adı. Bu parametre `NULL`, kod genel komut dosyası altyapısının bağlamında değerlendirilir.  
  
 `punkContext`  
 [in] Bağlam nesnesi. Bu nesne, böyle bir içeriğin etkin bir çalışma zamanı içeriğini temsil etmek üzere hata ayıklayıcı tarafından sağlanabilir burada bir hata ayıklama ortamında kullanım için ayrılmıştır. Bu parametre `NULL`, altyapısını kullanan `pstrItemName` içeriği tanımlamak için.  
  
 `pstrDelimiter`  
 [in] Yordam bitiş sınırlayıcısı. Zaman `pstrCode` ayrıştırılır metin akışından gibi iki yordamı sonuna algılamak için tırnak işaretleri ("), tek bir ana bilgisayar genellikle bir ayırıcı kullanır. Bu parametre, bazı koşullu sağlamak komut dosyası altyapısı verme konak kullanılan sınırlayıcıyı belirtir (örneğin, tek tırnak işaretini ['] ayırıcı olarak kullanılacak iki tek tırnak işareti ile değiştirerek) temel ön işleme. Tam olarak nasıl (ve ise) bu bilgileri komut dosyası altyapısına bağlıdır komut dosyası altyapısı kullanır. Bu parametre kümesine `NULL` konak yordamı sonunu işaretlemek için sınırlayıcı kullanmadıysanız.  
  
 `dwSourceContextCookie`  
 [in] Hata ayıklama amacıyla kullanılan uygulama tanımlı değer.  
  
 `ulStartingLineNumber`  
 [in] Hangi satırında bir ayrıştırma başlayacak belirleyen sıfır tabanlı değer.  
  
 `dwFlags`  
 [in] Yordamı ile ilişkili bayraklar. Bu değerleri bir birleşimi olabilir.  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-------------|  
|SCRIPTPROC_ISEXPRESSION|0x00000020|Bildiren kodda `pstrCode` yordamın dönüş değerini temsil eden bir ifadedir.|  
|SCRIPTPROC_IMPLICIT_THIS|0x00000100|Bildiren `this` işaretçi yordamı kapsamında yer almaktadır.|  
|SCRIPTPROC_IMPLICIT_PARENTS|0x00000200|Belirten üst öğelerinin `this` işaretçi yordamı kapsamında dahil edilir.|  
  
 `ppdisp`  
 [out] Gönderme sarmalayıcı varsayılan yöntemi ayrıştırıldığında bu yöntem tarafından yordamı olduğu döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_NOTIMPL`|Bu yöntem desteklenmiyor. Komut dosyası altyapısı çalışma zamanı yordamları ad alanına eklenmesini desteklemez.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı başlatılmamış veya kapatılmış durumdadır).|  
|`OLESCRIPT_E_SYNTAX`|Yordamda belirtilmeyen sözdizimi hatası oluştu.|  
|`S_FALSE`|Komut dosyası altyapısı, dağıtım nesnesi desteklemiyor; `ppdisp`parametrenin ayarlanmış `NULL`.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu çağrı sırasında hiçbir betik kodu değerlendirilir; Bunun yerine, yordam bir yönteme üzerinde derlenmiş `ppdisp` burada da çağrılabilir komut dosyası tarafından daha sonra.  
  
 Bu arabirim sunulmasıyla kullanım dışı `IActiveScriptParseProcedure` arabirimi. `IActiveScriptParseProcedure::ParseProcedureText` Yöntemi bu yönteme benzerdir, ancak yordam adı belirtilmesini sağlar. Tüm durumlarda, `IActiveScriptParseProcedure::ParseProcedureText` kullanılmalıdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptparseprocedureold arabirimi](../../winscript/reference/iactivescriptparseprocedureold-interface.md)   
 [IActiveScriptParseProcedure::ParseProcedureText](../../winscript/reference/iactivescriptparseprocedure-parseproceduretext.md)