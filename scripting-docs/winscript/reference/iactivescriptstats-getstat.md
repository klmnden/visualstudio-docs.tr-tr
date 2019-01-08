---
title: IActiveScriptStats::GetStat | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptStats.GetStat
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptStats::GetStat
ms.assetid: 31fd15b3-0713-4b55-b4f7-bfd7ea198493
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0d00c438f0fe03566dfb7efb93645cad02dc7477
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54095400"
---
# <a name="iactivescriptstatsgetstat"></a>IActiveScriptStats::GetStat
Standart komut dosyası istatistikleri döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetStat(  
   DWORD   stid,  
   ULONG*  pluHi,  
   ULONG*  pluLo  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `stid`  
 [in] Döndürülecek istatistik belirtir. Değeri olmalıdır:  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|SCRIPTSTAT_STATEMENT_COUNT|1.|Betik çalışmaya veya istatistikleri sıfırlandı yürütülen deyimleri sayısını döndürür.|  
  
 `pluHi`  
 [out] İstatistik temsil eden bir 64-bit işaretsiz tamsayıyı yüksek 32 bit.  
  
 `pluLo`  
 [out] İstatistik temsil eden bir 64-bit işaretsiz tamsayıyı düşük 32 bit.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler içerir, ancak aşağıdaki tablodaki değerlerle sınırlı değildir.  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem standart betik istatistikleri döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptStats::GetStatEx](../../winscript/reference/iactivescriptstats-getstatex.md)   
 [IActiveScriptStats Arabirimi](../../winscript/reference/iactivescriptstats-interface.md)