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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 0633c3e94a870117e1ae171903581da448b09ace
ms.sourcegitcommit: 01185dadd2fa1f9a040d2a366869f1a5e1d18e0f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54227219"
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