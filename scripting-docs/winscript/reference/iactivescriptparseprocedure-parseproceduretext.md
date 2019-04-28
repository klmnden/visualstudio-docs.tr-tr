---
title: IActiveScriptParseProcedure::ParseProcedureText | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptParseProcedure.ParseProcedureText
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptParseProcedure_ParseProcedureText
ms.assetid: 345a74ae-b4e8-42b2-abd8-633a370e8e7f
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 98425d12c53c61cb3f7557d1243cc757c326a89a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62954914"
---
# <a name="iactivescriptparseprocedureparseproceduretext"></a>IActiveScriptParseProcedure::ParseProcedureText
Verilen kod yordamı ayrıştırır ve yordamı ad alanına ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT ParseProcedureText(  
    LPCOLESTR pstrCode,              // address of procedure text  
    LPCOLESTR pstrFormalParams,      // address of formal parameter names  
    LPCOLESTR pstrProcedureName,     // address of procedure name  
    LPCOLESTR pstrItemName,          // address of item name  
    IUnknown *punkContext,           // address of debugging context  
    LPCOLESTR pstrDelimiter,         // address of end-of-procedure delimiter  
    DWORD_PTR dwSourceContextCookie, // application-defined value for debugging  
    ULONG ulStartingLineNumber,      // starting line of the script  
    DWORD dwFlags,                   // procedure flags  
    IDispatch **ppdisp               // receives IDispatch pointer  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrCode`  
 [in] Değerlendirilecek yordamı metni adresi. Bu dizenin yorumu komut dosyası diline bağlıdır.  
  
 `pstrFormalParams`  
 [in] Yordam için biçimsel parametre adları adresi. Parametre adları, komut dosyası altyapısı için uygun sınırlayıcılar ile ayrılmalıdır. Adlar parantez içine alınmalıdır değil.  
  
 `pstrProcedureName`  
 [in] Ayrıştırılacak yordam adı adresi.  
  
 `pstrItemName`  
 [in] Yordamı değerlendirilecek bağlamı veren öğe adı adresi. Bu parametre `NULL`, kod genel komut dosyası altyapısının bağlamında değerlendirilir.  
  
 `punkContext`  
 [in] Bağlam nesnesi adresi. Bu nesne, böyle bir içeriğin etkin bir çalışma zamanı içeriğini temsil etmek üzere hata ayıklayıcı tarafından sağlanabilir burada bir hata ayıklama ortamında kullanım için ayrılmıştır. Bu parametre `NULL`, altyapısını kullanan `pstrItemName` içeriği tanımlamak için.  
  
 `pstrDelimiter`  
 [in] Yordam bitiş sınırlayıcısı adresi. Zaman `pstrCode` ayrıştırılır metin akışından gibi iki yordamı sonuna algılamak için tırnak işaretleri ("), tek bir ana bilgisayar genellikle bir ayırıcı kullanır. Bu parametre, bazı koşullu ilkel bir ön işleme sağlamak komut dosyası altyapısı verme konak kullanılan sınırlayıcıyı belirtir (örneğin, tek tırnak işaretini ['] ayırıcı olarak kullanılacak iki tek tırnak işaretleri yerine). Tam olarak nasıl (ve ise) bu bilgilerin kullanılması, komut dosyası altyapısına bağlıdır kullanmayacağı. Bu parametre kümesine `NULL` konak yordamı sonunu işaretlemek için sınırlayıcı kullanmadıysanız.  
  
 `dwSourceContextCookie`  
 [in] Hata ayıklama amacıyla kullanılan uygulama tanımlı değer.  
  
 `ulStartingLineNumber`  
 [in] Hangi satır ayrıştırmaya başlanacağını belirleyen sıfır tabanlı değer.  
  
 `dwFlags`  
 [in] Yordamı ile ilişkili bayraklar. Bu değerleri bir birleşimi olabilir:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|SCRIPTPROC_ISEXPRESSION|Bildiren kodda `pstrCode` yordamın dönüş değerini temsil eden bir ifadedir. Varsayılan olarak, bir ifade, deyimlerin listesini veya başka bir yordamda komut dosyası dili tarafından izin verilen herhangi bir şey kod içerebilir.|  
|SCRIPTPROC_IMPLICIT_THIS|Bildiren `this` işaretçi yordamı kapsamında yer almaktadır.|  
|SCRIPTPROC_IMPLICIT_PARENTS|Belirten üst öğelerinin `this` işaretçi yordamı kapsamında dahil edilir.|  
  
 `ppdisp`  
 [out] Betiğin genel yöntemleri ve özellikleri içeren bir nesne için işaretçi adresi. Komut dosyası altyapısı böyle bir nesnenin desteklemiyorsa `NULL` döndürülür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_NOTIMPL`|Bu yöntem desteklenmiyor. Komut dosyası altyapısı çalışma zamanı yordamları ad alanına eklenmesini desteklemez.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı başlatılmamış veya kapatılmış durumdadır).|  
|`OLESCRIPT_E_SYNTAX`|Yordamda belirtilmeyen sözdizimi hatası oluştu.|  
|`S_FALSE`|Komut dosyası altyapısı, dağıtım nesnesi desteklemiyor; `ppdisp` parametrenin ayarlanmış `NULL`.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu çağrı sırasında hiçbir betik kodu değerlendirilir; Bunun yerine, yordam, burada, komut dosyası tarafından daha sonra çağrılabilir komut satırı durumuna derlenir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptParseProcedure](../../winscript/reference/iactivescriptparseprocedure.md)