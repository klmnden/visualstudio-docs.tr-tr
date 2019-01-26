---
title: Kaynağı Listele Komutu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- Debug.ListSource
helpviewer_keywords:
- Debug.ListSource command
- list source command
- ListSource command
ms.assetid: e45f08d2-f4a3-49c3-9452-aa60508e2f74
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b5348bd2533a10d98732911a6b7af5410e8ffe42
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55031636"
---
# <a name="list-source-command"></a>Kaynağı Listele Komutu
Belirtilen kaynak kodu satırlarını görüntüler.

## <a name="syntax"></a>Sözdizimi

```
Debug.ListSource [/Count:number] [/Current] [/File:filename]
[/Line:number] [/ShowLineNumbers:yes|no]
```

## <a name="switches"></a>Anahtarlar
 / Sayısı:`number`

 İsteğe bağlı. Görüntülenecek satır sayısını belirtir.

 / Geçerli

 İsteğe bağlı. Geçerli satırı gösterir.

 / Dosya:`filename`

 İsteğe bağlı. Gösterilecek dosyasının yolu. Dosya adı belirtilmezse, komut satırı geçerli deyimin için kaynak kodunu gösterir.

 / Çizgi:`number`

 İsteğe bağlı. Belirli bir satır numarasına gösterir.

 / ShowLineNumbers:`yes|no`

 İsteğe bağlı. Satır numaraları görüntülenip görüntülenmeyeceğini belirtir.

## <a name="example"></a>Örnek
 Bu örnekte, kaynak kodu satır numaralarını görünür olan Form1.vb, dosyanın 4 satırından listeler.

```
Debug.ListSource /File:"C:\Visual Studio Projects\Form1.vb" /Line:4 /ShowLineNumbers:yes
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)