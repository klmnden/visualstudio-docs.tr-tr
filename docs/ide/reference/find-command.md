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
ms.openlocfilehash: 9e94f8aa823fc7665144f1d774339d1c41f37edc
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926246"
---
# <a name="find-command"></a>Bul Komutu
**Bul ve Değiştir** penceresinin **dosyalarda bul** sekmesinde bulunan seçeneklerin bir alt kümesini kullanarak dosyaları arar.

## <a name="syntax"></a>Sözdizimi

```cmd
Edit.Find findwhat [/case] [/doc | /proc | /open | /sel]
[/markall] [/options] [/reset] [/up] [/wild | /regex] [/word]
```

## <a name="arguments"></a>Arguments
`findwhat`Gerekli. Eşleştirilecek metin.

## <a name="switches"></a>Anahtarlar
/Case veya/C\
İsteğe bağlı. Eşleşmeler yalnızca büyük ve küçük harfli karakterler `findwhat` bağımsız değişkende belirtilen olanlarla tam olarak eşleşiyorsa oluşur.

/doc veya/d\
İsteğe bağlı. Yalnızca geçerli belgeyi arar. Kullanılabilir `/doc`arama kapsamlarından `/proc` `/open`yalnızca birini belirtin,,, veya `/sel`.

/markall veya/M\
İsteğe bağlı. Geçerli belge içinde arama eşleşmesi içeren her satıra bir grafik koyar.

/Open veya/O\
İsteğe bağlı. Tüm açık belgeleri bir belge gibi arar. Kullanılabilir `/doc`arama kapsamlarından `/proc` `/open`yalnızca birini belirtin,,, veya `/sel`.

/Options veya/t \
İsteğe bağlı. Geçerli bulma seçeneği ayarlarının listesini görüntüler ve arama yapmaz.

/proc veya/p\
İsteğe bağlı. Yalnızca geçerli yordamı arar. Kullanılabilir `/doc`arama kapsamlarından `/proc` `/open`yalnızca birini belirtin,,, veya `/sel`.

/Reset süpürmeden veya/e\
İsteğe bağlı. Bulma seçeneklerini varsayılan ayarlarına döndürür ve arama yapmaz.

/sel veya/s\
İsteğe bağlı. Yalnızca geçerli seçimi arar. Kullanılabilir `/doc`arama kapsamlarından `/proc` `/open`yalnızca birini belirtin,,, veya `/sel`.

/up veya/U\
İsteğe bağlı. Dosyadaki geçerli konumdan dosyanın başlangıcına doğru arar. Varsayılan olarak, aramalar dosyadaki geçerli konumda başlar ve dosyanın sonuna doğru arar.

/Regex veya/r \
İsteğe bağlı. `findwhat` Bağımsız değişkende önceden tanımlanmış özel karakterleri, değişmez karakterler yerine metin desenlerini temsil eden gösterimler olarak kullanır. Normal ifade karakterlerinin tüm listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).

/joker veya/L\
İsteğe bağlı. Bağımsız değişkende, `findwhat` bir karakter veya karakter dizisini temsil etmek için önceden tanımlanmış özel karakterleri gösterimler olarak kullanır.

/Word veya/w\
İsteğe bağlı. Yalnızca tam sözcükleri arar.

## <a name="example"></a>Örnek
Bu örnek, kodun Şu anda seçili olan bölümünde "somestring" sözcüğü için büyük/küçük harfe duyarlı bir arama gerçekleştirir.

```cmd
>Edit.Find somestring /sel /case
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)