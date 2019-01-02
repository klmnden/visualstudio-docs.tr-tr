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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 942ab10a1d660ea5e33ca2cb679e4655bd6b3fbc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53959971"
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
 / Görüntüleme [{`register`&#124;`registerGroup`}...]

 Belirtilen değerleri görüntüler `register` veya `registerGroup`. Hayır ise `register` veya `registerGroup` belirtilirse, kayıtları varsayılan listesi görüntülenir. Hiçbir anahtarı belirtilmişse davranışı aynıdır. Örneğin:

 `Debug.ListRegisters /Display eax`

 eşdeğerdir

 `Debug.ListRegisters eax`

 / Listeleme

 YAZMAÇ grupları listesinde tüm görüntüler.

 / İzleme [{`register`&#124;`registerGroup`}...]

 Bir veya daha fazla ekler `register` veya `registerGroup` değerleri listesi.

 / Unwatch [{`register`&#124;`registerGroup`}...]

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
- [Hata ayıklama temelleri: Yazmaçlar penceresi](../../debugger/debugging-basics-registers-window.md)
- [Nasıl yapılır: Yazmaçlar penceresini kullanma](../../debugger/how-to-use-the-registers-window.md)