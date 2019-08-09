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
ms.openlocfilehash: 75afe1cdd0d1755d2953e6b9e6e3e85a089b3303
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926133"
---
# <a name="quick-watch-command"></a>Hızlı Bakış Komutu
[QuickWatch](../../debugger/watch-and-quickwatch-windows.md) penceresinin Expression alanında seçili veya belirtilen metni görüntüler. Bu iletişim kutusunu, hata ayıklayıcı tarafından tanınan bir değişkenin veya ifadenin geçerli değerini ya da bir kaydın içeriğini hesaplamak için kullanabilirsiniz. Ayrıca, herhangi bir const olmayan değişkenin veya herhangi bir kaydın içeriğinin değerini değiştirebilirsiniz.

## <a name="syntax"></a>Sözdizimi

```cmd
Debug.QuickWatchq [text]
```

## <a name="arguments"></a>Arguments

`text`\
İsteğe bağlı. **QuickWatch** iletişim kutusuna eklenecek metin.

## <a name="remarks"></a>Açıklamalar

`text` Atlanırsa, imlecin üzerinde şu anda seçili olan metin veya sözcük izleme penceresi eklenir.

## <a name="example"></a>Örnek

```cmd
>Debug.QuickWatch
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio 'da gözcü ve hızlı gözcü pencerelerini kullanarak değişkenlerde bir Izleme ayarlayın](../../debugger/watch-and-quickwatch-windows.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)