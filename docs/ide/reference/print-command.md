---
title: Debug.Print
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- debug.print
helpviewer_keywords:
- Debug.Print command
- Print method
- Print command
ms.assetid: 0412d381-590a-483f-bab4-6e1cca095645
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: df609011250cebc097d3d356242302dbe41f8007
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62969091"
---
# <a name="print-command"></a>Yazdır komutu

Bir ifadeyi değerlendirir veya belirtilen metni görüntüler.

## <a name="syntax"></a>Sözdizimi

```cmd
>Debug.Print text
```

## <a name="arguments"></a>Arguments

`text`

Gerekli. Değerlendirilecek ifade veya görüntülenecek metin.

## <a name="remarks"></a>Açıklamalar

Bu komut için bir diğer ad olarak, soru işareti (?) kullanabilirsiniz. Bunu, örneğin, komut

```cmd
>Debug.Print expA
```

olarak yazılabilir

```cmd
? expA
```

Bu komutun her iki sürümü ifadenin geçerli değerini döndürmek `expA`.

## <a name="example"></a>Örnek

```cmd
>Debug.Print DateTime.Now.Day
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Deyimi Değerlendir Komutu](../../ide/reference/evaluate-statement-command.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)