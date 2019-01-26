---
title: -Run (devenv.exe)
ms.date: 12/10/2018
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- /Run Devenv
- Run Devenv switch
- applications [Visual Studio], running
- /R Devenv switch
- Devenv, /Run switch
- R Devenv switch (/R)
ms.assetid: b1f22f9d-39a5-4918-8a2a-4b5c1e872665
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0d8e89a223ef43d7d2235772940a05b7fb42c0f8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54996343"
---
# <a name="run-devenvexe"></a>/Run (devenv.exe)

Derler ve belirtilen proje veya çözüm çalıştırır.

## <a name="syntax"></a>Sözdizimi

```shell
devenv {/Run|/R} {SolutionName|ProjectName} [/Out OutputFilename]
```

## <a name="arguments"></a>Arguments

- *SolutionName*

  Bir çözüm dosyası adını ve tam yolu.

- *projectName*

  Bir proje dosyasının adını ve tam yolu.

- `/Out` *OutputFilename*

  İsteğe bağlı. Aracı göndermek istediğiniz bir dosya adı için çıkış. Dosya zaten varsa, aracı çıkış dosyasının sonuna ekler.

## <a name="remarks"></a>Açıklamalar

Derler ve belirtilen proje veya çözümü etkin çözüm yapılandırması için belirtilen ayarlara göre çalıştırır. Bu anahtar IDE'yi başlatır ve sonra proje etkin bırakan veya çözüm çalıştırma tamamlandı.

- Çift tırnak içine boşluk dizeleri alın.

- Hataları dahil olmak üzere Özet bilgileri görüntülenebilir **komut** penceresinde veya belirtilen herhangi bir günlük dosyasını `/Out` geçin.

## <a name="example"></a>Örnek

Bu örnek çözüm çalıştırılır `MySolution` kullanarak etkin dağıtım yapılandırması.

```shell
devenv /run "%USERPROFILE%\source\repos\MySolution\MySolution.sln"
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [/ Runexit (devenv.exe)](../../ide/reference/runexit-devenv-exe.md)
- [/ Derleme (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/ (Devenv.exe out)](../../ide/reference/out-devenv-exe.md)