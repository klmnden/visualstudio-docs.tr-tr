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
ms.openlocfilehash: 5549bd0047b38ef8f0dff5fa420d4b5ce0ae4ce9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62790267"
---
# <a name="find-in-files-command"></a>Dosyalarda Bul Komutu
Arama bulunan seçenekler kümesini kullanarak dosyaları **dosyalarda Bul** sekmesinde **Bul ve Değiştir** penceresi.

## <a name="syntax"></a>Sözdizimi

```cmd
Edit.FindinFiles findwhat [/case] [/ext:extensions]
[/lookin:searchpath] [/names] [/options] [/reset] [/stop] [/sub]
[/text2] [/wild|/regex] [/word]
```

## <a name="arguments"></a>Arguments
 `findwhat` Gerekli. Eşleştirilecek metin.

## <a name="switches"></a>Anahtarlar
 /Case veya /c isteğe bağlı. Eşleşme gerçekleşmesi yalnızca büyük ve küçük harfleri tam olarak belirtilen platformlarla eşleşen `findwhat` bağımsız değişken.

 /ext: `extensions` İsteğe bağlı. Aratılmak üzere dosyalar için dosya uzantılarını belirtir. Bir daha önce girildiyse belirtilmezse, önceki uzantıyı kullanılır.

 /lookin: `searchpath` İsteğe bağlı. Aranacak dizini. Yol boşluklar içeriyorsa, yolun tamamını tırnak içine alın.

 /Names veya /n isteğe bağlı. Eşleşmeleri dosya adlarının bir listesini görüntüler.

 / Options veya /t isteğe bağlı. Geçerli bulma seçeneği ayarları listesini görüntüler ve arama yapmaz.

 /Regex veya /r isteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak sabit karakterleriyle yerine metin desenleri temsil eden gösterimler. Normal ifade karakterleri tam bir listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).

 Reset veya /e isteğe bağlı. Bulma seçenekleri varsayılan ayarlarına geri döndürür ve bir arama yapmaz.

 / İsteğe bağlı durdurun. Devam eden ise geçerli arama işlemini durdurur. Arama, diğer tüm bağımsız değişkenleri göz ardı eder, `/stop` belirtilmedi. Örneğin, geçerli aramayı durdurmak için aşağıdaki girmeniz gerekir:

```cmd
>Edit.FindinFiles /stop
```

 / Sub seçeneklerini veya /s isteğe bağlı. Alt klasörleri içinde /lookin belirtilen dizin içinde arar:`searchpath` bağımsız değişken.

 /text2 veya /2 isteğe bağlı. Arama sonuçları Bul sonuçları 2 penceresinde görüntüler.

 /wild veya/l isteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak bir karakter ya da dizi karakteri temsil etmek için gösterimler.

 /Word veya /w isteğe bağlı. Yalnızca için tam sözcükleri arar.

## <a name="example"></a>Örnek
 Bu örnekte "My Visual Studio projeleri" klasöründe yer alan tüm .cls dosyalarında btnCancel arar ve eşleştirme Bilgisi Bul sonuçları 2 penceresinde görüntüler.

```cmd
>Edit.FindinFiles btnCancel /lookin:"c:/My Visual Studio Projects" /ext:*.cls /text2
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Dosyalarda Bul](../../ide/find-in-files.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)