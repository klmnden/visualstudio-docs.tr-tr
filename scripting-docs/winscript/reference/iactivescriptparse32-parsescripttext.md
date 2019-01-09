---
title: IActiveScriptParse32::ParseScriptText | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f33e454c-69d8-4cab-9150-d1e7fd04786d
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
ms.openlocfilehash: 782c1d7bd2dd4c0708418ffd3e69c339dd993fde
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54094607"
---
# <a name="iactivescriptparse32parsescripttext"></a>IActiveScriptParse32::ParseScriptText
Verilen kod scriptlet ad alanına bildirimler ekleyerek ve kodu uygun şekilde değerlendirerek ayrıştırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT ParseScriptText(  
    LPCOLESTR pstrCode,              // address of scriptlet text  
    LPCOLESTR pstrItemName,          // address of item name  
    IUnknown *punkContext,           // address of debugging context  
    LPCOLESTR pstrDelimiter,         // address of end-of-scriptlet delimiter  
    DWORD_PTR dwSourceContextCookie, // cookie for debugging  
    ULONG ulStartingLineNumber,      // starting line of the script  
    DWORD dwFlags,                   // scriptlet flags  
    VARIANT *pvarResult,             // address of buffer for results  
    EXCEPINFO *pexcepinfo            // address of buffer for error data  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
  
|||  
|-|-|  
|`pstrCode`|[in] Değerlendirilecek kod oluşturma yöntemi metni adresi. Bu dizenin yorumu komut dosyası diline bağlıdır.|  
|`pstrItemName`|[in] Değerlendirilecek kod oluşturma olan bağlamı veren öğe adı adresi. Bu parametre NULL ise, kod genel komut dosyası altyapısının bağlamında değerlendirilir.|  
|`punkContext`|[in] Bağlam nesnesi adresi. Bu nesne, böyle bir içeriğin etkin bir çalışma zamanı içeriğini temsil etmek üzere hata ayıklayıcı tarafından sağlanabilir burada bir hata ayıklama ortamında kullanım için ayrılmıştır. Bu parametre NULL ise altyapısı kullanan `pstrItemName` içeriği tanımlamak için.|  
|`pstrDelimiter`|[in] Resimli bitiş sınırlayıcısı adresi. Zaman `pstrCode` ayrıştırılır metin akışından ayrıldığında son algılamak için tırnak işaretleri ("), iki tek gibi ana bilgisayar genellikle bir ayırıcı kullanır. Bu parametre, bazı koşullu ilkel bir ön işleme sağlamak komut dosyası altyapısı verme konak kullanılan sınırlayıcıyı belirtir (örneğin, tek tırnak işaretini ['] ayırıcı olarak kullanılacak iki tek tırnak işaretleri yerine). Tam olarak nasıl (ve ise) bu bilgilerin kullanılması, komut dosyası altyapısına bağlıdır kullanmayacağı. Bu parametre kümesine `NULL` ana bilgisayar kod oluşturma sonunu işaretlemek için sınırlayıcı kullanmadıysanız.|  
|`dwSourceContextCookie`|[in] Hata ayıklama amacıyla kullanılan tanımlama bilgisi.|  
|`ulStartingLineNumber`|[in] Hangi satır ayrıştırmaya başlanacağını belirleyen sıfır tabanlı değer.|  
|`dwFlags`|[in] Kod oluşturma yöntemiyle ilişkili bayraklar. Bu değerleri bir birleşimi olabilir:|  
  
|Değer|Açıklama|  
|-----------|-------------|  
|SCRIPTTEXT_ISEXPRESSION|Bir hesaplama ifadesi ve bir deyim arasındaki fark önemli, ancak komut dosyası dili sözdizimi kurallarına göre belirsiz ise, bu bayrak scriptlet bir deyimi veya deyimlerinin listesi olarak değil bir ifade olarak yorumlanacağını belirtir. Kod oluşturma metni sözdiziminden, doğru seçimi belirlenebilir sürece varsayılan olarak deyimler kabul edilir.|  
|SCRIPTTEXT_ISPERSISTENT|Komut dosyası altyapısı kaydedilirse, bu çağrı sırasında eklenen kodu kaydedilmesi gerektiğini belirtir (örneğin, bir çağrı yoluyla `IPersist*::Save`), veya komut dosyası altyapısı başlatılmış durumuna geçiş yoluyla sıfırlanır.|  
|SCRIPTTEXT_ISVISIBLE|Komut metni görünür olması gerektiğini belirtir (ve bu nedenle, çağrılabilmesini) komut dosyası ad alanında genel bir yöntem olarak.|  
  
|||  
|-|-|  
|`pvarResult`|[out] Kod oluşturma işlemi sonuçlarını alan arabellek adresi veya `NULL` çağıran hiçbir sonuç beklemiyorsa (yani, scrıpttext_ısexpressıon değeri ayarlanmaz).|  
|`pexcepinfo`|[out] Özel durum bilgileri alan bir yapının adresi. Bu yapı doldurulur `IActiveScriptParse::ParseScriptText` DISP_E_EXCEPTION döndürürse.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`DISP_E_EXCEPTION`|Kod oluşturma işlemede bir özel durum oluştu. `pexcepinfo` Parametre özel durum hakkında bilgi içerir.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_NOTIMPL`|Bu yöntem desteklenmiyor. Komut dosyası altyapısı çalışma zamanı değerlendirmesini deyimlerde ya da ifadelerde desteklemez.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı başlatılmamış veya kapatılmış durumdadır ya da scrıpttext_ısexpressıon bayrağı ayarlanmıştır ve komut dosyası altyapısı başlatılmış durumdadır).|  
|`OLESCRIPT_E_SYNTAX`|Kod oluşturma yönteminde belirtilmeyen sözdizimi hatası oluştu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Komut dosyası motoru başlatılmış durumdaysa bu çağrı sırasında gerçekte kod değerlendirilir; Bunun yerine, bu tür bir kod kuyruğa alınır ve komut dosyası altyapısı içinde (veya aracılığıyla) geçirildiğinde yürütülen başlatılmış durumda. Başlatılan durumda yürütülmesine izin verilmediğinden bu yöntemi scrıpttext_ısexpressıon bayrağıyla başlatılmış bir durumda olduğunda çağırmak için bir hata var.  
  
 Kod oluşturma yöntemi, bir ifade, deyimlerin listesini veya komut dosyası dili tarafından izin verilen herhangi bir şey olabilir. Örneğin, bu yöntem HTML veriyi değerlendirmede kullanılan \<BETİK > etiketini bunları komut satırı durumuna yalnızca derlenmesi yerine HTML sayfası oluşturulmuyor olarak yürütülmesini sağlar.  
  
 Bu yönteme geçirilen kod, geçerli ve tam bir kod bölümünü olması gerekir. Örneğin, VBScript içinde bu yöntemi Sub Function(x) ile bir ve daha sonra ile ikinci defa çağırmak geçersizdir `End Sub`. Ayrıştırıcı ikinci çağrının alt yordamı tamamlamak için bekleyeceği değil, ancak bir alt yordam bildirimi başlatılmış ancak tamamlanmamış nedeniyle yerine bir ayrıştırma hatası oluşturmalıdır.  
  
 Komut dosyası motoru durumu bölümü, komut dosyası durumları hakkında daha fazla bilgi için bkz. [Windows betik motorları](../../winscript/windows-script-engines.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptParse32](../../winscript/reference/iactivescriptparse32.md)