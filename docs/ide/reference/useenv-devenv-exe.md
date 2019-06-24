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
ms.openlocfilehash: 37326bbe44eed15a562f0d28c01eac02973a2487
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62789264"
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
