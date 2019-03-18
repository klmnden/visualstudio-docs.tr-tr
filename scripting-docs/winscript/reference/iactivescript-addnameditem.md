---
title: IActiveScript::AddNamedItem | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.AddNamedItem
apilocation:
- scrobj.dll
helpviewer_keywords:
- AddNamedItem method, IActiveScript interface
ms.assetid: a7c6317d-948f-4bb3-b169-1bbe5b7c7cc5
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: db0a97c01d948a0c26850ebd1c3f47c6e3900614
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58151862"
---
# <a name="iactivescriptaddnameditem"></a>IActiveScript::AddNamedItem
Komut dosyası altyapısının ad alanı için bir kök düzey öğesi adını ekler. Kök düzey öğesi, özellikleri ve yöntemleri, bir olay kaynağı veya üçünü içeren bir nesnedir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT AddNamedItem(  
    LPCOLESTR pstrName,  // address of item name  
    DWORD dwFlags          // item flags  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrName`  
 [in] Betikten göründüğü haliyle öğenin adını içeren bir arabellek adresi. Ad benzersiz ve kalıcı olması gerekir.  
  
 `dwFlags`  
 [in] Bir öğeyle ilişkili bayraklar. Bu değerleri bir birleşimi olabilir:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|SCRIPTITEM_CODEONLY|Adlandırılmış öğe yalnızca kod bir nesneyi temsil eder ve konak yoktur gösterir `IUnknown` Bu kod yalnızca nesne ile ilişkilendirilecek. Konak yalnızca bu nesne için bir adı vardır. Nesne yönelimli gibi C++ dilleri içinde bu bayrağı, bir sınıf oluşturursunuz. Bu bayrak tüm dilleri destekler.|  
|SCRIPTITEM_GLOBALMEMBERS|Öğesi genel özellikleri ve yöntemleri komut dosyasıyla ilişkilidir koleksiyonu olduğunu gösterir. Normalde, bir komut dosyası altyapısı nesne adı yok (dışında bir tanımlama bilgisi olarak kullanma amacıyla [IActiveScriptSite::GetItemInfo](../../winscript/reference/iactivescriptsite-getiteminfo.md) yöntemi veya açık kapsam çözümleme için) ve onun üyeleri genel olarak kullanıma sunma değişkenler ve yöntemler. Bu kitaplık (çalışma zamanı işlevleri ve benzeri) betiği kullanılabilir genişletmek konak sağlar. Komut dosyası altyapısı adıyla işlem sol (örneğin, iki SCRIPTITEM_GLOBALMEMBERS öğeleri aynı ada sahip yöntem olduğunda) bir hata nedeniyle bu durum döndürülmemesi gereken olsa da, çakışıyor.|  
|SCRIPTITEM_ISPERSISTENT|Komut dosyası altyapısı kaydedilirse öğesi kaydedilmesi gerektiğini gösterir. Benzer şekilde, bu bayrağı ayarlamanın gösteren bir geçiş yeniden başlatılmış bir durumda öğenin ad ve tür bilgileri (komut dosyası altyapısı gerekir ancak sürüm gerçek nesneye arabirimlerindeki tüm işaretçiler) korurlar.|  
|SCRIPTITEM_ISSOURCE|Öğe betik havuz olay kaynakları gösterir. Alt nesneleri (kendilerini içinde olan nesneler nesnenin özelliklerini), ayrıca betik olayları edinebilir. Bu özyinelemeli değildir, ancak ortak çalışması için kullanışlı bir mekanizma Örneğin, bir kapsayıcı ve tüm üye denetimleri oluşturmayı sağlar.|  
|SCRIPTITEM_ISVISIBLE|Öğenin adı erişimine izin özellikleri, yöntemleri ve olayları öğesi komut dosyası, ad alanında kullanılabilir olduğunu gösterir. Kural gereği öğenin alt öğeleri öğenin özelliklerini içerir. Bu nedenle, tüm alt nesne özellikleri ve yöntemleri (ve alt öğelerini, yinelemeli olarak) erişilebilir.|  
|SCRIPTITEM_NOCODE|Öğe yalnızca betiğin adını alanınıza eklenen bir ad ve kodu ilişkili olmalıdır, bir öğe olarak değerlendirilip değil gösterir. Örneğin, ayarlanan bu bayrağı olmadan VBScript adlandırılmış öğe için ayrı bir modül oluşturur ve C++ adlandırılmış öğe için ayrı bir sarmalayıcı sınıf oluşturabilirsiniz.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı henüz yüklenen başlatıldı veya).|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)