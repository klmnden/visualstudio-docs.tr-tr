---
title: Idiasymbol::get_editandcontinueenabled | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_editAndContinueEnabled method
ms.assetid: cd703c64-9ff8-4654-8493-8cde9309cb22
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 16e22de399d69c2e22cb4c24e12504786a28df74
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54951618"
---
# <a name="idiasymbolgeteditandcontinueenabled"></a>IDiaSymbol::get_editAndContinueEnabled
Modül ile derlenen olup olmadığını belirten bir bayrak alır [/z7, / zi, /zı (hata ayıklama bilgileri biçimi)](/cpp/build/reference/z7-zi-zi-debug-information-format) derleyici anahtarı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_editAndContinueEnabled (   
   BOOL* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Döndürür `TRUE` Düzenle ve devam et; derleme etkinleştirildiyse döndürür, aksi takdirde, `FALSE`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için mevcut olmadığı anlamına gelir.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v7.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [/Z7, /Zi, /ZI (Hata Ayıklama Bilgileri Biçimi)](/cpp/build/reference/z7-zi-zi-debug-information-format)