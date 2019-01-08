---
title: IDispatchEx::InvokeEx | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispatchEx.InvokeEx
apilocation:
- scrobj.dll
helpviewer_keywords:
- InvokeEx method
ms.assetid: d90783e6-4b89-4423-8a56-a9c8b4b2c813
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e631ecca1181a25fa3cf419f5fc96666f0db3cd6
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086534"
---
# <a name="idispatchexinvokeex"></a>IDispatchEx::InvokeEx
Özellikler ve yöntemler tarafından sunulan erişim sağlayan bir `IDispatchEx` nesne.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT InvokeEx(  
   DISPID id,  
   LCID lcid,  
   WORD wFlags,  
   DISPARAMS *pdp,  
   VARIANT *pVarRes,   
   EXCEPINFO *pei,   
   IServiceProvider *pspCaller   
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `id`  
 Üyeyi tanımlar. Kullanan `GetDispID` veya `GetNextDispID` gönderme tanımlayıcısının elde edilir.  
  
 `lcid`  
 Bağımsız değişkenlerin yorumlanacağı yerel ayar bağlamı. `lcid` Geçirilir `InvokeEx` bağımsız bir yerel ayar belirli yorumlamak nesne izin vermek için.  
  
 `wFlags`  
 Yasal değerler için `wFlags` şunlardır:  
  
 DISPATCH_PROPERTYGET &AMP;#124; DISPATCH_METHOD &AMP;#124; DISPATCH_PROPERTYPUT &AMP;#124; DISPATCH_PROPERTYPUTREF &AMP;#124; DISPATCH_CONSTRUCT  
  
 Bağlamını tanımlayan bayraklar `InvokeEx` çağırın:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|DISPATCH_METHOD|Üye bir yöntem çağrılır. Bir özelliği aynı ada sahipse, bu ve DISPATCH_PROPERTYGET bayrağı ayarlanmış olabilir (tarafından tanımlanan `IDispatch`).|  
|DISPATCH_PROPERTYGET|Üye bir özellik veya veri üyesi olarak alınır (tarafından tanımlanan `IDispatch`).|  
|DISPATCH_PROPERTYPUT|Üye bir özellik veya veri üyesi olarak değiştirildiğinde (tarafından tanımlanan `IDispatch`).|  
|DISPATCH_PROPERTYPUTREF|Üye bir değer atama yerine bir başvuru atamasından tarafından değiştirilir. Bu bayrağı yalnızca bir nesneye bir başvuru özelliği kabul ettiğinde geçerlidir (tarafından tanımlanan `IDispatch`).|  
|DISPATCH_CONSTRUCT|Üye Oluşturucu olarak kullanılır. (Yeni bir değer tarafından tanımlanan budur `IDispatchEx`). Yasal değerler için `wFlags` şunlardır:<br /><br /> DISPATCH_PROPERTYGET DISPATCH_METHOD DISPATCH_PROPERTYPUT DISPATCH_PROPERTYPUTREF DISPATCH_CONSTRUCT|  
  
 `pdp`  
 Bir dizi bağımsız değişkeni içeren bir yapıya yönelik işaretçi, adlandırılmış bağımsız değişkenler için bir dizi bağımsız değişken DISPID değeri ve dizilerdeki öğelerin sayısına ilişkin sayımlar. Bkz: `IDispatch` belgeleri DISPPARAMS yapısı tam bir açıklaması.  
  
 `pVarRes`  
 Sonuç depolanmış veya çağıran hiçbir sonuç beklemiyorsa Null olduğu konuma yönelik işaretçi. DISPATCH_PROPERTYPUT veya DISPATCH_PROPERTYPUTREF belirtilirse, bu bağımsız değişkeni yoksayılır.  
  
 `pei`  
 Özel durum bilgisi içeren bir yapıya yönelik işaretçi. Bu yapı sahipse doldurulması `DISP_E_EXCEPTION` döndürülür. Null olabilir. Bkz: `IDispatch` tam açıklamasını belgelerine `EXCEPINFO` yapısı.  
  
 `pspCaller`  
 İşaretçi nesnesinin, arayandan Hizmetleri elde sağlar çağıran tarafından sağlanan bir hizmet sağlayıcısı nesnesi. Null olabilir.  
  
 `IDispatchEx::InvokeEx` Tüm ile aynı özellikleri sağlayan `IDispatch::Invoke` ve birkaç uzantıları ekler:  
  
|||  
|-|-|  
|DISPATCH_CONSTRUCT|Öğe bir oluşturucu olarak kullanıldığını gösterir.|  
|`pspCaller`|`pspCaller` Hizmetleri çağıran tarafından sağlanan nesne erişmesini sağlar. Belirli hizmetleri çağıran tarafından işlenen veya daha fazla çağrı zincirine'kurmak arayanlara temsilcisi. Örneğin, bir komut dosyası altyapısının içinden, bir tarayıcı yapar bir `InvokeEx` dış nesne, nesne çağrısı izleyebilirsiniz `pspCaller` zinciri betik altyapısı veya tarayıcı Hizmetleri elde edilir. (Çağrı zinciri oluşturma zinciri ile aynı olmadığını unutmayın; kapsayıcı zinciri veya site zinciri olarak da bilinir. Zincir oluşturma gibi başka bir mekanizma aracılığıyla kullanılabilir olan `IObjectWithSite`.)|  
|`this` İşaretçi|DISPATCH_METHOD ayarlandığında `wFlags`, "Bu" değeri "adlandırılmış parametre" olabilir. DISPID DISPID_THIS olur ve ilk adlandırılmış parametre olmalıdır.|  
  
 Kullanılmayan `riid` parametresinde `IDispatch::Invoke` kaldırıldı.  
  
 `puArgArr` Parametresinde `IDispatch::Invoke` kaldırıldı.  
  
 Bkz: `IDispatch::Invoke` Aşağıdaki örnekler için belgeler:  
  
 "Bağımsız değişken içermeyen bir yöntemi çağırmak"  
  
 "Başlama ve özelliklerini ayarlama"  
  
 "Parametre geçirme"  
  
 "Dizin oluşturulmuş özellikleri"  
  
 "Invoke sırasında özel durumlarını oluşturma"  
  
 "Hataları döndürüyor."  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|||  
|-|-|  
|`S_OK`|Başarılı.|  
|DISP_E_BADPARAMCOUNT|DISPPARAMS için sağlanan öğelerin sayısı, yöntemi veya özelliği tarafından kabul edilen bağımsız değişken sayısı farklıdır.|  
|DISP_E_BADVARTYPE|İçinde bağımsız değişkenlerden biri `rgvarg` geçerli bir değişken türü değil.|  
|DISP_E_EXCEPTION|Özel durum uygulama gerekir. Yapı bu durumda, geçirilen `pei` doldurulması gerekir.|  
|DISP_E_MEMBERNOTFOUND|İstenen üye yok veya çağrı `InvokeEx` salt okunur bir özellik değeri ayarlanmaya çalışıldı.|  
|DISP_E_NONAMEDARGS|Bu uygulaması `IDispatch` adlandırılmış bağımsız değişkenler desteklemez.|  
|DISP_E_OVERFLOW|İçinde bağımsız değişkenlerden biri `rgvarg` belirtilen türe zorlanamadı.|  
|DISP_E_PARAMNOTFOUND|Bir parametre DISPID değeri yöntemine bir parametre karşılık gelmiyor.|  
|DISP_E_TYPEMISMATCH|Bir veya daha fazla bağımsız değişken zorlanamadı.|  
|DISP_E_UNKNOWNLCID|Dize bağımsız değişkenleri LCID göre çağrılmakta olan üye yorumlar ve LCID tanınmıyor. LCID bağımsız değişkenlerin yorumlanacağı gerekli değilse bu hata döndürülmelidir değil.|  
|DISP_E_PARAMNOTOPTIONAL|Gerekli parametre atlandı.|  
  
## <a name="example"></a>Örnek  
  
```cpp
VARIANT var;  
   BSTR bstrName;  
   DISPID dispid;  
   IDispatchEx *pdex;  
   DISPPARAMS dispparamsNoArgs = {NULL, NULL, 0, 0};  
  
   // Assign to pdex and bstrName  
   if (SUCCEEDED(pdex->GetDispID(bstrName, fdexNameCaseSensitive, &dispid)))  
   {  
      pdex->InvokeEx(dispid, LOCALE_USER_DEFAULT,  
         DISPATCH_PROPERTYGET, &dispparamsNoArgs,   
         &var, NULL, NULL);  
   }  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idispatchex arabirimi](../../winscript/reference/idispatchex-interface.md)   
 [IDispatchEx::GetDispID](../../winscript/reference/idispatchex-getdispid.md)   
 [IDispatchEx::GetNextDispID](../../winscript/reference/idispatchex-getnextdispid.md)