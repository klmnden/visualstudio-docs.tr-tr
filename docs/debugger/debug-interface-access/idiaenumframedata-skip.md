---
title: Idiaenumframedata::Skip | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumFrameData::Skip method
ms.assetid: 67140b4c-7125-4895-932d-42412326da29
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2ad89beb8672c8f8cf2d6d6710ee53dccba5b5ed
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55000337"
---
# <a name="idiaenumframedataskip"></a>IDiaEnumFrameData::Skip
Belirtilen sayıda bir numaralandırma sıralı çerçeve veri öğeleri atlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT Skip (   
   ULONG celt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 celt  
 [in] Veri öğeleri atlamak için sabit listesi sırası çerçeve sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` atlamak için daha fazla kayıt varsa.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaEnumFrameData](../../debugger/debug-interface-access/idiaenumframedata.md)