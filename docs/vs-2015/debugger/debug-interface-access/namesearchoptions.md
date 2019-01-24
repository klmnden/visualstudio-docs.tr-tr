---
title: NameSearchOptions | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- NameSearchOptions enumeration
ms.assetid: 67dfbede-2678-47df-b664-5c49841d0b9b
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 29b6500ab138883c8cbf71eda5a0afad1329494e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54755633"
---
# <a name="namesearchoptions"></a>NameSearchOptions
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Sembol ve dosya adları için arama seçeneklerini belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
