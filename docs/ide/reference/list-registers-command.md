---
title: Yazmaçları Listele Komutu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 83e79829caea30ece2c427d851b68d74bf9c586e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54943045"
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