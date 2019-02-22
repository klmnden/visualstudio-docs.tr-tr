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
ms.openlocfilehash: e7dbb82946d185e8e5ec81b171f5d9943751eee4
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56639693"
---
# <a name="namesearchoptions"></a>NameSearchOptions
Sembol ve dosya adları için arama seçeneklerini belirtir.

## <a name="syntax"></a>Sözdizimi

```C++
enum NameSearchOptions {
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
`nsNone` Hiçbir seçenek belirtilmedi.

`nsfCaseSensitive` Büyük/küçük harfe adı eşleştirmesi uygular.

`nsfCaseInsensitive` Büyük küçük harf duyarsız adı eşleştirmesi uygular.

`nsfFNameExt` Adları, yollar olarak değerlendirir ve DosyaAdı.uzn adı eşleştirmesi uygular.

`nsfRegularExpression` Joker karakter olarak yıldız işareti (*) ve soru işareti (?) kullanarak bir büyük/küçük harfe adı eşleştirmesi uygular.

`nsfUndecoratedName` Hem tamamlanmamış ve düzenlenmiş adları sembolleri geçerlidir.

## <a name="remarks"></a>Açıklamalar
Bu numaralandırma değerleri için aşağıdaki yöntemlerden geçirilir:

- [IDiaSession::findChildren](../../debugger/debug-interface-access/idiasession-findchildren.md)

- [IDiaSession::findFile](../../debugger/debug-interface-access/idiasession-findfile.md)

- [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md)

## <a name="requirements"></a>Gereksinimler
Üstbilgi: dia2.h

## <a name="see-also"></a>Ayrıca Bkz.
- [Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaSession::findChildren](../../debugger/debug-interface-access/idiasession-findchildren.md)
- [IDiaSession::findFile](../../debugger/debug-interface-access/idiasession-findfile.md)
- [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md)
