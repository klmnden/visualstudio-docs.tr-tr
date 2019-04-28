---
title: Proje Aç komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- file.openproject
- file.opensolution
helpviewer_keywords:
- op command
- File.OpenProject command
- Open Project command
ms.assetid: baa85f86-041b-49f4-9ced-0c397dc180e1
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7e9249088b188fde1b346772ab1230d33160fe59
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62996822"
---
# <a name="open-project-command"></a>Proje Aç komutu

Varolan bir projeyi veya çözümü açar.

## <a name="syntax"></a>Sözdizimi

```cmd
File.OpenProject filename
```

## <a name="arguments"></a>Arguments

`filename`

Gerekli. Tam yol ve dosya adı proje veya çözümü açın.

> [!NOTE]
> Sözdizimi `filename` bağımsız değişken gerektiriyor, boşluk içeren yolları tırnak işaretleri kullanın.

## <a name="remarks"></a>Açıklamalar

Otomatik Tamamlama, doğru yol ve dosya adı, türü bulmaya çalışır.

Bu komut hata ayıklama sırasında kullanılamaz.

## <a name="example"></a>Örnek

Aşağıdaki örnek, Visual Basic projesi açılır **Test1**:

```cmd
>File.OpenProject "C:\My Projects\Test1\Test1.vbproj"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)
- [Komut penceresi](../../ide/reference/command-window.md)
- [Bul/komut kutusu](../../ide/find-command-box.md)
- [Visual Studio komut diğer adları](../../ide/reference/visual-studio-command-aliases.md)