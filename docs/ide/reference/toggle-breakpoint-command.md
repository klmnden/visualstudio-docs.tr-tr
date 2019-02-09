---
title: Kesim Noktasını Değiştir Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- debug.togglebreakpoint
helpviewer_keywords:
- ToggleBreakpoint command
- Debug.ToggleBreakPoint command
- Toggle Breakpoint command
ms.assetid: d50dfadb-ce79-4d5e-9c09-1cfddd57876d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 214897a0f938d8ea52306b8f605948b38f196111
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55970471"
---
# <a name="toggle-breakpoint-command"></a>Kesim Noktasını Değiştir Komutu
Dosyadaki geçerli konumda geçerli durumuna bağlı olarak kesme noktasını açar veya devre dışı bırakır.

## <a name="syntax"></a>Sözdizimi

```
Debug.ToggleBreakpoint [text]
```

## <a name="arguments"></a>Arguments
 `text` İsteğe bağlı. Metin belirtilmezse, satır adlandırılmış bir kesme noktası işaretlenir. Aksi takdirde, satır F9 tuşuna bastığınızda ne olacağını için benzer olan adlandırılmamış bir kesme noktası işaretlenir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek geçerli kesme noktasını açar veya kapatır.

```
>Debug.ToggleBreakpoint
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)