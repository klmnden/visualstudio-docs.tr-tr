---
title: Varolan Projeyi Ekle Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- file.addexistingproject
helpviewer_keywords:
- Add Existing Project command
- File.AddExistingProject
ms.assetid: 71cf3e31-c76b-405b-ad6a-1b1bc654bd40
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d0946efb15758c76c078ff234717af6fd1fac15c
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55951637"
---
# <a name="add-existing-project-command"></a>Varolan Projeyi Ekle Komutu
Mevcut bir projeyi çözüme ekler.

## <a name="syntax"></a>Sözdizimi

```cmd
File.AddExistingProject filename
```

## <a name="arguments"></a>Arguments
 `filename` İsteğe bağlı. Tam yol ve proje adı, çözüme eklemek için projenin bir uzantıya sahip.

 Varsa `filename` bağımsız değişken boşluk içeriyorsa, tırnak işaretleri içine alınmalıdır.

 Dosya adı belirtilirse, bu kullanıcı, bir proje seçebilir böylece komut dosya iletişim kutusu açılır.

## <a name="remarks"></a>Açıklamalar
 Otomatik Tamamlama, doğru yol ve dosya adı, türü bulmaya çalışır.

## <a name="example"></a>Örnek
 Bu örnek ekler [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)] proje, TestProject1, geçerli çözüme.

```cmd
>File.AddExistingProject "c:\visual studio projects\TestProject1.vbproj"
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)