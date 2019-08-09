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
ms.openlocfilehash: 9bdc1c97d35b79fec40bbaf8994176cfbb27b8e8
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919226"
---
# <a name="go-to-command"></a>Git Komutu
İmleci belirtilen satıra taşır.

## <a name="syntax"></a>Sözdizimi

```cmd
Edit.GoTo [linenumber]
```

## <a name="arguments"></a>Arguments
`linenumber`\
İsteğe bağlı. Gidilecek satırın numarasını temsil eden bir tamsayı.

## <a name="remarks"></a>Açıklamalar
Satır numaralandırması bir kerede başlar. Değeri `linenumber` bir değerinden küçükse, ilk satır görüntülenir. Değeri `linenumber` , son satırın sayısından büyükse, son satır görüntülenir.

İçin `linenumber` bir değer belirtilmemişse, **satıra git** iletişim kutusu görüntülenir.

Bu komutun diğer adı Sayfayln 'dir.

## <a name="example"></a>Örnek

```cmd
>Edit.GoTo 125
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)