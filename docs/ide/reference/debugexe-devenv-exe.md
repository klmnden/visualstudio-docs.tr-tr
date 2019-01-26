---
title: -DebugExe (devenv.exe)
ms.date: 12/10/2018
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- Devenv, /DebugExe switch
- DebugExe switch
- /DebugExe [devenv.exe]
- debugging executables
ms.assetid: cd700006-1648-418f-924b-4b1e5c1412ab
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a93a582af62ed0eac8cdc0f5da55ac7bda555152
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55008978"
---
# <a name="debugexe-devenvexe"></a>/DebugExe (devenv.exe)

Ayıklanacak belirtilen yürütülebilir dosyayı açar.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /DebugExe ExecutableFile
```

## <a name="arguments"></a>Arguments

- *YürütülebilirDosya*

  Gerekli. Yol ve dosya adını bir `.exe` dosya. Varsa `.exe` dosya bulunamadığında veya mevcut değil, hiçbir uyarı veya hata görüntülenir ve Visual Studio normal olarak başlatır.

## <a name="remarks"></a>Açıklamalar

Aşağıdaki dizeleri *YürütülebilirDosya* parametresi, o dosya için bağımsız değişken olarak geçirilir.

## <a name="example"></a>Örnek

Aşağıdaki örnekte dosyayı açar `MyApplication.exe` hata ayıklama.

```shell
devenv /debugexe MyApplication.exe
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)