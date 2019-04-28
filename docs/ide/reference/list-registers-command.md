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
ms.openlocfilehash: fb1a2361534f167a0b88b3f1b5b38c005915243d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62422971"
---
# <a name="list-registers-command"></a>Yazmaçları Listele Komutu
Seçilen değeri kaydeder ve olanak tanır görüntüler liste kayıtları göstermek için değiştirin.

## <a name="syntax"></a>Sözdizimi

```cmd
Debug.ListRegisters [/Display [{register|registerGroup}...]] [/List]
[/Watch [{register|registerGroup}...]]
[/Unwatch [{register|registerGroup}...]]
```

## <a name="switches"></a>Anahtarlar
 /Display [{`register`&#124;`registerGroup`}...]

 Belirtilen değerleri görüntüler `register` veya `registerGroup`. Hayır ise `register` veya `registerGroup` belirtilirse, kayıtları varsayılan listesi görüntülenir. Hiçbir anahtarı belirtilmişse davranışı aynıdır. Örneğin:

 `Debug.ListRegisters /Display eax`

 eşdeğerdir

 `Debug.ListRegisters eax`

 / Listeleme

 YAZMAÇ grupları listesinde tüm görüntüler.

 / İzleme [{`register`&#124;`registerGroup`}...]

 Bir veya daha fazla ekler `register` veya `registerGroup` değerleri listesi.

 /Unwatch [{`register`&#124;`registerGroup`}...]

 Bir veya daha fazla kaldırır `register` veya `registerGroup` listedeki değerler.

## <a name="remarks"></a>Açıklamalar
 Diğer ad `r` yerine kullanılan `Debug.ListRegisters`.

## <a name="example"></a>Örnek
 Bu örnekte `Debug.ListRegisters` diğer `r` kayıt grubunun değerleri görüntülemek için `Flags`.

```cmd
r /Display Flags
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Hata Ayıklamanın Temelleri: Yazmaçlar Penceresi](../../debugger/debugging-basics-registers-window.md)
- [Nasıl yapılır: Yazmaçlar Penceresi Hakkında](../../debugger/how-to-use-the-registers-window.md)