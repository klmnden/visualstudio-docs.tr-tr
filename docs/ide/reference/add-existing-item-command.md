---
title: Varolan Öğeyi Ekle Komutu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- project.addexistingitem
helpviewer_keywords:
- File.AddExistingItem command
- Add Existing Item command
ms.assetid: 41f56131-d4c7-4f81-83b7-bdac713ea870
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: aaa9784b40b02ba726b1bcc4b82e0708223fb283
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55039637"
---
# <a name="add-existing-item-command"></a>Varolan Öğeyi Ekle Komutu
Geçerli çözüme var olan bir dosya ekler ve onu açar.

## <a name="syntax"></a>Sözdizimi

```cmd
File.AddExistingItem filename [/e:editorname]
```

## <a name="arguments"></a>Arguments
 `filename` Gerekli. Tam yol ve dosya adı, geçerli çözüme eklenecek öğe uzantısına sahip. Dosya yolu veya dosya adı boşluk içeriyorsa, yolun tamamını tırnak içine alın.

## <a name="switches"></a>Anahtarlar
 / e: `editorname` İsteğe bağlı. Dosyanın açılmasını düzenleyicinin adı. Bağımsız değişken belirtildi, ancak hiçbir Düzenleyici adı verilmesi, **birlikte Aç** iletişim kutusu görüntülenir.

 / E:`editorname` bağımsız değişkeni sözdizimini kullanan Düzenleyicisi adları gibi görünürler **ile iletişim kutusunu açma**tırnak işareti içine alınan. Örneğin, bir stil sayfası Kaynak Kod Düzenleyicisi'nde açmak için / e: şunları girersiniz`editorname` bağımsız değişken.

```cmd
/e:"Source Code (text) Editor"
```

## <a name="remarks"></a>Açıklamalar
 Otomatik Tamamlama, doğru yol ve dosya adı, türü bulmaya çalışır.

## <a name="example"></a>Örnek
 Bu örnek dosyayı Form1.frm, geçerli çözüme ekler.

```cmd
>File.AddExistingItem "C:\public\solution files\Form1.frm"
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)