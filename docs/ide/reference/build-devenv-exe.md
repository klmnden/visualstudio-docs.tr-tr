---
title: -Build (devenv.exe)
ms.date: 12/10/2018
ms.topic: reference
helpviewer_keywords:
- builds, command-line
- /build Devenv switch
- Devenv, /build switch
- build Devenv switch
- command-line builds
ms.assetid: ced21627-7653-455b-8821-3e31c6a448cf
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 67aba8d93514618fc09abe933cfd28023136a4d6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62790921"
---
# <a name="build-devenvexe"></a>/Build (devenv.exe)

Bir çözüm veya projeyi belirtilen çözüm yapılandırma dosyası kullanarak oluşturur.

## <a name="syntax"></a>Sözdizimi

```shell
devenv SolutionName /Build [SolnConfigName [/Project ProjName [/ProjectConfig ProjConfigName]] [/Out OutputFilename]]
```

## <a name="arguments"></a>Arguments

- *SolutionName*

  Gerekli. Çözüm dosyasının adını ve tam yolu.

- *SolnConfigName*

  İsteğe bağlı. Çözüm Yapılandırması adı (gibi `Debug` veya `Release`) adlı bir çözüm oluşturmak için kullanılacak *SolutionName*. Birden çok çözüm platformları kullanamıyorsanız, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`). Bu bağımsız değişken belirtilmezse, ya da boş bir dize (`""`), çözümün etkin Yapılandırma Aracı'nı kullanır.

- `/Project` *ProjName*

  İsteğe bağlı. Çözüm içindeki bir proje dosyasının adı ve yolu. Göreli bir yol girebilirsiniz *SolutionName* klasör proje dosyası veya projenin görünen adı veya tam yolu ve proje dosyasının adı.

- `/ProjectConfig` *ProjConfigName*

  İsteğe bağlı. Bir proje adını yapı yapılandırması (gibi `Debug` veya `Release`) adlı bir proje derlenirken kullanılacak. Çözüm birden fazla platformu varsa, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`). Bu anahtar belirtilirse, onu geçersiz kılar *SolnConfigName* bağımsız değişken.

- `/Out` *OutputFilename*

  İsteğe bağlı. Aracı göndermek istediğiniz bir dosya adı için çıkış. Dosya zaten varsa, aracı çıkış dosyasının sonuna ekler.

## <a name="remarks"></a>Açıklamalar

- `/Build` Anahtarı ile aynı işlevi gerçekleştirir **Çözümü Derle** tümleşik geliştirme ortamında (IDE) menü komutu.

- Çift tırnak içine boşluk dizeleri alın.

- Komut penceresinde veya belirtilen herhangi bir günlük dosyasını hataları dahil olmak üzere, derlemeler için Özet bilgiler görüntülenebilir `/Out` geçin.

- `/Build` Geçiş yalnızca son derlemeden sonra değiştirilen projeleri oluşturur. Bir çözümdeki tüm projeleri oluşturmak için kullanın [/rebuild](../../ide/reference/rebuild-devenv-exe.md) yerine.

- Bildiren bir hata iletisi alırsanız **geçersiz proje yapılandırması**, çözüm platformu veya proje platformu belirttiğiniz emin olun (örneğin, `Debug|Win32`).

## <a name="example"></a>Örnek

Aşağıdaki komut, projeyi derler `CSharpWinApp`kullanarak `Debug` içinde proje yapı yapılandırmasını `MySolution`.

```shell
devenv "%USERPROFILE%\source\repos\MySolution.sln" /build Debug /project "CSharpWinApp\CSharpWinApp.csproj" /projectconfig Debug
```

## <a name="see-also"></a>Ayrıca bkz.

- [Projeleri ve çözümleri oluşturma ve temizleme](../../ide/building-and-cleaning-projects-and-solutions-in-visual-studio.md)
- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/ Clean (devenv.exe)](../../ide/reference/clean-devenv-exe.md)
- [/ (Devenv.exe out)](../../ide/reference/out-devenv-exe.md)