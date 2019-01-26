---
title: Idiasymbol::get_hasseh | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_hasSEH method
ms.assetid: 1a709ded-22c8-464c-97be-eba5e464210c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7ced9377d017bfbbcb4a200c004f8223a5636f39
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54925590"
---
# <a name="idiasymbolgethasseh"></a>IDiaSymbol::get_hasSEH
İşlev herhangi içerip içermediğini belirten bir bayrak alır [yapılandırılmış özel durum işleme (C/C++)](/cpp/cpp/structured-exception-handling-c-cpp) (örneğin, __try /\__except bloğu).  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_hasSEH(  
   BOOL *pFlag  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pFlag`  
 [out] Döndürür `TRUE` tüm yapılandırılmış özel durum blokları; işleme işlevi varsa, aksi halde döndürür `FALSE`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v8.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [Yapılandırılmış Özel Durum İşleme (C/C++)](/cpp/cpp/structured-exception-handling-c-cpp)