---
title: -UseEnv (devenv.exe)
ms.date: 01/10/2019
ms.topic: reference
f1_keywords:
- VC.Project.UseEnvVars.ExcludePath
- VC.Project.UseEnvVars.LibraryPath
- VC.Project.UseEnvVars.SourcePath
- VC.Project.UseEnvVars.Include
- VC.Project.UseEnvVars.Path
- VC.Project.UseEnvVars.ReferencePath
helpviewer_keywords:
- UseEnv switch
- /UseEnv Devenv switch
- Devenv, /UseEnv
ms.assetid: 2dd14603-a61b-42d2-ba31-427a0ee8a799
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 16443b30ccf6ba03a01df0234695d27e4cd909af
ms.sourcegitcommit: 88f576ac32af31613c1a10c1548275e1ce029f4f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "71186491"
---
# <a name="useenv-devenvexe"></a>/UseEnv (devenv.exe)

Visual Studio 'Yu başlatır ve derleme için belirli ortam değişkenlerini yükler.

> [!NOTE]
> Bu anahtar ile birlikte yüklenir **C++ ile masaüstü geliştirme** iş yükü.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /UseEnv {SolutionName|ProjectName}
```

## <a name="arguments"></a>Arguments

- *SolutionName*

  Bir çözüm dosyasının tam yolu ve adı.

- *ProjectName*

  Bir proje dosyasının tam yolu ve adı.

## <a name="remarks"></a>Açıklamalar

Bu anahtar, **VC + + dizinleri**için proje özellikleri Içindeki VISUAL Studio IDE 'yi etkiler. `/UseEnv` Anahtarı belirtirseniz, **VC + + dizinleri** düğümü Path, INCLUDE, LIBPATH ve LIB ortam değişkenlerinin değerlerini gösterir. (Ayrıca, **kaynak dizinlerin** ve **Dışlanan dizinlerin**değerlerini gösterir.) Aksi halde düğüm, ortam değişkenlerini beş dizin değeriyle değiştirir: **Yürütülebilir dizinler**, **dizinler**, **başvuru dizinleri**, **kitaplık dizinleri**ve **kitaplık WinRT dizinleri**.

> [!TIP]
> Projeye sağ tıklayıp C++ **Özellikler**' i seçerek Proje özelliklerine erişirsiniz. **Özellik sayfaları** Iletişim kutusunda **yapılandırma özellikleri** ' ni ve ardından **VC + + dizinleri**' ni seçin.

Bu anahtarla bir proje adı belirtildiğinde araç, projenin üst çözümündeki tüm projeler için ortam değişkenlerini görüntüler.

## <a name="example"></a>Örnek

Aşağıdaki örnek Visual Studio 'yu başlatır ve ortam değişkenlerini `MySolution` çözümün özellik sayfalarına yükler.

```shell
devenv.exe /useenv "%USERPROFILE%\source\repos\MySolution\MySolution.sln"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [VC + + dizinleri Özellik sayfası (Windows)](/cpp/build/reference/vcpp-directories-property-page)
