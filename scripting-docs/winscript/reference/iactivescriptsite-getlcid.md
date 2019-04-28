---
title: IActiveScriptSite::GetLCID | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: c6ebcfec9764aae98f7d74ac98e0c88ecec7c4da
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992762"
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