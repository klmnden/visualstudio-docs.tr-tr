---
title: Yeni Öğe Ekle Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- project.addnewitem
helpviewer_keywords:
- Add New Item command
- File.AddNewItem command
ms.assetid: 63b7df32-db83-463b-bbe7-7ff011fe5298
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6a73bd7008e0058fe984fcb708c92c2bd983d427
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919365"
---
# <a name="add-new-item-command"></a>Yeni Öğe Ekle Komutu
Geçerli çözüme .htm, .css, .txt veya frameset gibi yeni bir çözüm öğesi ekler ve onu açar.

## <a name="syntax"></a>Sözdizimi

```cmd
File.AddNewItem [filename] [/t:templatename] [/e:editorname]
```

## <a name="arguments"></a>Arguments
`filename`\
İsteğe bağlı. Çözüme eklenecek öğenin yolu ve dosya adı.

## <a name="switches"></a>Anahtarlar
/t`templatename`\
İsteğe bağlı. Oluşturulacak dosyanın türünü belirtir. Şablon adı verilmezse, varsayılan olarak bir metin dosyası oluşturulur.

/T:`templatename` Argument sözdizimi, **yeni çözüm öğesi Ekle** iletişim kutusunda bulunan bilgileri yansıtır. Kategori adını dosya türünden bir ters eğik çizgi (`\`) ile ayırarak ve tüm dizeyi tırnak işaretleri içine alarak, tam kategoriyi ve ardından dosya türünü girmeniz gerekir.

Örneğin, yeni bir metin dosyası oluşturmak için/t:`templatename` Argument için aşağıdakini girersiniz.

```cmd
/t:"General\Style Sheet"
```

/e`editorname`\
İsteğe bağlı. Dosyanın açıldığı düzenleyicinin adı. Bağımsız değişken belirtilmişse ancak düzenleyici adı sağlanmadığında, **birlikte Aç** iletişim kutusu görüntülenir.

/E:`editorname` Argument sözdizimi, **birlikte Aç iletişim kutusunda**göründükleri gibi, tırnak işaretleri içine alınan düzenleyici adlarını kullanır.

Örneğin, kaynak kodu düzenleyicisinde bir stil sayfası açmak için/e:`editorname` Argument için aşağıdakini girersiniz.

```cmd
/e:"Source Code (text) Editor"
```

## <a name="example"></a>Örnek
Bu örnek, geçerli çözüme MyHTMLpg adlı yeni bir çözüm öğesi ekler.

```cmd
>File.AddNewItem MyHTMLpg /t:"General\HTML Page"
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)