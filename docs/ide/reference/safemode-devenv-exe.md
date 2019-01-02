---
title: -SafeMode (devenv.exe)
ms.date: 11/04/2016
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
ms.openlocfilehash: ed14c3ec0da75df37c5a006f4e25240ac6630d20
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53949660"
---
# <a name="safemode-devenvexe"></a>/SafeMode (devenv.exe)
Başlar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] güvenli modda, yalnızca varsayılan ortama ve Hizmetleri Yükleniyor.

## <a name="syntax"></a>Sözdizimi

```cmd
devenv /SafeMode
```

## <a name="remarks"></a>Açıklamalar
 Bu anahtar, ne zaman yüklenmesini tüm üçüncü taraf VSPackages engeller [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] böylece kararlı yürütme sağlamaya başlar.

## <a name="description"></a>Açıklama
 Aşağıdaki örnek başlatır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] güvenli modda.

## <a name="code"></a>Kod

```cmd
Devenv.exe /SafeMode
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)