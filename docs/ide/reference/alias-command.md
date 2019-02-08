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
ms.openlocfilehash: e55b27ebc3a0a9690e04e19e53b65a7aa44834de
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55919423"
---
# <a name="alias-command"></a>Diğer Ad Komutu
Tam komut, tam komut ve bağımsız değişkenler için yeni bir diğer ad veya başka bir diğer ad oluşturur.

> [!TIP]
> Yazarak `>alias` herhangi bir bağımsız değişken görüntüler olmadan geçerli diğer adlar ve tanımlarının listesi.


## <a name="syntax"></a>Sözdizimi

```cmd
Tools.Alias [/delete] [/reset] [aliasname] [aliasstring]
```

## <a name="arguments"></a>Arguments
 `aliasname` İsteğe bağlı. Yeni diğer adı. İçin herhangi bir değer sağlanmazsa `aliasname`, geçerli diğer adlar ve tanımlarının bir listesi görüntülenir.

 `aliasstring` İsteğe bağlı. Tam komu adı veya mevcut bir diğer ad ve bir diğer ad olarak oluşturmak istediğiniz herhangi bir parametre. İçin herhangi bir değer sağlanmazsa `aliasstring`, belirtilen diğer ad görüntüler için diğer ad ve diğer ad dizesi.

## <a name="switches"></a>Anahtarlar
 / DELETE veya/DEL veya /d isteğe bağlı. Otomatik tamamlamadan kaldırarak belirtilen diğer adları siler.

 / İsteğe bağlı sıfırlayın. Önceden tanımlanmış diğer adlar listesini özgün ayarlarına sıfırlar. Diğer bir deyişle, önceden tanımlanmış tüm diğer adları geri yükler ve kullanıcı tarafından tanımlanan tüm diğer adları kaldırır.

## <a name="remarks"></a>Açıklamalar
 Diğer adlar komutları temsil ettiğinden, komut satırının başında bulunmaları gerekir.

 Bu komut yayınlanırken, diğer adlardan sonra değil komutun hemen sonrasına anahtarları içermelidir, aksi takdirde anahtar diğer ad dizesinin bir parçası olarak dahil edilir.

 `/reset` Anahtarı diğer adlar geri yüklenmeden önce bir onay ister. İn bir kısa biçimi yoktur `/reset`.

## <a name="examples"></a>Örnekler
 Bu örnek, yeni bir diğer ad oluşturur `upper`, tam komut Edit.MakeUpperCase için.

```cmd
>Tools.Alias upper Edit.MakeUpperCase
```

 Bu örnek, diğer adını siler `upper`.

```cmd
>Tools.alias /delete upper
```

 Bu örnek, tüm geçerli diğer adlar ve açıklamalarının bir listesini görüntüler.

```cmd
>Tools.Alias
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)