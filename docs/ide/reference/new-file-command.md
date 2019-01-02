---
title: Yeni Dosya Komutu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- file.newfile
helpviewer_keywords:
- File.NewFile command
- New File command
ms.assetid: 767868d6-a525-425b-a43b-2198f636ab6b
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: eb4ccae573813811567033dfa574c94e1bf809b3
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53932122"
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