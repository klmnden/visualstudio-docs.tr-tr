---
title: Sayı Tabanını Ayarla Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- debug.setradix
helpviewer_keywords:
- Set Radix command
- Debug.SetRadix command
ms.assetid: 6ffd1554-7530-4da4-b5f5-e276a5034f3b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 70b61dff4ebe7486c2e04e4fd3061cd4110feca1
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55938403"
---
# <a name="set-radix-command"></a>Sayı Tabanını Ayarla Komutu
Tamsayı değerleri görüntülemek için kullanılan sayısal taban döndürür veya ayarlar.

## <a name="syntax"></a>Sözdizimi

```cmd
Debug.SetRadix [10 | 16 | hex | dec]
```

## <a name="arguments"></a>Arguments
 `10` veya `16` veya `hex` veya `dec`

 İsteğe bağlı. Ondalık gösterir (10 veya Ara) ya da onaltılık (16 veya onaltılık). Ardından bir bağımsız değişken yoksayılırsa geçerli taban değeri döndürülür.

## <a name="example"></a>Örnek
 Bu örnek, tamsayı değerlerini onaltılık biçimde görüntülemek için ortamı ayarlar.

```cmd
>Debug.SetRadix hex
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)