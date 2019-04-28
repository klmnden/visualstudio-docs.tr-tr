---
title: Dosya Aç Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- file.openfile
helpviewer_keywords:
- Open File command
- File.OpenFile command
- of command
ms.assetid: a51a83fc-e3c6-4fa2-8882-8b7b6c0a6406
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b76db52534f4c264e065152548d49f9773863a29
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62995238"
---
# <a name="open-file-command"></a>Dosya Aç komutu

Varolan bir dosyayı açar ve bir düzenleyici belirtmenize olanak tanır.

## <a name="syntax"></a>Sözdizimi

```cmd
File.OpenFile filename [/e:editorname]
```

## <a name="arguments"></a>Arguments

`filename`

Gerekli. Tam veya kısmi yolu ve dosya adını dosyayı açın. Boşluk içeren yolları tırnak içine alınmalıdır.

## <a name="switches"></a>Anahtarlar

/ e:`editorname`

İsteğe bağlı. Dosyanın açılmasını düzenleyicinin adı. Bağımsız değişken belirtildi, ancak hiçbir Düzenleyici adı verilmesi, **birlikte Aç** iletişim kutusu görüntülenir.

/ E:`editorname` bağımsız değişkeni sözdizimini açık ile iletişim kutusunda tırnak işaretleri arasına göründükleri gibi Düzenleyicisi adları kullanır.

Örneğin, bir dosya kaynak kod Düzenleyicisi'nde açmak için / e: şunları girersiniz`editorname` bağımsız değişken.

```cmd
/e:"Source Code (text) Editor"
```

## <a name="remarks"></a>Açıklamalar

Bir yol girin gibi doğru yol ve dosya adı bulmak otomatik tamamlama çalışır.

## <a name="example"></a>Örnek

Bu örnek, Kaynak Kod Düzenleyicisi'nde "Test1.css" stil dosyasını açar.

```cmd
>File.OpenFile "C:\My Projects\project1\Test1.css" /e:"Source Code (text) Editor"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)
- [Komut penceresi](../../ide/reference/command-window.md)
- [Komut penceresi](../../ide/reference/immediate-window.md)
- [Bul/komut kutusu](../../ide/find-command-box.md)
- [Visual Studio komut diğer adları](../../ide/reference/visual-studio-command-aliases.md)