---
title: -SafeMode (devenv.exe)
ms.date: 12/10/2018
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
ms.openlocfilehash: 14b2ac3a80a9e17e0c554f56ae8e31ac32450c5e
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55938689"
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