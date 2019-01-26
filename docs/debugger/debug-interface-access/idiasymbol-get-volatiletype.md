---
title: Idiasymbol::get_volatiletype | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_volatileType method
ms.assetid: 19782a4d-40a8-467b-ab7d-58bc4d812309
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e358efc95d3c0d281a24109ee5ab954d6ea88506
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54989040"
---
# <a name="idiasymbolgetvolatiletype"></a>IDiaSymbol::get_volatileType
Kullanıcı tanımlı veri türü (UDT) geçici olup olmadığını belirten bir bayrak alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_volatileType (   
   BOOL* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Döndürür `TRUE` UDT, aksi takdirde geçici döndürür `FALSE`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.  
  
## <a name="remarks"></a>Açıklamalar  
 C++'da bir UDT ile işaretlenebilir `volatile` içeriğinin bir erişimden sonraki bulunması kabul edilemez belirten bir anahtar sözcüğü,.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)