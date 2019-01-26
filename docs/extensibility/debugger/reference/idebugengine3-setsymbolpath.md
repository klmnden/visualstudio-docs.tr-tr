---
title: IDebugEngine3::SetSymbolPath | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugEngine3::SetSymbolPath
helpviewer_keywords:
- IDebugEngine3::SetSymbolPath
ms.assetid: 47b48f84-8a96-401f-84df-0baa8a96d26e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c92bdd32c43e3877262bae16011e27eb73963e7a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54932967"
---
# <a name="idebugengine3setsymbolpath"></a>IDebugEngine3::SetSymbolPath
Yol veya hata ayıklama simgeleri arama yollarını ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT SetSymbolPath (  
   LPOLESTR            szSymbolSearchPath,  
   LPOLESTR            szSymbolCachePath,  
   LOAD_SYMBOLS_FLAGS  Flags  
);  
```  
  
```csharp  
int SetSymbolPath(  
   string                    szSymbolSearchPath,   
   string                    szSymbolCachePath,   
   enum_LOAD_SYMBOLS_FLAGS   Flags  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`szSymbolSearchPath`|[in] Sembol arama yolu veya yolları içeren dize. Ayrıntılar için "Açıklamalar" bakın. Null olamaz.|  
|`szSymbolCachePath`|[in] Burada sembolleri önbelleğe alınabilir yerel yolu içeren dize. Null olamaz.|  
|`Flags`|[in] Kullanılmayan; her zaman 0 olarak ayarlayın.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Dize `szSymbolSearchPath` simge araması için noktalı virgülle ayırarak bir veya daha fazla yolları bir listesidir. Bu yollar, yerel bir yol, bir stil UNC yolu veya bir URL olabilir. Bu yolları farklı türlerinin bir karışımını de olabilir. UNC yolu ise (örneğin, \\\Symserver\Symbols), hata ayıklama altyapısı yolu için bir sembol sunucusu ve tarafından belirtilen yoldaki bunları önbelleğe alma, o sunucudan sembolleri değiştirebilmesi belirlemelisiniz sonra `szSymbolCachePath`.  
  
 Sembol yolu bir veya daha fazla önbellek konumlarını da içerebilir. Önbellekler öncelik sırasına, en yüksek öncelikli önbellek ile ilk önce listelenir ve ayrılmış * semboller. Örneğin:  
  
```  
\\symbols\symbols;\\someotherserver\symbols;c:\symbols\httpsymbols*http://msdl.microsoft.com  
```  
  
 [LoadSymbols](../../../extensibility/debugger/reference/idebugengine3-loadsymbols.md) yöntemi gerçek yük sembolleri gerçekleştirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [LoadSymbols](../../../extensibility/debugger/reference/idebugengine3-loadsymbols.md)   
 [IDebugEngine3](../../../extensibility/debugger/reference/idebugengine3.md)