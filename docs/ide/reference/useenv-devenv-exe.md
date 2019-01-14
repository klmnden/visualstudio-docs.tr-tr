---
title: -UseEnv (devenv.exe)
ms.date: 01/10/2019
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f238cb2c426bcb931783b68a1ba0b4f3337e18b2
ms.sourcegitcommit: 38db86369af19e174b0aba59ba1918a5c4fe4a61
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/14/2019
ms.locfileid: "54270412"
---
# <a name="useenv-devenvexe"></a>/UseEnv (devenv.exe)

Visual Studio başlatılır ve derleme için belirli ortam değişkenlerini yükler.

> [!NOTE]
> Bu anahtar ile birlikte yüklenir **C++ ile masaüstü geliştirme** iş yükü.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /UseEnv {SolutionName|ProjectName}
```

## <a name="arguments"></a>Arguments

- *SolutionName*

  Bir çözüm dosyası adını ve tam yolu.

- *projectName*

  Bir proje dosyasının adını ve tam yolu.

## <a name="remarks"></a>Açıklamalar

Bu anahtar için Proje Özellikleri Visual Studio IDE'de etkiler **VC ++ dizinleri**. Belirtirseniz `/UseEnv` geçiş, **VC ++ dizinleri** düğüm yolu, INCLUDE, LIBPATH ve LIB ortam değişkenleri için değerleri gösterir. (Ayrıca değerleri gösterir **kaynak dizinleri** ve **dizinleri hariç tutmak**.) Aksi takdirde, düğümün ortam değişkenlerini beş directory değerlerle değiştirir: **Yürütülebilir dizinler**, **ekleme kodu dizinleri**, **başvuru dizinleri**, **kitaplık dizinleri**, ve **WinRT kitaplığı Dizinleri**.

> [!TIP]
> Bir C++ projesini sağ tıklatıp seçerek proje özelliklerine erişmek **özellikleri**. İçinde **özellik sayfaları** iletişim kutusunda **yapılandırma özellikleri** ardından **VC ++ dizinleri**.

Bu anahtarı kullanarak bir proje adı belirtildiğinde, araç projenin üst çözüm içindeki tüm projeler için ortam değişkenlerini görüntüler.

## <a name="example"></a>Örnek

Aşağıdaki örnek, Visual Studio başlatılır ve özellik sayfaları'nın ortam değişkenlerini yükler `MySolution` çözüm.

```shell
devenv.exe /useenv "%USERPROFILE%\source\repos\MySolution\MySolution.sln"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [VC ++ dizinleri özellik sayfası (Windows)](/cpp/ide/vcpp-directories-property-page)
