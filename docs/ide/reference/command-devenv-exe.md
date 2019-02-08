---
title: -Command (devenv.exe)
ms.date: 12/10/2018
ms.topic: reference
helpviewer_keywords:
- Devenv, /Command switch
- /Command Devenv switch
- Command Devenv switch
ms.assetid: 13c20cd6-f09d-400a-8b7b-ecc266a32cef
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cf8f72f0d9b0c2d847ddb2c5e7e6c3c8d4ae4467
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55932501"
---
# <a name="command-devenvexe"></a>/Command (devenv.exe)

Visual Studio IDE başlatıldıktan sonra belirtilen komutu yürütür.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /Command CommandName
```

## <a name="arguments"></a>Arguments

- *commandName*

  Gerekli. Visual Studio komut ya da çift tırnak işareti içine alınmış diğer adının, tam adı. Komut ve diğer ad sözdizimi hakkında daha fazla bilgi için bkz: [Visual Studio komutları](../../ide/reference/visual-studio-commands.md).

## <a name="remarks"></a>Açıklamalar

Başlangıç tamamlandıktan sonra IDE adlandırılmış komutu yürütür. Bu anahtarı kullanırsanız, IDE başlangıçta Visual Studio Başlangıç sayfası görüntülemez.

Bir eklenti bir komut sunarsa, komut satırından eklentiyi başlatmak için bu anahtarı kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Eklentileri Eklenti Yöneticisi'ni kullanarak denetim](/previous-versions/xwdatdwh(v=vs.140)).

## <a name="example"></a>Örnek

İlk örnek, Visual Studio başlatır ve makro açık sık kullanılan dosyaları otomatik olarak çalıştırır.

İkinci örnek bir web tarama IDE içinde sekme açar ve Microsoft Docs siteye gider.

Üçüncü örnek adlı yeni bir dosya oluşturur `some_file.cs` ve Kod Düzenleyicisi'nde açılır.

```shell
devenv /command "Macros.MyMacros.Module1.OpenFavoriteFiles"

devenv /command "navigate https://docs.microsoft.com/"

devenv /command "nf some_file.cs"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
- [Komut penceresi](command-window.md)