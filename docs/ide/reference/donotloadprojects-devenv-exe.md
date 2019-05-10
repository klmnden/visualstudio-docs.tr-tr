---
title: -DoNotLoadProjects (devenv.exe)
ms.date: 04/30/2019
ms.topic: reference
helpviewer_keywords:
- Devenv, /DoNotLoadProjects switch
- /DoNotLoadProjects Devenv switch
- DoNotLoadProjects Devenv switch
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a414fde4dee401016e997fa5d6890da2ae8d9d53
ms.sourcegitcommit: db30651dc0ce4d0b274479b23a6bd102a5559098
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65083927"
---
# <a name="donotloadprojects-devenvexe"></a>/ DoNotLoadProjects (devenv.exe)

**Yeni Visual Studio 2019 sürüm 16.1 için**

Tüm projeler yükleniyor olmadan belirtilen çözümü açar. Daha fazla bilgi için [filtrelenmiş çözümlerini Visual Studio'da](../filtered-solutions.md).

## <a name="syntax"></a>Sözdizimi

```shell
devenv /DoNotLoadProjects SolutionName
```

## <a name="arguments"></a>Arguments

*SolutionName*

Gerekli. Açılacak bir çözüm adını ve tam yolu.

## <a name="example"></a>Örnek

Örnek, herhangi bir projeyi yüklemeden MySln.sln çözümü açar.

```shell
devenv /donotloadprojects MySln.sln
```

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da filtrelenmiş çözümleri](../filtered-solutions.md)
- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
