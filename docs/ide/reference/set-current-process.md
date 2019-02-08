---
title: Geçerli Süreci Ayarla
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- Debug.SetCurrentProcess command
- Set Current Process command
ms.assetid: 1e016ebd-aadd-411f-a606-03bf69d3f8aa
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 24f4c08147f72168f5207418a51d7a9cfa8a2b51
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55938442"
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