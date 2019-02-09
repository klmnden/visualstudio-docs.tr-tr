---
title: Hızlı Bakış Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- debug.quickwatch
helpviewer_keywords:
- Quick Watch command
- Debug.Quickwatch command
ms.assetid: 9670ac3a-8f2f-4874-974d-cb87d3b0cde1
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5e45a6c63cb1f886c1440b93d58f944458f61290
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55969873"
---
# <a name="quick-watch-command"></a>Hızlı Bakış Komutu
İfade alanında seçilen veya belirtilen metni görüntüler [QuickWatch](../../debugger/watch-and-quickwatch-windows.md) penceresi. Bir değişkenin veya ifadenin hata ayıklayıcı veya bir kaydın içeriğini tarafından tanınan geçerli değerini hesaplamak için bu iletişim kutusunu kullanabilirsiniz. Ayrıca, herhangi bir sabit olmayan değişken değeri veya herhangi bir kayıt içeriğini değiştirebilirsiniz.

## <a name="syntax"></a>Sözdizimi

```cmd
Debug.QuickWatchq [text]
```

## <a name="arguments"></a>Arguments
 `text`

 İsteğe bağlı. Eklenecek metin **QuickWatch** iletişim kutusu.

## <a name="remarks"></a>Açıklamalar
 Varsa `text` olan atlanırsa, seçili durumdaki metni veya word imlecin İzle penceresine eklenir.

## <a name="example"></a>Örnek

```cmd
>Debug.QuickWatch
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Değişkenleri izleme ve QuickWatch Windows Visual Studio kullanarak bir izleme ayarlayın](../../debugger/watch-and-quickwatch-windows.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)