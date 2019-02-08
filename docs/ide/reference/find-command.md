---
title: Bul Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- edit.find
helpviewer_keywords:
- Find command
- Edit.Find command
ms.assetid: f0c705dc-2b97-423d-abbf-5584d4827208
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9cd4a50ebf4c27213d288cbab33647931c4a399d
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55953067"
---
# <a name="find-command"></a>Bul Komutu
Dosyaları bulunan seçenekler kümesini kullanarak arar **dosyalarda Bul** sekmesinde **Bul ve Değiştir** penceresi.

## <a name="syntax"></a>Sözdizimi

```cmd
Edit.Find findwhat [/case] [/doc | /proc | /open | /sel]
[/markall] [/options] [/reset] [/up] [/wild | /regex] [/word]
```

## <a name="arguments"></a>Arguments
 `findwhat` Gerekli. Eşleştirilecek metin.

## <a name="switches"></a>Anahtarlar
 /Case veya /c isteğe bağlı. Eşleşme gerçekleşmesi yalnızca büyük ve küçük harfleri tam olarak belirtilen platformlarla eşleşen `findwhat` bağımsız değişken.

 / doc veya /d isteğe bağlı. Yalnızca geçerli belgede arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.

 /markall veya /m isteğe bağlı. Geçerli belge içinde bir arama eşleşme içeren her satırda bir grafik yerleştirir.

 /Open veya /o isteğe bağlı. Bir belge değilmiş gibi tüm açık belgeleri arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.

 / Options veya /t isteğe bağlı. Geçerli bulma seçeneği ayarları listesini görüntüler ve arama yapmaz.

 /proc veya /p isteğe bağlı. Yalnızca geçerli yordamı arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.

 Reset veya /e isteğe bağlı. Bulma seçenekleri varsayılan ayarlarına geri döndürür ve bir arama yapmaz.

 /sel veya /s isteğe bağlı. Yalnızca geçerli seçimi arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.

 /UP veya /u isteğe bağlı. Dosyanın başına doğru dosyasındaki geçerli konumda arar. Varsayılan olarak geçerli konumda dosyanın sonuna doğru arar ve dosya aramaları başlar.

 /Regex veya /r isteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak sabit karakterleriyle yerine metin desenleri temsil eden gösterimler. Normal ifade karakterleri tam bir listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).

 /wild veya/l isteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak bir karakter ya da dizi karakteri temsil etmek için gösterimler.

 /Word veya /w isteğe bağlı. Yalnızca için tam sözcükleri arar.

## <a name="example"></a>Örnek
 Bu örnek, şu anda seçili kod bölümünde "somestring" sözcüğü için büyük küçük harfe duyarlı bir arama gerçekleştirir.

```cmd
>Edit.Find somestring /sel /case
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)