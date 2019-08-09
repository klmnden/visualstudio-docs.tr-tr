---
title: Değiştir Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- edit.replace
helpviewer_keywords:
- Edit.Replace command
- Replace command
ms.assetid: a15767f1-5a3d-44f5-8c77-7b0f1157f340
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: edcff51428451b50dc149b7b55cee11cb9ede853
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919040"
---
# <a name="replace-command"></a>Değiştir Komutu
Dosyalardaki metni **Bul ve Değiştir** penceresinin **dosyaları değiştir** sekmesinde bulunan seçeneklerin bir alt kümesini kullanarak değiştirir.

## <a name="syntax"></a>Sözdizimi

```
Edit.Replace findwhat replacewith [/all] [/case]
[/doc|/proc|/open|/sel] [/hidden] [/options] [/reset] [/up]
[/wild|/regex] [/word]
```

## <a name="arguments"></a>Arguments
`findwhat`

Gerekli. Eşleştirilecek metin.

`replacewith`

Gerekli. Eşleşen metnin yerine konacak metin.

## <a name="switches"></a>Anahtarlar
/All veya/a

İsteğe bağlı. Arama metninin tüm oluşumlarını değiştirme metniyle değiştirir.

/Case veya/c

İsteğe bağlı. Eşleşmeler yalnızca büyük ve küçük harfli karakterlerin `findwhat` bağımsız değişkende belirtilen olanlarla tam olarak eşleşmesi durumunda oluşur.

/doc veya/d

İsteğe bağlı. Yalnızca geçerli belgeyi arar. Kullanılabilir `/doc`arama kapsamlarından `/proc` `/open`yalnızca birini belirtin,,, veya `/sel`.

/Hidden veya/h

İsteğe bağlı. Tasarım zamanı denetiminin meta verileri, ana hatlı bir belgenin gizli bir bölgesi veya daraltılmış bir sınıf veya yöntem gibi gizli ve daraltılmış metinleri arar.

/Open veya/o

İsteğe bağlı. Tüm açık belgeleri bir belge gibi arar. Kullanılabilir `/doc`arama kapsamlarından `/proc` `/open`yalnızca birini belirtin,,, veya `/sel`.

/Options veya/t

İsteğe bağlı. Geçerli bulma seçeneği ayarlarının listesini görüntüler ve arama yapmaz.

/proc veya/p

İsteğe bağlı. Yalnızca geçerli yordamı arar. Kullanılabilir `/doc`arama kapsamlarından `/proc` `/open`yalnızca birini belirtin,,, veya `/sel`.

/Regex veya/r

İsteğe bağlı. `findwhat` Bağımsız değişkende önceden tanımlanmış özel karakterleri, değişmez karakterler yerine metin desenlerini temsil eden gösterimler olarak kullanır. Normal ifade karakterlerinin tüm listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).

/Reset süpürmeden veya/e

İsteğe bağlı. Bulma seçeneklerini varsayılan ayarlarına döndürür ve arama yapmaz.

/sel or/s

İsteğe bağlı. Yalnızca geçerli seçimi arar. Kullanılabilir `/doc`arama kapsamlarından `/proc` `/open`yalnızca birini belirtin,,, veya `/sel`.

/up veya/u

İsteğe bağlı. Dosyadaki geçerli konumdan dosyanın en üstüne doğru arar. Varsayılan olarak, aramalar dosyadaki geçerli konumda başlar ve dosyanın alt kısmına doğru ilerler.

/joker veya/l

İsteğe bağlı. Bağımsız değişkende, `findwhat` bir karakter veya karakter dizisini temsil etmek için önceden tanımlanmış özel karakterleri gösterimler olarak kullanır.

/Word veya/w

İsteğe bağlı. Yalnızca tam sözcükleri arar.

## <a name="example"></a>Örnek
Bu örnek, `btnSend` tüm `btnSubmit` açık belgelerde ile değiştirilir.

```
>Edit.Replace btnSend btnSubmit /open
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Metin Bulma ve Değiştirme](../../ide/finding-and-replacing-text.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)