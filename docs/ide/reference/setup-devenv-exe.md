---
title: Devenv.exe kurulum anahtarı
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- setup Devenv switch
- /setup Devenv switch
- Devenv, /setup switch
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 3f1f801d4da451d9357082359a1cf001915e1041
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53829280"
---
# <a name="setup-devenvexe"></a>/Setup (devenv.exe)

/ Setup geçiş menüleri, araç çubukları ve komut gruplarından tüm kullanılabilir VSPackages tanımlayan kaynak meta verileri birleştirmek için Visual Studio neden olur.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /setup
```

## <a name="remarks"></a>Açıklamalar

Bu anahtar hiçbir bağımsız değişkeni alır. `devenv /setup` Komut genellikle yükleme işleminin son adımı verilir. Kullanım `/setup` anahtar Visual Studio ile başlamıyor.

> [!NOTE]
> Çalıştırmalısınız `devenv` kullanabilmek için yönetici olarak `/setup` geçin.

## <a name="example"></a>Örnek

Bu örnekte, bir VSPackage içeren Visual Studio sürümünü yüklemeyi son adım gösterilmektedir.

```shell
devenv /setup
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)