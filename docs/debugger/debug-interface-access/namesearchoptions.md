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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4bbe801b749b60cd22ce8a980ea78b7713fa4422
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54973895"
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