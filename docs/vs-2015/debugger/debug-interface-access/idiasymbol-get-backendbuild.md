---
title: Idiasymbol::get_backendbuild | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_backEndBuild method
ms.assetid: 423af497-9294-438e-92b4-456c6f56dc56
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 28d4f9f7f54a518b7dcb85f48003e3681df4b1c9
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54781742"
---
# <a name="idiasymbolgetbackendbuild"></a>IDiaSymbol::get_backEndBuild
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Derleyici arka uç yapı sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT get_backEndBuild (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Arka uç yapı numarasını döndürür. Açıklamalara bakın.  
  
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
