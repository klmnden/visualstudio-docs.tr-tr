---
title: Yeni Öğe Ekle Komutu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- project.addnewitem
helpviewer_keywords:
- Add New Item command
- File.AddNewItem command
ms.assetid: 63b7df32-db83-463b-bbe7-7ff011fe5298
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8c094e30c9491783733e49901fb297c36c1e94f9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53952478"
---
# <a name="add-new-item-command"></a>Yeni Öğe Ekle Komutu
Geçerli çözüme .htm, .css, .txt veya frameset gibi yeni bir çözüm öğesi ekler ve onu açar.

## <a name="syntax"></a>Sözdizimi

```cmd
File.AddNewItem [filename] [/t:templatename] [/e:editorname]
```

## <a name="arguments"></a>Arguments
 `filename` İsteğe bağlı. Çözüme eklenecek öğe yolu ve dosya adı.

## <a name="switches"></a>Anahtarlar
 / t: `templatename` İsteğe bağlı. Oluşturulacak dosya türünü belirtir. Hiçbir şablon adı belirtilmezse, varsayılan olarak bir metin dosyası oluşturulur.

 / T:`templatename` bağımsız değişken söz dizimi içinde bulunan bilgileri yansıtır **yeni çözüm Öğe Ekle** iletişim kutusu. Dosya türü kategori adı bir ters eğik çizgi dosya türünü ayırmak, ardından tam kategori girmeniz gerekir (`\`) ve tırnak dizenin tamamını kapsayan.

 Örneğin, yeni bir metin dosyası oluşturmak için / t: şunları girersiniz`templatename` bağımsız değişken.

```cmd
/t:"General\Style Sheet"
```

 / e: `editorname` İsteğe bağlı. Dosyanın açılmasını Düzenleyicisi adı. Bağımsız değişken belirtildi, ancak hiçbir Düzenleyici adı verilmesi, **birlikte Aç** iletişim kutusu görüntülenir.

 / E:`editorname` bağımsız değişkeni sözdizimini kullanan Düzenleyicisi adları gibi görünürler **ile iletişim kutusunu açma**tırnak işareti içine alınan.

 Örneğin, bir stil sayfası Kaynak Kod Düzenleyicisi'nde açmak için / e: şunları girersiniz`editorname` bağımsız değişken.

```cmd
/e:"Source Code (text) Editor"
```

## <a name="example"></a>Örnek
 Bu örnek, yeni bir çözüm öğesi MyHTMLpg, geçerli çözüme ekler.

```cmd
>File.AddNewItem MyHTMLpg /t:"General\HTML Page"
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)