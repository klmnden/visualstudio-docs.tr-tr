---
title: -SafeMode (devenv.exe)
ms.date: 12/10/2018
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- /SafeMode Devenv switch
- Devenv, /SafeMode switch
- SafeMode switch
ms.assetid: b191f6a5-8f12-47ec-bcc7-b68149a22aa8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b794c80768990a3abac85d3ea3b93699f3b220dd
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54970441"
---
# <a name="safemode-devenvexe"></a>/SafeMode (devenv.exe)

Visual Studio, yalnızca varsayılan ortama ve servisler yüklenirken güvenli modda başlatır.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /SafeMode
```

## <a name="remarks"></a>Açıklamalar

Bu anahtar, tüm üçüncü taraf VSPackages kararlı yürütülmesine izin Visual Studio başladığında yüklenmesini engeller.

## <a name="example"></a>Örnek

Aşağıdaki örnek, Visual Studio güvenli modda başlatır.

```shell
devenv /safemode
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)