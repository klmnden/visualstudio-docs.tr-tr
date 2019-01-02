---
title: Idiasymbol::get_frontendmajor | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_frontEndMajor method
ms.assetid: f8a067c5-3306-4fc5-bc20-8910a47ed504
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 29d132e39277e0bb9c868fc8d4c2ad3877aa6546
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53851517"
---
# <a name="idiasymbolgetfrontendmajor"></a>IDiaSymbol::get_frontEndMajor
Ön uç ana sürüm numarasını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_frontEndMajor (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Ön uç ana sürüm numarasını döndürür. Açıklamalara bakın.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için mevcut olmadığı anlamına gelir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir derleyici genellikle birincil iki öğeden oluşur: bir ara forma kaynak kodu ayrıştırma işleyen ön uç (ayrıştırıcının) ve derlemeye Ara formun dönüştüren bir arka uç (Kod Oluşturucu). Arka uçtan farklı bir sürüm ön uç için sık karşılaşılan bir durum değil.  
  
 Ön uç veya arka uç sürüm numarası, üç bölümden oluşur: \<ana >.\< küçük >. \<Yapı >, burada \<ana > ana sürüm numarası \<küçük > alt sürüm numarası ve \<Yapı > yapı numarasıdır. Örneğin, 13.10.3077.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v7.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)