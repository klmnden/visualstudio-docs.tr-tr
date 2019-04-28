---
title: -DebugExe (devenv.exe)
ms.date: 12/10/2018
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
ms.openlocfilehash: 05266a6f1b5ee0be22e2edc8df1c03b720844f4f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62968086"
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