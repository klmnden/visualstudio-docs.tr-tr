---
title: İş Parçacıklarını Listele Komutu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- debug.listthreads
helpviewer_keywords:
- ListThreads command
- list threads command
- Debug.ListThreads command
ms.assetid: 34b665c0-d46f-4c1a-a066-b678eba5ac54
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f1a914ffcd242626b0f519ab541c4c381a4597da
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53846145"
---
# <a name="list-threads-command"></a>İş Parçacıklarını Listele Komutu
Geçerli programdaki iş parçacıklarının listesini görüntüler.

## <a name="syntax"></a>Sözdizimi

```
Debug.ListThreads [index]
```

## <a name="arguments"></a>Arguments
 `index`

 İsteğe bağlı. Bir iş parçacığı geçerli iş parçacığı olarak dizine göre seçer.

## <a name="remarks"></a>Açıklamalar
 Bu seçenek belirtildiğinde, `index` bağımsız değişkeni, belirtilen iş parçacığı geçerli iş parçacığı olarak işaretler. Bir yıldız işareti (*), geçerli iş parçacığı yanındaki listede görüntülenir.

## <a name="example"></a>Örnek

```
>Debug.ListThreads
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Çağrı Yığınını Listele Komutu](../../ide/reference/list-call-stack-command.md)
- [Ayrıştırılmış Kodu Listele Komutu](../../ide/reference/list-disassembly-command.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)