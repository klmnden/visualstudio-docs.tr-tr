---
title: Başlat Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- debug.start
helpviewer_keywords:
- Start command
- Debug.Start command
ms.assetid: dc4e4aa2-b0ab-4e00-92db-6dc3058ddc21
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8f455306a87c82c5cd4fe55ccacdbba070b4467c
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926023"
---
# <a name="start-command"></a>Başlat Komutu
Başlangıç projesinde hata ayıklamaya başlar.

## <a name="syntax"></a>Sözdizimi

```cmd
Debug.Start [address]
```

## <a name="arguments"></a>Arguments
`address`

İsteğe bağlı. Kaynak kodundaki bir kesme noktasına benzer şekilde programın yürütmeyi askıya aldığı adres. Bu bağımsız değişken yalnızca hata ayıklama modunda geçerlidir.

## <a name="remarks"></a>Açıklamalar
Çalıştırıldığında **Başlat** komutu, belirtilen adrese bir RunToCursor işlemi gerçekleştirir.

## <a name="example"></a>Örnek
Bu örnek, hata ayıklayıcıyı başlatır ve oluşan tüm özel durumları yoksayar.

```cmd
>Debug.Start
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)