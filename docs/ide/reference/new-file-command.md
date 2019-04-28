---
title: Yeni Dosya Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- file.newfile
helpviewer_keywords:
- File.NewFile command
- New File command
ms.assetid: 767868d6-a525-425b-a43b-2198f636ab6b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9d6707d2e9ed8e001762939cb08ffee58f1c1cdc
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62950906"
---
# <a name="new-file-command"></a>Yeni Dosya Komutu
Yeni bir dosya oluşturur ve onu açar. Dosyanın çeşitli dosyalar klasörü altında görünür.

## <a name="syntax"></a>Sözdizimi

```cmd
File.NewFile [filename] [/t:templatename] [/editor:editorname]
```

## <a name="arguments"></a>Arguments
 `filename`

 İsteğe bağlı. Dosyanın adı. Adı sağlanmazsa, varsayılan adı sağlanır. Hiçbir şablon adı listede yoksa, bir metin dosyası oluşturulur.

## <a name="switches"></a>Anahtarlar
 / t:`templatename`

 İsteğe bağlı. Oluşturulacak dosya türünü belirtir.

 / T:`templatename` bağımsız değişkeni sözdizimini yeni dosya iletişim kutusunda bulunan bilgileri yansıtır. Ardından bir eğik kategori adı girin (`\`) ve şablon adı ve tüm dizeyi tırnak içine alın.

 Örneğin, yeni bir [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] kaynak dosyası, / t: şunları girersiniz`templatename` bağımsız değişken.

```cmd
/t:"Visual C++\C++ File (.cpp)"
```

 Yukarıdaki örnekte C++ dosyası şablonu Visual C++ kategorisi altında bulunduğunu gösterir **yeni dosya** iletişim kutusu.

 / e:`editorname`

 İsteğe bağlı. Dosyanın açılmasını düzenleyicinin adı. Bağımsız değişken belirtildi, ancak hiçbir Düzenleyici adı verilmesi, **birlikte Aç** iletişim kutusu görüntülenir.

 / E:`editorname` bağımsız değişkeni sözdizimini açık ile iletişim kutusunda tırnak işaretleri arasına göründükleri gibi Düzenleyicisi adları kullanır.

 Örneğin, bir dosya kaynak kod Düzenleyicisi'nde açmak için / e: şunları girersiniz`editorname` bağımsız değişken.

```cmd
/e:"Source Code (text) Editor"
```

## <a name="example"></a>Örnek
 Bu örnek, yeni bir web sayfası "test1.htm" oluşturur ve Kaynak Kod Düzenleyicisi'nde açılır.

```cmd
>File.NewFile test1 /t:"General\HTML Page" /e:"Source Code (text) Editor"
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Komut Penceresi](../../ide/reference/immediate-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)