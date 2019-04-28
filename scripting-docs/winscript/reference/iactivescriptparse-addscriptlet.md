---
title: IActiveScriptParse::AddScriptlet | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptParse.AddScriptlet
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptParse_AddScriptlet
ms.assetid: 824929f4-4dd3-473a-92d9-0b96acea2f14
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ee5d76060789118e9051c2d8dcc5fc570617f6a8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62954960"
---
# <a name="iactivescriptparseaddscriptlet"></a>IActiveScriptParse::AddScriptlet
Kod oluşturma yöntemini komut dosyasına ekler. Bu yöntem, burada betik kalıcı durumunu, konak belgeyle birbirine ve ana betik döndürmekten sorumludur ortamlarda kullanılır yerine ile bir `IPersist*` arabirimi. Kod parçacıklarını iç olayları eklenmesi HTML belgesinde gömülü kod izin HTML komut dosyası dilleri birincil örnekler (örneğin, ONCLICK="button1.text='Exit'").  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT AddScriptlet(  
    LPCOLESTR pstrDefaultName,       // address of default name of scriptlet  
    LPCOLESTR pstrCode,              // address of scriptlet text  
    LPCOLESTR pstrItemName,          // address of item name  
    LPCOLESTR pstrSubItemName,       // address of subitem name  
    LPCOLESTR pstrEventName,         // address of event name  
    LPCOLESTR pstrDelimiter,         // address of end-of-scriptlet delimiter  
    DWORD_PTR dwSourceContextCookie, // application-defined value for debugging  
    ULONG ulStartingLineNumber,      // starting line of the script  
    DWORD dwFlags,                   // scriptlet flags  
    BSTR *pbstrName,                 // address of actual name of scriptlet  
    EXCEPINFO *pexcepinfo            // address of exception information  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrDefaultName`  
 [in] Kod oluşturma yöntemiyle ilişkilendirmek için varsayılan adı adresi. Kod oluşturma (örnekte ONCLICK yukarıdaki) adlandırma bilgi içermiyorsa, bu ad, kod oluşturma yöntemi tanımlamak için kullanılır. Bu parametre `NULL`, komut dosyası altyapısı gerekirse benzersiz bir ad üretir.  
  
 `pstrCode`  
 [in] Eklemek için kod oluşturma yöntemi metni adresi. Bu dizenin yorumu komut dosyası diline bağlıdır.  
  
 `pstrItemName`  
 [in] Bu kod oluşturma yöntemiyle ilişkili öğe adı içeren bir arabellek adresi. Ek olarak, bu parametre `pstrSubItemName`, kod oluşturma olan bir olay işleyicisi nesneyi tanımlar.  
  
 `pstrSubItemName`  
 [in] Adını içeren bir arabelleğin adresi bir `subobject` adlı öğesi, bu kod oluşturma ilişkilidir; bu ad adlandırılmış öğenin tür bilgileri bulunamadı. Kod oluşturma yerine adlandırılmış öğe ile ilişkilendirilecek Bu parametre NULL ise bir `subitem`. Ek olarak, bu parametre `pstrItemName`, kod oluşturma olan bir olay işleyicisi belirli bir nesneyi tanımlar.  
  
 `pstrEventName`  
 [in] Kod oluşturma yöntemi bir olay işleyicisi olduğu olay adını içeren bir arabellek adresi.  
  
 `pstrDelimiter`  
 [in] Resimli bitiş sınırlayıcısı adresi. Zaman `pstrCode` parametresi, bir metin akışından ayrıştırılır, gibi iki kod oluşturma sonuna algılamak için tırnak işaretleri ("), tek bir ana bilgisayar genellikle bir ayırıcı kullanır. Bu parametre, bazı koşullu ilkel bir ön işleme sağlamak komut dosyası altyapısı verme konak kullanılan sınırlayıcıyı belirtir (örneğin, tek tırnak işaretini ['] ayırıcı olarak kullanılacak iki tek tırnak işaretleri yerine). Tam olarak nasıl (ve ise) bu bilgilerin kullanılması, komut dosyası altyapısına bağlıdır kullanmayacağı. Ana bilgisayar kod oluşturma sonunu işaretlemek için sınırlayıcı kullanmadıysanız, bu parametre NULL olarak ayarlayın.  
  
 `dwSourceContextCookie`  
 [in] Hata ayıklama amacıyla kullanılan uygulama tanımlı değer.  
  
 `ulStartingLineNumber`  
 [in] Hangi satır ayrıştırmaya başlanacağını belirleyen sıfır tabanlı değer.  
  
 `dwFlags`  
 [in] Kod oluşturma yöntemiyle ilişkili bayraklar. Aşağıdaki değerlerin bir birleşimi olabilir:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|SCRIPTTEXT_ISVISIBLE|Komut metni görünür olması gerektiğini belirtir (ve bu nedenle, çağrılabilmesini) komut dosyası ad alanında genel bir yöntem olarak.|  
|SCRIPTTEXT_ISPERSISTENT|Komut dosyası altyapısı kaydedilirse, bu çağrı sırasında eklenen kodu kaydedilmesi gerektiğini belirtir (örneğin, bir çağrı yoluyla `IPersist*::Save`), veya komut dosyası altyapısı başlatılmış durumuna geçiş yoluyla sıfırlanır. Bu durumu hakkında daha fazla bilgi için komut dosyası motoru durumu bakın.|  
  
 `pbstrName` ,  
 [out] Kod oluşturma yöntemi tanımlamak için kullanılan gerçek adı. Bu tercih sırasına göre olacak: kod oluşturma yöntemi metni açıkça belirtilen bir ad, varsayılan adı sağlanan `pstrDefaultName`, veya komut dosyası altyapısı tarafından oluşturulan benzersiz bir ad.  
  
 `pexcepinfo` ,  
 [out] Özel durum bilgilerini içeren bir yapının adresi. DISP_E_EXCEPTION döndürülürse, bu yapı doldurulması.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`DISP_E_EXCEPTION`|Kod oluşturma ayrıştırma işlemlerinde bir özel durum oluştu. `pexcepinfo` Parametre özel durum hakkında bilgi içerir.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_NOTIMPL`|Bu yöntem desteklenmiyor; komut dosyası altyapısı, olay indirme kod parçacıklarını eklemeyi desteklemez.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı henüz yüklenen başlatıldı veya) ve bu nedenle başarısız oldu.|  
|`OLESCRIPT_E_INVALIDNAME`|Bu komut dili ile sağlanan varsayılan adı geçersiz.|  
|`OLESCRIPT_E_SYNTAX`|Kod oluşturma yönteminde belirtilmeyen sözdizimi hatası oluştu.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptParse](../../winscript/reference/iactivescriptparse.md)