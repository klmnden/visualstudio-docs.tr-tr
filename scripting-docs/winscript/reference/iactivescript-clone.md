---
title: IActiveScript::Clone | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.Clone
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_Clone
ms.assetid: aa000b2a-7085-448d-a422-f7adac7851cb
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 084da486d2e5831176130ccd080b9e09a80c9bcc
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54093671"
---
# <a name="iactivescriptclone"></a>IActiveScript::Clone
Geçerli iş parçacığındaki hiçbir sitede yüklü bir komut dosyası altyapısı döndüren geçerli komut dosyası altyapısı (tüm geçerli yürütme durumu), eksi kopyalar. Bu yeni bir komut dosyası altyapısı özelliklerini özgün komut dosyası altyapısı, geçti, başlatılmamış duruma geri olması özellikleri aynı olacaktır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Clone(  
    IActiveScript **ppscript  // receives pointer to IActiveScript  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppscript`  
 [out] Bir işaretçiye alan değişkenin adresini [IActiveScript](../../winscript/reference/iactivescript.md) kopyalanan komut dosyası altyapısı arabirimi. Ana bilgisayar bir site ve çağrı oluşturmalısınız [IActiveScript::SetScriptSite](../../winscript/reference/iactivescript-setscriptsite.md) başlatılan durumda kullanılabilmesi yeni komut dosyası altyapısı yöntemi ve bu nedenle, kullanılabilir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_NOTIMPL`|Bu yöntem desteklenmiyor.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı henüz yüklenen başlatıldı veya).|  
  
## <a name="remarks"></a>Açıklamalar  
 `IActiveScript::Clone` Yöntemdir bir en iyi duruma getirilmesi `IPersist*::Save`, `CoCreateInstance`, ve `IPersist*::Load`, özgün komut dosyası motoru durumu kaydedildi ve yeni bir komut dosyası altyapısı yüklenmiş gibi yeni komut dosyası motoru durumu aynı olmalıdır. Adlandırılmış öğeleri kopyalanan komut dosyası altyapısı içinde yinelenen, ancak her öğe için belirli nesne işaretçileri unutulur ve elde edilen [IActiveScriptSite::GetItemInfo](../../winscript/reference/iactivescriptsite-getiteminfo.md) yöntemi. Bu, kullanılacak iş parçacığı başına giriş noktaları (apartman modeli) ile aynı nesne modeli sağlar.  
  
 Bu yöntem, aynı betiği birden çok örneğini çalıştırabilirsiniz birden çok iş parçacıklı server konakları için kullanılır. Komut dosyası altyapısı döndürebilir `E_NOTIMPL`, konak durumunu sürekli çoğaltma ve komut dosyası altyapısı ile yeni bir örneğini oluşturarak bu durumda aynı sonucu ulaşabileceği bir `IPersist*` arabirimi.  
  
 Temel olmayan belirtme ana bilgisayar nesneleri veya çok kaynaklanan olmadan, bu yöntem temel olmayan iş parçacığından çağrılabilir [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md) arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)