---
title: -RunExit (devenv.exe)
ms.date: 12/10/2018
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- RunExit Devenv switch
- Devenv, /RunExit switch
- /RunExit Devenv switch
ms.assetid: bfc94875-5fc0-4110-b961-d59c0b403790
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7ebeba5afc1eb50703f62e386f7453d7c0c3c1f6
ms.sourcegitcommit: 01185dadd2fa1f9a040d2a366869f1a5e1d18e0f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54227193"
---
# <a name="runexit-devenvexe"></a>/ RunExit (devenv.exe)

Derler ve belirtilen proje veya çözüm çalıştırır ve ardından tümleşik geliştirme ortamı (IDE) kapatır.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /RunExit {SolutionName|ProjectName} [/Out OutputFilename]
```

## <a name="arguments"></a>Arguments

- *SolutionName*

  Bir çözüm dosyası adını ve tam yolu.

- *projectName*

  Bir proje dosyasının adını ve tam yolu.

- `/Out` *OutputFilename*

  İsteğe bağlı. Aracı göndermek istediğiniz bir dosya adı için çıkış. Dosya zaten varsa, aracı çıkış dosyasının sonuna ekler.

## <a name="remarks"></a>Açıklamalar

Derler ve belirtilen proje veya çözümü etkin çözüm yapılandırması için belirtilen ayarlara göre çalıştırır. IDE projeyi sırasında bu anahtar en aza indirir veya çözümü çalıştırın. Proje sonra IDE'yi kapatır veya çözüm çalıştırma tamamlandı.

- Çift tırnak içine boşluk dizeleri alın.

- Hataları dahil olmak üzere Özet bilgileri görüntülenebilir **komut** penceresinde veya belirtilen herhangi bir günlük dosyasını `/Out` geçin.

## <a name="example"></a>Örnek

Bu örnek çözüm çalıştırılır `MySolution` simge durumuna küçültülmüş IDE'de etkin dağıtım yapılandırması kullanan ve daha sonra IDE'yi kapatır.

```
devenv /runexit "%USERPROFILE%\source\repos\MySolution\MySolution.sln"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [/ Çalıştırma (devenv.exe)](../../ide/reference/run-devenv-exe.md)
- [/ Derleme (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/ (Devenv.exe out)](../../ide/reference/out-devenv-exe.md)