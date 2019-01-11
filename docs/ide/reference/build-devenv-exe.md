---
title: -Build (devenv.exe)
ms.date: 12/10/2018
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c2b5c13665de3836844b16c405bf85c56f287e39
ms.sourcegitcommit: 01185dadd2fa1f9a040d2a366869f1a5e1d18e0f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54227401"
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

  İsteğe bağlı. Adlı çözümü derlemek için kullanılan çözüm yapılandırması adı *SolutionName*. Birden çok çözüm platformları kullanamıyorsanız, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`). Bu bağımsız değişken kalan, çözümün etkin Yapılandırma Aracı'nı kullanır.

- `/Project` *ProjName*

  İsteğe bağlı. Çözüm içindeki bir proje dosyasının adı ve yolu. Göreli bir yol girebilirsiniz *SolutionName* klasör proje dosyası veya projenin görünen adı veya tam yolu ve proje dosyasının adı.

- `/ProjectConfig` *ProjConfigName*

  İsteğe bağlı. Bir proje adı, adlandırılmış bir proje derlenirken kullanılacak yapılandırması oluşturun. Birden çok proje platformu varsa, aynı zamanda platforma, örneğin belirtmeniz gerekir `Debug|Win32`. Bu anahtar belirtilirse, onu geçersiz kılar *SolnConfigName* bağımsız değişken.

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