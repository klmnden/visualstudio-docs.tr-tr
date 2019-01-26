---
title: BasicType | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- BasicType enumeration
ms.assetid: 19ae53ba-cd6e-47b6-9f94-27ae663ce955
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7fb6000da7ab5d9ff17f78cacf87608432b839e8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55030944"
---
# <a name="basictype"></a>BasicType
Simgenin temel türünü belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
enum BasicType {   
   btNoType   = 0,  
   btVoid     = 1,  
   btChar     = 2,  
   btWChar    = 3,  
   btInt      = 6,  
   btUInt     = 7,  
   btFloat    = 8,  
   btBCD      = 9,  
   btBool     = 10,  
   btLong     = 13,  
   btULong    = 14,  
   btCurrency = 25,  
   btDate     = 26,  
   btVariant  = 27,  
   btComplex  = 28,  
   btBit      = 29,  
   btBSTR     = 30,  
   btHresult  = 31,  
   btChar16   = 32,  // char16_t
   btChar32   = 33,  // char32_t
};  
```  
  
## <a name="elements"></a>Öğeleri  
 btNoType  
 Belirtilen hiçbir temel türü.  
  
 btVoid  
 Temel türü bir `void`.  
  
 btChar  
 Temel türü bir `char` (C/C++ türü).  
  
 btWChar  
 Temel türü olan geniş karakter (Unicode) (`WCHAR`).  
  
 btInt  
 Temel türü `signed int` (C/C++ türü).  
  
 btUInt  
 Temel türü `unsigned int` (C/C++ türü).  
  
 btFloat  
 Temel türü olan bir kayan noktalı sayı (`FLOAT`).  
  
 btBCD  
 Temel türü, ikili dosya kodlanmış bir ondalık (`BCD`).  
  
 btBool  
 Temel türü olan bir Boole değeri (`BOOL`).  
  
 btLong  
 Temel türü bir `long int` (C/C++ türü).  
  
 btULong  
 Temel türü bir `unsigned long int` (C/C++ türü).  
  
 btCurrency  
 Para birimi temel türüdür.  
  
 btDate  
 Temel türü, tarih/saat (`DATE`).  
  
 btVariant  
 Temel türü olan bir değişken türü yapısı (`VARIANT`).  
  
 btComplex  
 Temel türü karmaşık bir sayıdır.  
  
 btBit  
 Temel bir bit türüdür.  
  
 btBSTR  
 Temel türü olan temel ya da ikili bir dize (`BSTR`).  
  
 btHresult  
 Temel türü bir `HRESULT`.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu sabit listesi değerleri tarafından döndürülen [Idiasymbol::get_basetype](../../debugger/debug-interface-access/idiasymbol-get-basetype.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: cvconst.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri ve yapıları](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [Idiasymbol::get_basetype](../../debugger/debug-interface-access/idiasymbol-get-basetype.md)   
 [IDiaSymbol::get_length](../../debugger/debug-interface-access/idiasymbol-get-length.md)
