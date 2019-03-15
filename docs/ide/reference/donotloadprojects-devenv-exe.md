---
title: -DoNotLoadProjects (devenv.exe)
ms.date: 03/11/2019
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
ms.openlocfilehash: 91c4da26d202e1a23ff70a7c655f64fd6c05a340
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57875094"
---
# <a name="donotloadprojects-devenvexe"></a>/ DoNotLoadProjects (devenv.exe)

Tüm projeler yükleniyor olmadan belirtilen çözümü açar.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /DoNotLoadProjects SolutionName
```

## <a name="arguments"></a>Arguments

- *SolutionName*

  Gerekli. Açılacak bir çözüm adını ve tam yolu.

## <a name="example"></a>Örnek

Örnek, herhangi bir projeyi yüklemeden MySln.sln gündeki çözümü açar.

```shell
devenv /donotloadprojects MySln.sln

```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
