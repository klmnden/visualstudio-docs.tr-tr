---
title: Idiasymbol::get_issplitted | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_isSplitted method
ms.assetid: ff160cf6-003b-4ef5-a406-20a7b287b2bf
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7cb5005472243632d4e4e189ca57715cc7d3d030
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54967134"
---
# <a name="idiasymbolgetissplitted"></a>IDiaSymbol::get_isSplitted
Veri simgesi bir toplama veya diğer semboller koleksiyonu bölünmüş olup olmadığını belirten bir bayrak alır; bunlar gerçekten daha büyük bir simge bir parçası olmasına rağmen derleyici sembolleri ayrı varlıklar olarak değerlendirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_isSplitted(  
   BOOL *pFlag  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pFlag`  
 [out] Döndürür `TRUE` sembol simgeleri; toplama ayırırsanız, aksi takdirde döndürür `FALSE`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.  
  
## <a name="remarks"></a>Açıklamalar  
 [Idiasymbol::get_isaggregated](../../debugger/debug-interface-access/idiasymbol-get-isaggregated.md) yöntemi döndürür `TRUE` bölünmüş sembol parçası olan tüm sembolleri için.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v8.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [IDiaSymbol::get_isAggregated](../../debugger/debug-interface-access/idiasymbol-get-isaggregated.md)