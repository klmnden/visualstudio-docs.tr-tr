---
title: -Out (devenv.exe)
ms.date: 12/10/2018
ms.topic: reference
helpviewer_keywords:
- errors [Visual Studio], builds
- Devenv, /Out switch
- builds [Visual Studio], logs
- error logs [Visual Studio], command-line build errors
- error logs [Visual Studio]
- /Out Devenv switch
- Out Devenv switch
- builds [Visual Studio], errors
- output files, build errors
ms.assetid: 9002d8c2-36d4-451c-b489-8f01932f31f7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 039456c10993199ec2265042aabc0ed5c475ccd9
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55954744"
---
# <a name="out-devenvexe"></a>/Out (devenv.exe)

Depolamak ve hataları görüntülemek için bir dosya belirtir olduğunda, [çalıştırma](run-devenv-exe.md), [çalıştırın ve çıkış](runexit-devenv-exe.md), [yükseltme](upgrade-devenv-exe.md), [derleme](build-devenv-exe.md), [yenidenoluşturun](rebuild-devenv-exe.md), [temiz](clean-devenv-exe.md), veya [dağıtma](deploy-devenv-exe.md) bir çözüm.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /Out FileName
```

## <a name="arguments"></a>Arguments

- *Dosya adı*

  Gerekli. Almak için dosyanın adı ve yolu yürütülebilir oluşturduğunuzda çıktı.

## <a name="remarks"></a>Açıklamalar

Dosya, varolmayan dosya adı belirtilirse, otomatik olarak oluşturulur. Aksi takdirde dosya zaten var ve sonuçları için dosyanın mevcut içeriğini eklenir.

Komut satırı derleme hataları görüntülenir **komut** penceresi ve çözüm Oluşturucusu'nu görüntülemek **çıkış** penceresi. Bu anahtar, katılımsız yapılar sonuçlarını görüntülemek için yararlıdır.

## <a name="example"></a>Örnek

Bu örnek çalıştırılır `MySolution` ve hataları Yazar `MyErrorLog.txt`.

```shell
devenv /run "%USERPROFILE%\source\repos\MySolution\MySolution.sln" /out "C:\MyErrorLog.txt"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [/ Çalıştırma (devenv.exe)](../../ide/reference/run-devenv-exe.md)
- [/ RunExit (devenv.exe)](runexit-devenv-exe.md)
- [/ Yükseltme (devenv.exe)](upgrade-devenv-exe.md)
- [/ Clean (devenv.exe)](clean-devenv-exe.md)
- [/ Derleme (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/ (Devenv.exe) dağıtma](../../ide/reference/deploy-devenv-exe.md)