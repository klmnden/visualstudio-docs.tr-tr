---
title: Kapsayıcılar için İleri düzey örnek
description: ''
ms.date: 04/18/2018
ms.topic: conceptual
ms.assetid: e03835db-a616-41e6-b339-92b41d0cfc70
author: heaths
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 1d14a02c70c0e4496c482940237054027e152a70
ms.sourcegitcommit: c7b9ab1bc19d74b635c19b1937e92c590dafd736
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2019
ms.locfileid: "67552855"
---
# <a name="advanced-example-for-containers"></a>Kapsayıcılar için İleri düzey örnek

::: moniker range="vs-2017"

Örnek Dockerfile içinde [derleme araçlarını bir kapsayıcıya alın yükleme](build-tools-container.md) her zaman kullanır [microsoft/dotnet-framework:4.7.2](https://hub.docker.com/r/microsoft/dotnet-framework) görüntünün en son microsoft/windowsservercore görüntü ve en son Visual temel Studio derleme araçları yükleyicisi. Bu uyarı görüntüye yayımlarsanız bir [Docker kayıt defteri](https://azure.microsoft.com/services/container-registry) başkalarının çekmek bu görüntü birçok senaryo için uygun olabilir. Ancak, uygulamada hangi temel görüntü hakkında belirli olmasını daha yaygındır, indirdiğiniz, hangi ikili dosyalarını kullanmak ve Aracı sürümleri yüklemeniz.

::: moniker-end

::: moniker range="vs-2019"

Örnek Dockerfile içinde [derleme araçlarını bir kapsayıcıya alın yükleme](build-tools-container.md) her zaman kullanır [microsoft/dotnet-framework: 4.8](https://hub.docker.com/r/microsoft/dotnet-framework) görüntünün en son microsoft/windowsservercore görüntü ve en son Visual temel Studio derleme araçları yükleyicisi. Bu uyarı görüntüye yayımlarsanız bir [Docker kayıt defteri](https://azure.microsoft.com/services/container-registry) başkalarının çekmek bu görüntü birçok senaryo için uygun olabilir. Ancak, uygulamada hangi temel görüntü hakkında belirli olmasını daha yaygındır, indirdiğiniz, hangi ikili dosyalarını kullanmak ve Aracı sürümleri yüklemeniz.

::: moniker-end

Aşağıdaki örnek Dockerfile dotnet/microsoft-framework görüntünün bir belirli sürüm etiketi kullanır. Belirli bir etiketi için temel bir görüntü kullanarak sıradan bir hale ve bu yapı unutmayın kolaylaştırır ya da aynı temel görüntüleri her zaman yeniden sahiptir.

> [!NOTE]
> Visual Studio microsoft/windowsservercore:10.0.14393.1593 ya da bunu temel alan herhangi bir kapsayıcıda yükleyicisi başlatılıyor sorunlara görüntüsüne yükleyemezsiniz. Daha fazla bilgi için [bilinen sorunlar kapsayıcılar için](build-tools-container-issues.md).

Aşağıdaki örnek, derleme Araçları'nın en son sürümünü yükler. Daha sonra bir kapsayıcıya yükleme derleme Araçları'nın önceki bir sürümünü kullanmak istiyorsanız, önce [oluşturma](create-an-offline-installation-of-visual-studio.md) ve [korumak](update-a-network-installation-of-visual-studio.md) düzeni.

## <a name="install-script"></a>Komut dosyası yükleme

Yükleme hata günlüklerini toplamak için gerçekleşir, "Install.cmd" adlı toplu betiği oluşturmak çalışma dizininde aşağıdaki içeriği içerir:

```shell
@if not defined _echo echo off
setlocal enabledelayedexpansion

call %*
if "%ERRORLEVEL%"=="3010" (
    exit /b 0
) else (
    if not "%ERRORLEVEL%"=="0" (
        set ERR=%ERRORLEVEL%
        call C:\TEMP\collect.exe -zip:C:\vslogs.zip

        exit /b !ERR!
    )
)
```

## <a name="dockerfile"></a>Dockerfile

Çalışma dizininde aşağıdaki içerikle "Dockerfile" oluşturun:

::: moniker range="vs-2017"

```dockerfile
# escape=`

# Use a specific tagged image. Tags can be changed, though that is unlikely for most images.
# You could also use the immutable tag @sha256:3eaa3ba18f45e6561f32d8dd927045413f1dd043d7d29fb581f5cb3c6f7d7481
ARG FROM_IMAGE=mcr.microsoft.com/dotnet/framework/sdk:4.7.2-windowsservercore-ltsc2019
FROM ${FROM_IMAGE}

# Copy our Install script.
COPY Install.cmd C:\TEMP\

# Download collect.exe in case of an install failure.
ADD https://aka.ms/vscollect.exe C:\TEMP\collect.exe

# Use the latest release channel. For more control, specify the location of an internal layout.
ARG CHANNEL_URL=https://aka.ms/vs/15/release/channel
ADD ${CHANNEL_URL} C:\TEMP\VisualStudio.chman

# Download and install Build Tools excluding workloads and components with known issues.
ADD https://aka.ms/vs/15/release/vs_buildtools.exe C:\TEMP\vs_buildtools.exe
RUN C:\TEMP\Install.cmd C:\TEMP\vs_buildtools.exe --quiet --wait --norestart --nocache `
    --installPath C:\BuildTools `
    --channelUri C:\TEMP\VisualStudio.chman `
    --installChannelUri C:\TEMP\VisualStudio.chman `
    --all `
    --remove Microsoft.VisualStudio.Component.Windows10SDK.10240 `
    --remove Microsoft.VisualStudio.Component.Windows10SDK.10586 `
    --remove Microsoft.VisualStudio.Component.Windows10SDK.14393 `
    --remove Microsoft.VisualStudio.Component.Windows81SDK

# Start developer command prompt with any other commands specified.
ENTRYPOINT C:\BuildTools\Common7\Tools\VsDevCmd.bat &&

# Default to PowerShell if no other command specified.
CMD ["powershell.exe", "-NoLogo", "-ExecutionPolicy", "Bypass"]
```

   > [!WARNING]
   > Visual Studio 2017 sürüm 15,8 veya öncesi (herhangi bir ürünü) üzerinde mcr düzgün yüklenmez\.microsoft\.com\/windows\/servercore:1809 veya üzeri. Herhangi bir hata görüntülenir.
   >
   > Bkz: [bilinen sorunlar kapsayıcılar için](build-tools-container-issues.md) daha fazla bilgi için.

::: moniker-end

::: moniker range="vs-2019"

```dockerfile
# escape=`

# Use a specific tagged image. Tags can be changed, though that is unlikely for most images.
# You could also use the immutable tag @sha256:324e9ab7262331ebb16a4100d0fb1cfb804395a766e3bb1806c62989d1fc1326
ARG FROM_IMAGE=mcr.microsoft.com/dotnet/framework/sdk:4.8-windowsservercore-ltsc2019
FROM ${FROM_IMAGE}

# Copy our Install script.
COPY Install.cmd C:\TEMP\

# Download collect.exe in case of an install failure.
ADD https://aka.ms/vscollect.exe C:\TEMP\collect.exe

# Use the latest release channel. For more control, specify the location of an internal layout.
ARG CHANNEL_URL=https://aka.ms/vs/16/release/channel
ADD ${CHANNEL_URL} C:\TEMP\VisualStudio.chman

# Download and install Build Tools excluding workloads and components with known issues.
ADD https://aka.ms/vs/16/release/vs_buildtools.exe C:\TEMP\vs_buildtools.exe
RUN C:\TEMP\Install.cmd C:\TEMP\vs_buildtools.exe --quiet --wait --norestart --nocache `
    --installPath C:\BuildTools `
    --channelUri C:\TEMP\VisualStudio.chman `
    --installChannelUri C:\TEMP\VisualStudio.chman `
    --all `
    --remove Microsoft.VisualStudio.Component.Windows10SDK.10240 `
    --remove Microsoft.VisualStudio.Component.Windows10SDK.10586 `
    --remove Microsoft.VisualStudio.Component.Windows10SDK.14393 `
    --remove Microsoft.VisualStudio.Component.Windows81SDK

# Start developer command prompt with any other commands specified.
ENTRYPOINT C:\BuildTools\Common7\Tools\VsDevCmd.bat &&

# Default to PowerShell if no other command specified.
CMD ["powershell.exe", "-NoLogo", "-ExecutionPolicy", "Bypass"]
```

::: moniker-end

Geçerli çalışma dizininde görüntüsünü oluşturmak için aşağıdaki komutu çalıştırın:

::: moniker range="vs-2017"

```shell
docker build -t buildtools2017:15.6.27428.2037 -t buildtools2017:latest -m 2GB .
```

::: moniker-end

::: moniker range="vs-2019"

```shell
docker build -t buildtools2019:16.0.28714.193 -t buildtools2019:latest -m 2GB .
```

::: moniker-end

İsteğe bağlı olarak veya her ikisi de geçirmek `FROM_IMAGE` veya `CHANNEL_URL` bağımsız değişkenleri kullanarak `--build-arg` farklı bir temel görüntü veya bir sabit görüntü korumak için bir iç düzen konumunu belirtmek için komut satırı anahtarı.

## <a name="diagnosing-install-failures"></a>Yükleme hatalarını tanılama

Bu örnek, belirli araçları yükler ve karmalar eşleştiğini doğrular. Yükleme hatası oluşursa, hatayı çözümlemek için konak makinenizi günlükleri kopyalayabilirsiniz. böylece en son Visual Studio ve .NET günlük toplama yardımcı programının de yükler.

::: moniker range="vs-2017"

```shell
> docker build -t buildtools2017:15.6.27428.2037 -t buildtools2017:latest -m 2GB .
Sending build context to Docker daemon

...
Step 8/10 : RUN C:\TEMP\Install.cmd C:\TEMP\vs_buildtools.exe --quiet --wait --norestart --nocache ...
 ---> Running in 4b62b4ce3a3c
The command 'cmd /S /C C:\TEMP\Install.cmd C:\TEMP\vs_buildtools.exe ...' returned a non-zero code: 1603

> docker cp 4b62b4ce3a3c:C:\vslogs.zip "%TEMP%\vslogs.zip"
```

::: moniker-end

::: moniker range="vs-2019"

```shell
> docker build -t buildtools2019:16.0.28714.193 -t buildtools2019:latest -m 2GB .
Sending build context to Docker daemon

...
Step 8/10 : RUN C:\TEMP\Install.cmd C:\TEMP\vs_buildtools.exe --quiet --wait --norestart --nocache ...
 ---> Running in 4b62b4ce3a3c
The command 'cmd /S /C C:\TEMP\Install.cmd C:\TEMP\vs_buildtools.exe ...' returned a non-zero code: 1603

> docker cp 4b62b4ce3a3c:C:\vslogs.zip "%TEMP%\vslogs.zip"
```

::: moniker-end

Son satırı yürütme sona erdikten sonra "% TEMP%\vslogs.zip" makinenizde açın veya sorun gönderme sırasında [Geliştirici topluluğu](https://developercommunity.visualstudio.com) Web sitesi.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Derleme Araçlarını Bir Kapsayıcıya Yükleme](build-tools-container.md)
* [Kapsayıcılar için Bilinen Sorunlar](build-tools-container-issues.md)
* [Visual Studio derleme araçları iş yükü ve Bileşen kimlikleri](workload-component-id-vs-build-tools.md)
