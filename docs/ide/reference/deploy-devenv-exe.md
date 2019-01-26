---
title: -Deploy (devenv.exe)
ms.date: 12/10/2018
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- Devenv, /Deploy switch
- Deploy Devenv switch
- deploying applications [Visual Studio], after build
- /Deploy Devenv switch
ms.assetid: e47c8723-df08-4645-aa2d-0c956e7ccca2
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0eef6420f09157a349658ca232a9e2551476b9d1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55008484"
---
# <a name="deploy-devenvexe"></a>/Deploy (devenv.exe)

Bir çözüm oluşturma veya yeniden oluşturma sonra dağıtır. Yalnızca yönetilen kod projeleri için geçerlidir.

## <a name="syntax"></a>Sözdizimi

```shell
devenv SolutionName /Deploy [SolnConfigName [/Project ProjName [/ProjectConfig ProjConfigName]] [/Out OutputFilename]]
```

## <a name="arguments"></a>Arguments

- *SolutionName*

  Gerekli. Çözüm dosyasının adını ve tam yolu.

- *SolnConfigName*

  İsteğe bağlı. Çözüm Yapılandırması adı (gibi `Debug` veya `Release`) adlı bir çözüm oluşturmak için kullanılacak *SolutionName*. Çözüm birden fazla platformu varsa, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`). Bu bağımsız değişken belirtilmezse, ya da boş bir dize (`""`), çözümün etkin Yapılandırma Aracı'nı kullanır.

- `/Project` *ProjName*

  İsteğe bağlı. Çözüm içindeki bir proje dosyasının adı ve yolu. Projenin görünen adını veya göreli bir yol girebilirsiniz *SolutionName* proje dosyasını klasör. Ayrıca, proje dosyasının adını ve tam yolunu da girebilirsiniz.

- `/ProjectConfig` *ProjConfigName*

  İsteğe bağlı. Bir proje adını derleme yapılandırması (gibi `Debug` veya `Release`) oluştururken kullanılacak `/Project` adlı. Çözüm birden fazla platformu varsa, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`). Bu anahtar belirtilirse, onu geçersiz kılar *SolnConfigName* bağımsız değişken.

- `/Out` *OutputFilename*

  İsteğe bağlı. Aracı göndermek istediğiniz bir dosya adı için çıkış. Dosya zaten varsa, aracı çıkış dosyasının sonuna ekler.

## <a name="remarks"></a>Açıklamalar

Belirtilen projeyi bir dağıtım projesi olmalıdır. Dağıtım için derlenen proje geçirildiğinde belirtilen projeyi bir dağıtım projesi yoksa, bir hata ile başarısız olur.

Çift tırnak içine boşluk dizeleri alın.

Hataları dahil olmak üzere, derlemeler için Özet bilgiler görüntülenebilir **komut** penceresinde veya belirtilen herhangi bir günlük dosyasını [/Out](out-devenv-exe.md) geçin.

## <a name="example"></a>Örnek

Bu örnek projesini dağıtır `CSharpWinApp`kullanarak `Release` içinde proje yapı yapılandırmasını `MySolution`.

```shell
devenv "%USERPROFILE%\source\repos\MySolution\MySolution.sln" /deploy Release /project "CSharpWinApp\CSharpWinApp.csproj" /projectconfig Release
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [/ Project (devenv.exe)](../../ide/reference/project-devenv-exe.md)
- [/ Derleme (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/ Clean (devenv.exe)](../../ide/reference/clean-devenv-exe.md)
- [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/ (Devenv.exe out)](../../ide/reference/out-devenv-exe.md)