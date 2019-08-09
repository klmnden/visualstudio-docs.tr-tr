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
ms.openlocfilehash: eb121962bbfd61dc4d4aac84467a2a8659918b63
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926114"
---
# <a name="replace-in-files-command"></a>Dosyalarda Değiştir Komutu
Dosyalardaki metni **Bul ve Değiştir** penceresinin **dosyaları değiştir** sekmesinde bulunan seçeneklerin bir alt kümesini kullanarak değiştirir.

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

Gerekli. Eşleşen metnin yerine konacak metin.

## <a name="switches"></a>Anahtarlar
/All veya/a

İsteğe bağlı. Arama metninin tüm oluşumlarını değiştirme metniyle değiştirir.

/Case veya/c

İsteğe bağlı. Eşleşmeler yalnızca büyük ve küçük harfli karakterlerin `findwhat` bağımsız değişkende belirtilen olanlarla tam olarak eşleşmesi durumunda oluşur.

leri`extensions`

İsteğe bağlı. Aranacak dosyalar için dosya uzantılarını belirtir.

/Keep veya/k

İsteğe bağlı. Değiştirilen tüm dosyaların açık kaldığını belirtir.

aramakonumu`searchpath`

İsteğe bağlı. Aranacak dizin. Yol boşluk içeriyorsa, tüm yolu tırnak işaretleri içine alın.

/Options veya/t

İsteğe bağlı. Geçerli bulma seçeneği ayarlarının listesini görüntüler ve arama yapmaz.

/Regex veya/r

İsteğe bağlı. `findwhat` Bağımsız değişkende önceden tanımlanmış özel karakterleri, değişmez karakterler yerine metin desenlerini temsil eden gösterimler olarak kullanır. Normal ifade karakterlerinin tüm listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).

/Reset süpürmeden veya/e

İsteğe bağlı. Bulma seçeneklerini varsayılan ayarlarına döndürür ve arama yapmaz.

/Stop

İsteğe bağlı. Devam eden bir işlem varsa geçerli arama işlemini durdurur. Değiştirme belirtildiğinde diğer tüm bağımsız değişkenleri `/stop` yoksayar. Örneğin, geçerli değişikliği durdurmak için şunu girin:

```
>Edit.ReplaceinFiles /stop
```

/Sub seçeneklerini veya/s

İsteğe bağlı. /Lookin:`searchpath` bağımsız değişkeninde belirtilen dizin içindeki alt klasörleri arar.

/text2 veya/2

İsteğe bağlı. Değişiklik **sonuçları 2** penceresinde değiştirme işleminin sonuçlarını görüntüler.

/joker veya/l

İsteğe bağlı. Bağımsız değişkende, `findwhat` bir karakter veya karakter dizisini temsil etmek için önceden tanımlanmış özel karakterleri gösterimler olarak kullanır.

/Word veya/w

İsteğe bağlı. Yalnızca tam sözcükleri arar.

## <a name="example"></a>Örnek
Bu örnek, " `btnCancel` My Visual Studio Projects `btnReset` " klasöründe bulunan tüm. CLS dosyalarında bunu arar ve yerini alır ve **sonuçları bul 2** penceresinde değiştirme bilgilerini görüntüler.

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