---
title: IActiveScriptStats::GetStatEx | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptStats.GetStatEx
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptStats::GetStatEx
ms.assetid: f526f51d-8ab5-49ef-a8f7-ae0ac1cb46e4
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3e5f25887d8fdd5b5fb774cc2e8619c1a93432c1
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63442773"
---
# <a name="iactivescriptstatsgetstatex"></a>IActiveScriptStats::GetStatEx
Özel betik istatistiği döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetStatEx(  
   REFGUID  guid,  
   ULONG*   pluHi,  
   ULONG*   pluLo  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `guid`  
 [in] Döndürülecek istatistik belirtir. Semantiği istatistik karşılık gelen belirli bir GUID tamamen tanımlanan altyapısıdır.  
  
 `pluHi`  
 [out] İstatistik temsil eden bir 64-bit işaretsiz tamsayıyı yüksek 32 bit.  
  
 `pluLo`  
 [out] İstatistik temsil eden bir 64-bit işaretsiz tamsayıyı düşük 32 bit.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_NOTIMPL`|Yöntem uygulanmadı.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem için özel bir ana bilgisayar istatistikleri anlamlı döndürmek bir özel betik altyapısı sağlar.  
  
> [!NOTE]
> Bu yöntem henüz uygulanmadı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptStats::GetStat](../../winscript/reference/iactivescriptstats-getstat.md)   
 [IActiveScriptStats Arabirimi](../../winscript/reference/iactivescriptstats-interface.md)