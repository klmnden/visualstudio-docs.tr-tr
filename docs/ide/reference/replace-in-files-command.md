---
title: Dosyalarda Değiştir Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- edit.replaceinfiles
helpviewer_keywords:
- Edit.ReplaceInFiles command
- Replace In Files command
- ReplaceInFiles command
ms.assetid: f116066a-4f65-4f2c-94ef-12cbd8cfb598
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a87b4dcff0bd626947a0d98822150d03fc7c7059
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55935660"
---
# <a name="replace-in-files-command"></a>Dosyalarda Değiştir Komutu
Metin dosyalarında bulunan seçenekler kümesini kullanarak değiştirir **dosyalarda Değiştir** sekmesinde **Bul ve Değiştir** penceresi.

## <a name="syntax"></a>Sözdizimi

```
Edit.ReplaceinFiles findwhat replacewith [/all] [/case]
[/ext:extensions] [/keep] [/lookin:searchpath] [/options] [/regex]
[/reset] [/stop] [/sub] [/text2] [/wild] [/word]
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

 /ext: `extensions`

 İsteğe bağlı. Aratılmak üzere dosyalar için dosya uzantılarını belirtir.

 /Keep veya /k

 İsteğe bağlı. Tüm değiştirilen dosyaları açık bırakılan olduğunu belirtir.

 /lookin: `searchpath`

 İsteğe bağlı. Aranacak dizini. Yol boşluklar içeriyorsa, yolun tamamını tırnak içine alın.

 / Options veya /t

 İsteğe bağlı. Geçerli bulma seçeneği ayarları listesini görüntüler ve arama yapmaz.

 /Regex veya /r

 İsteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak sabit karakterleriyle yerine metin desenleri temsil eden gösterimler. Normal ifade karakterleri tam bir listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).

 Reset veya /e

 İsteğe bağlı. Bulma seçenekleri varsayılan ayarlarına geri döndürür ve bir arama yapmaz.

 / stop

 İsteğe bağlı. Devam eden ise geçerli arama işlemini durdurur. Değiştir, diğer tüm bağımsız değişkenleri göz ardı eder, `/stop` belirtilmedi. Örneğin, geçerli değişiklik durdurmak için aşağıdaki girmeniz gerekir:

```
>Edit.ReplaceinFiles /stop
```

 / Sub seçeneklerini veya /s

 İsteğe bağlı. Alt klasörleri içinde /lookin belirtilen dizin içinde arar:`searchpath` bağımsız değişken.

 /text2 veya /2

 İsteğe bağlı. Değiştirme işleminde sonuçlarını görüntüler **Bul sonuçları 2** penceresi.

 /wild veya/l

 İsteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak bir karakter ya da dizi karakteri temsil etmek için gösterimler.

 /Word veya /w

 İsteğe bağlı. Yalnızca tam sözcükleri arar.

## <a name="example"></a>Örnek
 Bu örnekte arar `btnCancel` ve ile değiştirir `btnReset` tüm .cls dosyaları, "visual studio Projelerim" klasöründe ve değiştirilen bilgileri görüntüler **Bul sonuçları 2** penceresi.

```
>Edit.ReplaceinFiles btnCancel btnReset /lookin:"c:/my visual studio projects" /ext:.cls /text2
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Metin Bulma ve Değiştirme](../../ide/finding-and-replacing-text.md)
- [Dosyalarda Değiştir](../../ide/replace-in-files.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)