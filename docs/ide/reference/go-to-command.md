---
title: Git Komutu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- edit.goto
helpviewer_keywords:
- Debug.Goto command
- Go To command
ms.assetid: 201e1dd2-6701-467d-8cc1-faec2ef20511
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fad99d77c7dc086e3e83f25b9ffea08fe60d914b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55012462"
---
# <a name="go-to-command"></a>Git Komutu
İmleci belirtilen satıra taşır.

## <a name="syntax"></a>Sözdizimi

```cmd
Edit.GoTo [linenumber]
```

## <a name="arguments"></a>Arguments
 `linenumber`

 İsteğe bağlı. Gitmek için satır sayısını temsil eden bir tamsayı.

## <a name="remarks"></a>Açıklamalar
 Satır numaraları tek başlar. Varsa değerini `linenumber` değerden daha az, ilk satır görüntüler. Varsa değerini `linenumber` son satırın son satır görüntüler sayısından büyüktür.

 İçin bir değer `linenumber` belirtilmezse, **satıra Git** iletişim kutusu görüntüler.

 Bu komut diğer GoToLn adıdır.

## <a name="example"></a>Örnek

```cmd
>Edit.GoTo 125
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)