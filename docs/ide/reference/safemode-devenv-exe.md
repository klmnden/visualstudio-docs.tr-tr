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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 092cc1fc3267113e862646b7572e9091b8f6ddef
ms.sourcegitcommit: 01185dadd2fa1f9a040d2a366869f1a5e1d18e0f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54227206"
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