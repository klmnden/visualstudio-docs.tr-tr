---
title: Git Komutu
ms.date: 11/04/2016
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
ms.openlocfilehash: 82dd3f226931dfeca2fa0dfad38daa24684fb8da
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55947438"
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