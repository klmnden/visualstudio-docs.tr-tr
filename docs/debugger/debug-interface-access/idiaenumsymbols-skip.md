---
title: Idiaenumsymbols::Skip | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumSymbols::Skip method
ms.assetid: e601fbc9-b10b-41c7-8180-959e57efabe8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0168c3f58cf9bd701f0cc34edf77673c70e66222
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55021448"
---
# <a name="idiaenumsymbolsskip"></a>IDiaEnumSymbols::Skip
Bir numaralandırma sıralı sembolleri belirtilen sayıda atlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT Skip (   
   ULONG celt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 celt  
 [in] Sabit listesi sırası atlamak için sembolleri sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` atlamak için daha fazla sembol varsa.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)