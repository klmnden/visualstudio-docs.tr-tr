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
ms.openlocfilehash: 3de5b1b5add1337451d7b6a463c89951754e3581
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55942576"
---
# <a name="replace-command"></a>Değiştir Komutu
Metin dosyalarında bulunan seçenekler kümesini kullanarak değiştirir **dosyalarda Değiştir** sekmesinde **Bul ve Değiştir** penceresi.

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

 Gerekli. Eşleşen metni eklenecek metin.

## <a name="switches"></a>Anahtarlar
 / all veya /a

 İsteğe bağlı. Arama metni tüm oluşumlarını değiştirme metni ile değiştirir.

 /Case veya /c

 İsteğe bağlı. Eşleşme gerçekleşmesi yalnızca zaman büyük ve küçük harfleri tam olarak belirtilen platformlarla eşleşen `findwhat` bağımsız değişken.

 / doc veya /d

 İsteğe bağlı. Yalnızca geçerli belgede arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.

 / Gizli veya/h

 İsteğe bağlı. Bir tasarım zamanı denetimi, gizli bir bölge anahatları belirlenmiş bir belge veya bir daraltılmış sınıf veya yöntemin meta verilerini gibi altına gizlenmiş ve daraltılmış metin araması yapar.

 /Open veya /o

 İsteğe bağlı. Bir belge değilmiş gibi tüm açık belgeleri arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.

 / Options veya /t

 İsteğe bağlı. Geçerli bulma seçeneği ayarları listesini görüntüler ve arama yapmaz.

 /proc veya /p

 İsteğe bağlı. Yalnızca geçerli yordamı arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.

 /Regex veya /r

 İsteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak sabit karakterleriyle yerine metin desenleri temsil eden gösterimler. Normal ifade karakterleri tam bir listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).

 Reset veya /e

 İsteğe bağlı. Bulma seçenekleri varsayılan ayarlarına geri döndürür ve bir arama yapmaz.

 /sel veya /s

 İsteğe bağlı. Yalnızca geçerli seçimi arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.

 /UP veya /u

 İsteğe bağlı. Dosyanın üst tarafındaki dosya geçerli konumda arar. Varsayılan olarak, dosya ve İlerle dosyasının en altına doğru geçerli konumu aramaları başlar.

 /wild veya/l

 İsteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak bir karakter ya da dizi karakteri temsil etmek için gösterimler.

 /Word veya /w

 İsteğe bağlı. Yalnızca için tam sözcükleri arar.

## <a name="example"></a>Örnek
 Bu örnekte değiştirir `btnSend` ile `btnSubmit` tüm açık belgeleri.

```
>Edit.Replace btnSend btnSubmit /open
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Metin Bulma ve Değiştirme](../../ide/finding-and-replacing-text.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)