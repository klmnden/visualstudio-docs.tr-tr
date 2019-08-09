---
title: Dosyalarda Bul Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- edit.findinfiles
helpviewer_keywords:
- Edit.FindInFiles command
- find in files command
ms.assetid: 2fc78bfe-b339-4599-97f9-4cafd8a194d9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2877057f32ba6553a2cdcefbbc1bb7a8bf2884da
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919249"
---
# <a name="find-in-files-command"></a>Dosyalarda Bul Komutu
**Bul ve Değiştir** penceresinin **dosyalarda bul** sekmesinde bulunan seçeneklerin bir alt kümesini kullanarak dosyaları arayın.

## <a name="syntax"></a>Sözdizimi

```cmd
Edit.FindinFiles findwhat [/case] [/ext:extensions]
[/lookin:searchpath] [/names] [/options] [/reset] [/stop] [/sub]
[/text2] [/wild|/regex] [/word]
```

## <a name="arguments"></a>Arguments

`findwhat`\
Gerekli. Eşleştirilecek metin.

## <a name="switches"></a>Anahtarlar
/Case veya/C\
İsteğe bağlı. Eşleşmeler yalnızca büyük ve küçük harfli karakterler `findwhat` bağımsız değişkende belirtilen olanlarla tam olarak eşleşiyorsa oluşur.

leri`extensions`\
İsteğe bağlı. Aranacak dosyalar için dosya uzantılarını belirtir. Belirtilmemişse, önceki uzantı daha önce girilmişse kullanılır.

aramakonumu`searchpath`\
İsteğe bağlı. Aranacak dizin. Yol boşluk içeriyorsa, tüm yolu tırnak işaretleri içine alın.

/Names veya/n\
İsteğe bağlı. Eşleşmeler içeren dosya adlarının listesini görüntüler.

/Options veya/t \
İsteğe bağlı. Geçerli bulma seçeneği ayarlarının listesini görüntüler ve arama yapmaz.

/Regex veya/r \
İsteğe bağlı. `findwhat` Bağımsız değişkende önceden tanımlanmış özel karakterleri, değişmez karakterler yerine metin desenlerini temsil eden gösterimler olarak kullanır. Normal ifade karakterlerinin tüm listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).

/Reset süpürmeden veya/e\
İsteğe bağlı. Bulma seçeneklerini varsayılan ayarlarına döndürür ve arama yapmaz.

/Stop
İsteğe bağlı. Devam eden bir işlem varsa geçerli arama işlemini durdurur. Arama `/stop` , belirtildiğinde diğer tüm bağımsız değişkenleri yoksayar. Örneğin, geçerli aramayı durdurmak için şunu girin:

```cmd
>Edit.FindinFiles /stop
```

/Sub seçeneklerini veya/s\
İsteğe bağlı. /Lookin:`searchpath` bağımsız değişkeninde belirtilen dizin içindeki alt klasörleri arar.

/text2 veya/2 \
İsteğe bağlı. Arama sonuçlarını bul 2 penceresinde görüntüler.

/joker veya/L\
İsteğe bağlı. Bağımsız değişkende, `findwhat` bir karakter veya karakter dizisini temsil etmek için önceden tanımlanmış özel karakterleri gösterimler olarak kullanır.

/Word veya/w\
İsteğe bağlı. Yalnızca tam sözcükleri arar.

## <a name="example"></a>Örnek
Bu örnek, "My Visual Studio Projects" klasöründe bulunan tüm. CLS dosyalarında btnCancel arar ve sonuçları bul 2 penceresinde eşleşme bilgilerini görüntüler.

```cmd
>Edit.FindinFiles btnCancel /lookin:"c:/My Visual Studio Projects" /ext:*.cls /text2
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Dosyalarda Bul](../../ide/find-in-files.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)