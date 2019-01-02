---
title: Idiaenumframedata::framebyva | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumFrameData::frameByVA method
ms.assetid: 0b1e441b-710a-46d8-8060-bed39071c834
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9f905c3aa380c6decd6687ff2332af2f196d0b68
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53851595"
---
# <a name="idiaenumframedataframebyva"></a>IDiaEnumFrameData::frameByVA
Bir çerçeve sanal adres (VA) döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT frameByVA(   
   ULONGLONG       virtualAddress,  
   IDiaFrameData** frame  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 virtualAddress  
 [in] VA ilgi çerçeve.  
  
 çerçeve  
 [out] Döndürür bir [Idiaframedata](../../debugger/debug-interface-access/idiaframedata.md) sağlanan adresini içeren çerçeveyi temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` belirtilen adresi çerçeve veri eşleşmesi durumunda. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumframedata](../../debugger/debug-interface-access/idiaenumframedata.md)   
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)