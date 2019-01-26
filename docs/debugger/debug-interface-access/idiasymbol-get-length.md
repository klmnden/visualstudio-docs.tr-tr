---
title: Idiasymbol::get_length | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_length method
ms.assetid: cc62f028-d195-4fbf-93bc-10b08bef52d2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b536aae5431163ae8ac6d7bd2a52d23ced662447
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54941508"
---
# <a name="idiasymbolgetlength"></a>IDiaSymbol::get_length
Bu simge ile temsil edilen nesne tarafından kullanılan belleğin bayt bit sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_length (   
   ULONGLONG* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Bayt sayısı veya bu simge ile temsil edilen nesne tarafından kullanılan bellek BITS döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.  
  
## <a name="remarks"></a>Açıklamalar  
 Varsa [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md) simgesi olan `LocIsBitField`, bu yöntem tarafından döndürülen bit uzunluğunda; Aksi takdirde diğer konum türleri için bayt cinsinden uzunluk olur.  
  
## <a name="example"></a>Örnek  
  
```C++  
IDiaSymbol* pSymbol;  
ULONGLONG   length;  
pSymbol->get_length( &length );  
```  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v7.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [LocationType Numaralandırması](../../debugger/debug-interface-access/locationtype.md)