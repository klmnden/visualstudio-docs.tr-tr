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
ms.openlocfilehash: 18473fbd8ee0f7c4b415880da61c86de0bae6fc5
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68925968"
---
# <a name="toggle-breakpoint-command"></a>Kesim Noktasını Değiştir Komutu
Dosyadaki geçerli konumda geçerli durumuna bağlı olarak kesme noktasını açar veya devre dışı bırakır.

## <a name="syntax"></a>Sözdizimi

```
Debug.ToggleBreakpoint [text]
```

## <a name="arguments"></a>Arguments

`text`\
İsteğe bağlı. Metin belirtilirse, satır adlandırılmış bir kesme noktası olarak işaretlenir. Aksi takdirde, çizgi adlandırılmamış bir kesme noktası olarak işaretlenir ve bu, F9 tuşuna bastığınızda ne olacağı ile benzerdir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, geçerli kesme noktasına geçiş yapar.

```
>Debug.ToggleBreakpoint
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)