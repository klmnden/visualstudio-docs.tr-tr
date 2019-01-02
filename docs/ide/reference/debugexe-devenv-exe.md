---
title: -DebugExe (devenv.exe)
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- Devenv, /DebugExe switch
- DebugExe switch
- /DebugExe [devenv.exe]
ms.assetid: cd700006-1648-418f-924b-4b1e5c1412ab
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 99f256b47125f4e07ca5dc148c4351871389a94b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53889416"
---
# <a name="debugexe-devenvexe"></a>/DebugExe (devenv.exe)
Ayıklanacak belirtilen yürütülebilir dosyayı açar.

## <a name="syntax"></a>Sözdizimi

```cmd
Devenv /debugexe ExecutableFile
```

## <a name="arguments"></a>Arguments
 `ExecutableFile`

 Gerekli. Bir .exe dosyası yolu ve dosya adı.

 .Exe dosyası bulunamadı veya yok, hiçbir uyarı veya hata görüntülenir ve [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] normalde başlatır.

## <a name="remarks"></a>Açıklamalar
 Aşağıdaki dizeleri `ExecutableFile` parametresi, o dosya için bağımsız değişken olarak geçirilir.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte dosyayı açar `MyApplication.exe` hata ayıklama.

```cmd
Devenv.exe /debugexe MyApplication.exe
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)