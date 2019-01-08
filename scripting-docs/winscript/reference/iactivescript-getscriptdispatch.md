---
title: IActiveScript::GetScriptDispatch | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.GetScriptDispatch
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_GetScriptDispatch
ms.assetid: 2092ccd4-1f4c-493a-b5b7-077a70ce95ca
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2a18d6781ca2b7820686b317ad0be5da425ade1f
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097688"
---
# <a name="iactivescriptgetscriptdispatch"></a>IActiveScript::GetScriptDispatch
Alır `IDispatch` arabirimdeki yöntemleri ve özellikleri şu anda çalışan bir komut dosyasıyla ilişkilidir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetScriptDispatch(  
    LPCOLESTR pstrItemName  // address of item name  
    IDispatch **ppdisp      // receives IDispatch pointer  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrItemName`  
 [in] Kendisi için çağıranın ilişkili dağıtım nesnesi gerekiyor öğesinin adını içeren bir arabellek adresi. Bu parametre `NULL`, dağıtım nesnesi grupların üyeleri komut dosyası tarafından tanımlanan tüm genel yöntemleri ve özellikleri içerir. Aracılığıyla `IDispatch` arabirimi ve ilişkili `ITypeInfo` arabirimi, konak betik yöntemleri veya Görünüm çağırır ve komut dosyası değişkenleri değiştirin.  
  
 `ppdisp`  
 [out] Betiğin genel yöntemleri ve özellikleri ile ilişkili nesneye bir işaretçi alan değişkenin adresi. Komut dosyası altyapısı böyle bir nesnenin desteklemiyorsa `NULL` döndürülür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı henüz yüklenen başlatıldı veya).|  
|`S_FALSE`|Komut dosyası altyapısı, dağıtım nesnesi desteklemiyor; `ppdisp` parametresi NULL olarak ayarlanır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yöntemlere ve özelliklere çağırarak eklenebildiği [Iactivescriptparse](../../winscript/reference/iactivescriptparse.md) arabirimi `IDispatch` bu yöntem tarafından döndürülen arabirimi yeni yöntemleri ve özellikleri dinamik olarak destekleyebilir. Benzer şekilde, `IDispatch::GetTypeInfo` yöntemi döndürmelidir yeni, benzersiz `ITypeInfo` arabirim yöntemleri ve özellikleri eklendiğinde. Ancak, dil altyapıları değiştirmemelisiniz unutmayın `IDispatch` arabiriminde bir şekilde uyumlu herhangi önceki `ITypeInfo` arabirimi döndürdü. Bu, örneğin, DISPID değeri hiçbir zaman kullanılabilmeleri anlamına gelir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)