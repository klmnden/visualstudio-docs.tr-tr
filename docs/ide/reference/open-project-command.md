---
title: Proje Aç komutu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 34a6783e71d2a6dfee718aa441fbb3007aa71fa9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53946246"
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