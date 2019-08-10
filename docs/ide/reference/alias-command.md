---
title: Diğer Ad Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- tools.alias
helpviewer_keywords:
- aliases, Visual Studio commands
- commands, aliases
- Tools.Alias command
- command aliases
- alias command
ms.assetid: bdf857df-b5d5-450f-8c10-a6fd4dccc130
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 396db6e08da211a801361328416d97622ee3eac8
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926334"
---
# <a name="alias-command"></a>Diğer Ad Komutu
Tüm komut, komut ve bağımsız değişkenler ya da başka bir diğer ad için yeni bir diğer ad oluşturur.

> [!TIP]
> Bağımsız `>alias` değişken olmadan yazmak, diğer adların ve tanımlarının geçerli listesini görüntüler.

## <a name="syntax"></a>Sözdizimi

```cmd
Tools.Alias [/delete] [/reset] [aliasname] [aliasstring]
```

## <a name="arguments"></a>Arguments
`aliasname`\
İsteğe bağlı. Yeni diğer ad için ad. İçin `aliasname`hiçbir değer sağlanmazsa, geçerli diğer adların ve tanımlarının bir listesi görüntülenir.

`aliasstring`\
İsteğe bağlı. Tüm komut adı veya var olan diğer ad ve diğer ad olarak oluşturmak istediğiniz parametreler. İçin `aliasstring`değer sağlanmazsa, belirtilen diğer ad için diğer ad ve diğer ad dizesi görüntülenir.

## <a name="switches"></a>Anahtarlar
/DELETE veya/del&lt ya da/d\
İsteğe bağlı. Belirtilen diğer adı siler ve otomatik tamamlamayı kaldırır.

/Reset süpürmeden
İsteğe bağlı. Önceden tanımlanmış diğer adların listesini orijinal ayarlarına sıfırlar. Diğer bir deyişle, önceden tanımlanmış tüm diğer adları geri yükler ve Kullanıcı tanımlı tüm diğer adları kaldırır.

## <a name="remarks"></a>Açıklamalar
Diğer adlar komutları temsil ettiğinden, bunlar komut satırının başlangıcında bulunmalıdır.

Bu komutu verirken, diğer adlarla değil, anahtardan hemen sonra gelen anahtarları eklemeniz gerekir, aksi takdirde anahtar, diğer ad dizesinin bir parçası olarak dahil edilir.

Bu `/reset` anahtar, diğer adlar geri yüklenmeden önce onay ister. İçin kısa bir `/reset`biçim yoktur.

## <a name="examples"></a>Örnekler
Bu örnek, tüm komut Edit. `upper`makebüyük komutu için yeni bir diğer ad oluşturur.

```cmd
>Tools.Alias upper Edit.MakeUpperCase
```

Bu örnek, diğer adı siler `upper`,.

```cmd
>Tools.alias /delete upper
```

Bu örnek, tüm geçerli diğer adlar ve tanımlar listesini görüntüler.

```cmd
>Tools.Alias
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)