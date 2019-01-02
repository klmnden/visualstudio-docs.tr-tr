---
title: NameSearchOptions | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- NameSearchOptions enumeration
ms.assetid: 67dfbede-2678-47df-b664-5c49841d0b9b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e816c559215d5662fe1a20dcad21eaf30f7667bc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53868059"
---
# <a name="namesearchoptions"></a>NameSearchOptions
Sembol ve dosya adları için arama seçeneklerini belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
enum NameSearchOptions {   
   nsNone,  
   nsfCaseSensitive     = 0x1,  
   nsfCaseInsensitive   = 0x2,  
   nsfFNameExt          = 0x4,  
   nsfRegularExpression = 0x8,  
   nsfUndecoratedName   = 0x10,  
  
// For backward compatibility:  
   nsCaseSensitive           = nsfCaseSensitive,  
   nsCaseInsensitive         = nsfCaseInsensitive,  
   nsFNameExt                = nsfCaseInsensitive | nsfFNameExt,  
   nsRegularExpression       = nsfRegularExpression | nsfCaseSensitive,  
   nsCaseInRegularExpression = nsfRegularExpression | nsfCaseInsensitive  
};  
```  
  
## <a name="elements"></a>Öğeleri  
 `nsNone`  
 Hiçbir seçenek belirtilmedi.  
  
 `nsfCaseSensitive`  
 Büyük/küçük harfe adı eşleştirmesi uygular.  
  
 `nsfCaseInsensitive`  
 Büyük küçük harf duyarsız adı eşleştirmesi uygular.  
  
 `nsfFNameExt`  
 Adları, yollar olarak değerlendirir ve DosyaAdı.uzn adı eşleştirmesi uygular.  
  
 `nsfRegularExpression`  
 Joker karakter olarak yıldız işareti (*) ve soru işareti (?) kullanarak bir büyük/küçük harfe adı eşleştirmesi uygular.  
  
 `nsfUndecoratedName`  
 Hem tamamlanmamış ve düzenlenmiş adları sembolleri geçerlidir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu numaralandırma değerleri için aşağıdaki yöntemlerden geçirilir:  
  
-   [IDiaSession::findChildren](../../debugger/debug-interface-access/idiasession-findchildren.md)  
  
-   [IDiaSession::findFile](../../debugger/debug-interface-access/idiasession-findfile.md)  
  
-   [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md)  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: dia2.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri ve yapıları](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [Idiasession::findchildren](../../debugger/debug-interface-access/idiasession-findchildren.md)   
 [Idiasession::findfile](../../debugger/debug-interface-access/idiasession-findfile.md)   
 [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md)