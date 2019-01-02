---
title: Geçerli Süreci Ayarla
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- Debug.SetCurrentProcess command
- Set Current Process command
ms.assetid: 1e016ebd-aadd-411f-a606-03bf69d3f8aa
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 0c01c399dc76d1b328443edef27edd9a921b1b9c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53855289"
---
# <a name="set-current-process"></a>Geçerli Süreci Ayarla
Belirtilen işlemi Hata ayıklayıcıdaki etkin işlem olarak ayarlar.

## <a name="syntax"></a>Sözdizimi

```cmd
Debug.SetCurrentProcess index
```

## <a name="arguments"></a>Arguments
 `index`

 Gerekli. İşlem dizini.

## <a name="remarks"></a>Açıklamalar
 Hata ayıklama, ancak yalnızca bir işlem dublajcı içerisinde belirli bir zamanda birden çok işleme iliştirebilirsiniz. Kullanabileceğiniz `SetCurrentProcess` etkin işlemi ayarlamak için komutu.

## <a name="example"></a>Örnek

```cmd
>Debug.SetCurrentProcess 1
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)