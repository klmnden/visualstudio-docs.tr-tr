---
title: -ProjectConfig (devenv.exe)
ms.date: 12/10/2018
ms.topic: reference
helpviewer_keywords:
- /ProjectConfig Devenv switch
- configurations, rebuilding
- deployment projects, creating
- configurations, cleaning
- deployment projects, specifying
- deployment projects, adding
- build configurations, specifying
- Devenv, /ProjectConfig switch
- ProjectConfig Devenv switch (/ProjectConfig)
- projects [Visual Studio], build configuration
- projects [Visual Studio], cleaning
ms.assetid: 6b54ef59-ffed-4f62-a645-1279ede97ebf
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e6127be41e4b791fa03182b65ab78c9814e16d30
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62968909"
---
# <a name="projectconfig-devenvexe"></a>/ProjectConfig (devenv.exe)

Derleme, temizleme, yeniden oluşturun veya adlı projeyi dağıtmak uygulanacak bir proje yapı yapılandırmasını belirtir `/Project` bağımsız değişken.

## <a name="syntax"></a>Sözdizimi

```shell
devenv SolutionName {/Build|/Clean|/Deploy|/Rebuild} [SolnConfigName [/Project ProjName [/ProjectConfig ProjConfigName]] [/Out OutputFilename]]
```

## <a name="arguments"></a>Arguments

- *SolutionName*

  Gerekli. Çözüm dosyasının adını ve tam yolu.

- {`/Build`|`/Clean`|`/Deploy`|`/Rebuild`}

  Gerekli. [Yapılar](build-devenv-exe.md), [temizler](clean-devenv-exe.md), [dağıtır](deploy-devenv-exe.md), veya [oluşturur](rebuild-devenv-exe.md) proje.

- *SolnConfigName*

  İsteğe bağlı. Çözüm Yapılandırması adı (gibi `Debug` veya `Release`) adlı çözüm için uygulanacak *SolutionName*. Çözüm birden fazla platformu varsa, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`). Bu bağımsız değişken belirtilmezse, ya da boş bir dize (`""`), çözümün etkin Yapılandırma Aracı'nı kullanır.

- `/Project` *ProjName*

  İsteğe bağlı. Çözüm içindeki bir proje dosyasının adı ve yolu. Projenin görünen adını veya göreli bir yol girebilirsiniz *SolutionName* proje dosyasını klasör. Ayrıca, proje dosyasının adını ve tam yolunu da girebilirsiniz.

- `/ProjectConfig` *ProjConfigName*

  İsteğe bağlı. Projenin yapı yapılandırması adı (gibi `Debug` veya `Release`) uygulanacak `/Project` adlı. Çözüm birden fazla platformu varsa, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`).

- `/Out` *OutputFilename*

  İsteğe bağlı. Aracı göndermek istediğiniz bir dosya adı için çıkış. Dosya zaten varsa, aracı çıkış dosyasının sonuna ekler.

## <a name="remarks"></a>Açıklamalar

`/ProjectConfig` Anahtar kullanılmalıdır `/Project` geçiş kapsamında bir `/Build`, /`Clean`, `/Deploy`, veya `/Rebuild` komutu.

Çift tırnak içine boşluk dizeleri alın.

Komut penceresinde veya belirtilen herhangi bir günlük dosyasını hataları dahil olmak üzere, derlemeler için Özet bilgiler görüntülenebilir `/Out` geçin.

## <a name="example"></a>Örnek

Aşağıdaki komut, projeyi derler `CSharpWinApp`kullanarak `Debug` içinde proje yapı yapılandırmasını `MySolution`:

```shell
devenv "%USERPROFILE%\source\repos\MySolution\MySolution.sln" /build Debug /project "CSharpWinApp\CSharpWinApp.csproj" /projectconfig Debug
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [/ Project (devenv.exe)](../../ide/reference/project-devenv-exe.md)
- [/ Derleme (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/ Clean (devenv.exe)](../../ide/reference/clean-devenv-exe.md)
- [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/ (Devenv.exe) dağıtma](../../ide/reference/deploy-devenv-exe.md)
- [/ (Devenv.exe out)](../../ide/reference/out-devenv-exe.md)