---
title: Command penceresi çıktısı günlüğü tut komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- tools.logcommandwindowoutput
helpviewer_keywords:
- log Command window output command
- View.LogCommandWindowOutput command
ms.assetid: d4ecec35-5af4-4954-8d60-2cd24583fbb4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6ab2dfea4c51ee33407088c208aea351732b8a4a
ms.sourcegitcommit: 9753c7544cec852ca5efd0834e0956d9e53a5734
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67043526"
---
# <a name="log-command-window-output-command"></a>Komut penceresi çıktısı günlüğü tut komutu

Tüm giriş ve çıkış kopyaları **komut** penceresine bir dosya.

## <a name="syntax"></a>Sözdizimi

```cmd
Tools.LogCommandWindowOutput [filename] [/on|/off] [/overwrite]
```

## <a name="arguments"></a>Arguments

`filename`\
İsteğe bağlı. Günlük dosyasının adı. Varsayılan olarak, kullanıcı profili klasöründe bir dosya oluşturulur. Dosya adı zaten varsa, günlük varolan dosyanın sonuna eklenir. Dosya yok belirtilirse, belirtilen son dosya kullanılır. Önceki dosya varsa, cmdline.log adlı varsayılan günlük dosyası oluşturulur.

> [!TIP]
> Günlük dosyasına kaydedildiği konumu değiştirmek için yol boşluk içeriyorsa tırnak işareti içine alınmış dosyanın tam yolunu girin.

## <a name="switches"></a>Anahtarlar

/on\
İsteğe bağlı. Günlüğü başlar **komut** belirtilen dosya penceresinde ve yeni bilgiler ile dosya ekler.

/off\
İsteğe bağlı. Günlüğü durdurur **komut** penceresi.

/overwrite\
İsteğe bağlı. Dosyanın içinde belirtilen `filename` bağımsız değişken var olan bir dosya ile eşleşen, dosyanın üzerine yazılır.

## <a name="remarks"></a>Açıklamalar

Dosya yok belirtilirse, dosya cmdline.log varsayılan olarak oluşturulur. Varsayılan olarak, bu komut için diğer ad günlüktür.

## <a name="examples"></a>Örnekler

Bu örnek, yeni bir günlük dosyası cmdlog, oluşturur ve komut günlük başlatır.

```cmd
>Tools.LogCommandWindowOutput cmdlog
```

Bu örnek, oturum açma komutları durdurur.

```cmd
>Tools.LogCommandWindowOutput /off
```

Bu örnek komut daha önce kullanılan günlük dosyasında günlük sürdürür.

```cmd
>Tools.LogCommandWindowOutput /on
```

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)
- [Komut penceresi](../../ide/reference/command-window.md)
- [Bul/komut kutusu](../../ide/find-command-box.md)
- [Visual Studio komut diğer adları](../../ide/reference/visual-studio-command-aliases.md)