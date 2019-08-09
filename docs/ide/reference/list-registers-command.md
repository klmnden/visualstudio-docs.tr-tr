---
title: Yazmaçları Listele Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- debug.listregisters
helpviewer_keywords:
- list registers command
- Debug.ListRegisters command
- ListRegisters command
ms.assetid: 19a9d789-f6c9-46b3-b1f6-4934fc33e055
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 95edb5098d73e8fccb47f9f059473394afe5f542
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919107"
---
# <a name="list-registers-command"></a>Yazmaçları Listele Komutu
Seçili yazmaçların değerini görüntüler ve gösterilecek kayıt listesini değiştirmenize izin verir.

## <a name="syntax"></a>Sözdizimi

```cmd
Debug.ListRegisters [/Display [{register|registerGroup}...]] [/List]
[/Watch [{register|registerGroup}...]]
[/Unwatch [{register|registerGroup}...]]
```

## <a name="switches"></a>Anahtarlar
/Display [{`register`&#124;`registerGroup`}...]

Belirtilen `register` veya`registerGroup`değerlerini görüntüler. `register` Veya`registerGroup` belirtilmemişse, varsayılan kayıt listesi görüntülenir. Anahtar belirtilmemişse, davranış aynıdır. Örneğin:

`Debug.ListRegisters /Display eax`

eşdeğerdir

`Debug.ListRegisters eax`

/List

Listedeki tüm kayıt gruplarını görüntüler.

/Watch [{`register`&#124;`registerGroup`}...]

Listeye bir veya daha `register` fazla `registerGroup` veya değer ekler.

/Unwatch [{`register`&#124;`registerGroup`}...]

Listeden bir veya daha `register` fazla `registerGroup` veya değeri kaldırır.

## <a name="remarks"></a>Açıklamalar
Diğer ad `r` , yerine kullanılabilir `Debug.ListRegisters`.

## <a name="example"></a>Örnek
Bu örnek, `Debug.ListRegisters` yazmaç grubunun `r` `Flags`değerlerini göstermek için diğer adı kullanır.

```cmd
r /Display Flags
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Hata Ayıklamanın Temelleri: Yazmaçlar Penceresi](../../debugger/debugging-basics-registers-window.md)
- [Nasıl yapılır: Yazmaçlar Penceresi Hakkında](../../debugger/how-to-use-the-registers-window.md)