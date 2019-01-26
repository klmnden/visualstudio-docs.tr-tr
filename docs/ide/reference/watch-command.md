---
title: İzle Komutu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- debug.watch
helpviewer_keywords:
- Watch command
- Debug.Watch command
ms.assetid: aa02e647-d9f5-4905-a651-52a8df595795
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f979162dbbef7c04372d42d9ab693b013f33b8ad
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54923341"
---
# <a name="watch-command"></a>İzle Komutu
Oluşturur ve belirtilen bir örneğini açar bir **Watch** penceresi. Kullanabileceğiniz bir **Watch** penceresi değişkenleri ve ifadeleri kayıtları, bu değerleri düzenleme ve sonuçları kaydetmek için değerleri hesaplamak için.

## <a name="syntax"></a>Sözdizimi

```cmd
Debug.Watch[index]
```

## <a name="arguments"></a>Arguments
 `index`

 Gerekli. İzleme penceresi örneği sayısı.

## <a name="remarks"></a>Açıklamalar
 `index` Bir tamsayı olmalıdır. Geçerli değerler 1, 2, 3 veya 4 arasındadır.

## <a name="example"></a>Örnek

```cmd
>Debug.Watch1
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Otomatikler ve Yereller Pencereleri](../../debugger/autos-and-locals-windows.md)
- [Değişkenleri izleme ve QuickWatch Windows Visual Studio kullanarak bir izleme ayarlayın](../../debugger/watch-and-quickwatch-windows.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)