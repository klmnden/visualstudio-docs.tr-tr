---
title: Sembol Yolu Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- debug.symbolpath
helpviewer_keywords:
- symbol path command
- Debug.SymbolPath command
- SymbolPath command
ms.assetid: b697ef2d-3f5d-40df-b113-7068a5bec0d4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 23a7a59ca23dc444bcdc714ade2fce5bedb87e8c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62945134"
---
# <a name="symbol-path-command"></a>Sembol Yolu Komutu
Hata ayıklayıcının simge araması dizinler listesini ayarlar.

## <a name="syntax"></a>Sözdizimi

```
Debug.SymbolPath pathname1;pathname2;... pathnameN
```

## <a name="arguments"></a>Arguments
 `pathname`

 İsteğe bağlı. Noktalı virgül hata ayıklayıcının simge araması yolları bir listesidir.

## <a name="remarks"></a>Açıklamalar
 Hayır ise `pathname` belirtilirse, komut geçerli simge yollarını listeler.

## <a name="example"></a>Örnek
 Bu örnek simge dizinleri listesine iki yol ekler.

```
Debug.SymbolPath C:\Symbol Path 1;C:\Symbol Path 2
```

## <a name="example"></a>Örnek
 Bu örnek, geçerli simge yollarının noktalı virgülle ayrılmış bir liste görüntüler.

```
Debug.SymbolPath
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Komut Penceresi](../../ide/reference/command-window.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)