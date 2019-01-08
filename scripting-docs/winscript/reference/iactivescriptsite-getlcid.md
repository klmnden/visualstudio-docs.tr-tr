---
title: IActiveScriptSite::GetLCID | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSite.GetLCID
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSite_GetLCID
ms.assetid: 7b4a2dc1-bcf6-4bbf-884e-97b305a28eb7
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 959989d14d2a71f9c9eab4c78ef1b1bd9078362f
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54095010"
---
# <a name="iactivescriptsitegetlcid"></a>IActiveScriptSite::GetLCID
Ana bilgisayarın kullanıcı arabirimi ile ilişkilendirilmiş yerel ayar tanımlayıcısını alır. Komut dosyası altyapısı tanımlayıcı hata dizelerini ve altyapı tarafından oluşturulan diğer kullanıcı arabirimi öğeleri uygun dilde göründüğünden emin olmak için kullanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetLCID(  
    LCID *plcid  // address of variable for language identifier  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `plcid`  
 [out] Komut dosyası altyapısı tarafından görüntülenen kullanıcı arabirimi öğeleri için yerel ayar tanıtıcısını alan bir değişkenin adresidir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_NOTIMPL`|Bu yöntem uygulanmadı. Sistem tarafından tanımlanan yerel ayarı kullanın.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem döndürürse `E_NOTIMPL`, sistem tarafından tanımlanan bir yerel ayar tanımlayıcısı kullanılmalıdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSite](../../winscript/reference/iactivescriptsite.md)