---
title: Idiasymbol::get_noreturn | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_noReturn method
ms.assetid: 704c1cc0-5b84-4334-a02a-70f43aff39d5
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 817d515d9ab744ec7be146e6ee39373cb7d2d2ee
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53863883"
---
# <a name="idiasymbolgetnoreturn"></a>IDiaSymbol::get_noReturn
İşlevi ile hiçbir zaman döndüren olarak işaretlenmiş olup olmadığını belirten bir bayrak alır [noreturn](/cpp/cpp/noreturn) özniteliği.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_noReturn(  
   BOOL *pFlag  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pFlag  
 [out] Döndürür `TRUE` işlevi ile hiçbir zaman döndüren olarak bildirilmiş ise `noreturn` özniteliği; Aksi halde döndürür `FALSE`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v8.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [noreturn](/cpp/cpp/noreturn)