---
title: Visual Studio derleme araçları bir kapsayıcıya yükleme
titleSuffix: ''
description: Visual Studio derleme araçları, sürekli tümleştirme ve sürekli teslim (CI/CD) iş akışlarını destekleyen bir Windows kapsayıcısına yüklemeyi öğrenin.
ms.date: 04/18/2018
ms.custom: seodec18
ms.topic: conceptual
ms.assetid: d5c038e2-e70d-411e-950c-8a54917b578a
author: heaths
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 1c7d4b2cb910a6e6ee55ecb783fe124958d251e2
ms.sourcegitcommit: 3cc73e74921a9ceb622542e0e263abeebc455c00
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/08/2019
ms.locfileid: "67624109"
---
# <a name="install-build-tools-into-a-container"></a>Derleme araçları bir kapsayıcıya yükleme

Visual Studio derleme araçları, sürekli tümleştirme ve sürekli teslim (CI/CD) iş akışlarını destekleyen bir Windows kapsayıcısına yükleyebilirsiniz. Bu makalede hangi Docker yapılandırma değişikliklerini ne yanı sıra gerekli aracılığıyla kılavuzları [iş yüklerinin ve bileşenlerin](workload-component-id-vs-build-tools.md) bir kapsayıcıda yükleyebilirsiniz.

[Kapsayıcıları](https://www.docker.com/what-container) yalnızca bir CI/CD sunucu ortamında, ancak geliştirme ortamları için kullanabileceğiniz bir tutarlı yapı sistemi paketlemek için harika bir yoludur. Örneğin, kaynak kodunuzu kodunuzu yazmak için Visual Studio veya diğer araçları kullanmaya devam ederken, özelleştirilmiş bir ortamı tarafından oluşturulacak bir kapsayıcıya bağlayabilir. CI/CD akışınızı aynı kapsayıcı görüntüsü kullanıyorsa, tutarlı bir şekilde, kodunuzun derlendiğinden güvenli yaslayabilirsiniz. Kapsayıcıları, birden çok kapsayıcı bir düzenleme sistemi ile kullanarak mikro hizmetler için ortak olan çalışma zamanı tutarlılık için de kullanabilirsiniz; Ancak, bu makalenin kapsamı dışındadır olur.

Visual Studio derleme araçları, kaynak kodunuzu derlemek için ihtiyacınız yoksa, aynı adımları diğer Visual Studio ürünleri için kullanılabilir. Ancak, komutların otomatik şekilde Windows kapsayıcıları etkileşimli bir kullanıcı arabirimi desteklemediğini unutmayın.

## <a name="before-you-begin"></a>Başlamadan önce

Bazı konusunda [Docker](https://www.docker.com/what-docker) aşağıda varsayılır. Zaten Windows Docker çalıştırmayla ilgili bilgi sahibi değilseniz, konusunu okuyun [yükleme ve Windows Docker altyapısı yapılandırma](https://docs.microsoft.com/virtualization/windowscontainers/manage-docker/configure-docker-daemon).

Aşağıdaki temel görüntü bir örnektir ve sisteminiz için çalışmayabilir. Okuma [Windows kapsayıcı sürümü uyumluluğu](https://docs.microsoft.com/virtualization/windowscontainers/deploy-containers/version-compatibility) hangi temel görüntü belirlemek için ortamınızı kullanmanız gerekir.

## <a name="create-and-build-the-dockerfile"></a>Oluşturma ve Dockerfile'ı oluşturma

Aşağıdaki örnek Dockerfile, disk üzerinde yeni bir dosyaya kaydedin. Dosya yalnızca "Dockerfile" ise, varsayılan olarak kabul edilir.

> [!WARNING]
> Bu örnekte, yalnızca önceki Windows kapsayıcılarına yüklü SDK'ları Dockerfile dışlar. Önceki sürümlerde, derleme komutunun başarısız olmasına neden.

1. Bir komut istemi açın.

1. (Önerilen) yeni bir dizin oluşturun:

   ```shell
   mkdir C:\BuildTools
   ```

1. Bu yeni dizine dizinleri değiştirin:

   ```shell
   cd C:\BuildTools
   ```

1. Aşağıdaki içeriğe C:\BuildTools\Dockerfile için kaydedin.
 
   ::: moniker range="vs-2017"

   ```dockerfile
   # escape=`

   # Use the latest Windows Server Core image with .NET Framework 4.7.2.
   FROM mcr.microsoft.com/dotnet/framework/sdk:4.7.2-windowsservercore-ltsc2019

   # Restore the default Windows shell for correct batch processing.
   SHELL ["cmd", "/S", "/C"]

   # Download the Build Tools bootstrapper.
   ADD https://aka.ms/vs/15/release/vs_buildtools.exe C:\TEMP\vs_buildtools.exe

   # Install Build Tools excluding workloads and components with known issues.
   RUN C:\TEMP\vs_buildtools.exe --quiet --wait --norestart --nocache `
       --installPath C:\BuildTools `
       --all `
       --remove Microsoft.VisualStudio.Component.Windows10SDK.10240 `
       --remove Microsoft.VisualStudio.Component.Windows10SDK.10586 `
       --remove Microsoft.VisualStudio.Component.Windows10SDK.14393 `
       --remove Microsoft.VisualStudio.Component.Windows81SDK `
    || IF "%ERRORLEVEL%"=="3010" EXIT 0

   # Start developer command prompt with any other commands specified.
   ENTRYPOINT C:\BuildTools\Common7\Tools\VsDevCmd.bat &&

   # Default to PowerShell if no other command specified.
   CMD ["powershell.exe", "-NoLogo", "-ExecutionPolicy", "Bypass"]
   ```

   > [!WARNING]
   > Görüntünüzü doğrudan microsoft/windowsservercore veya mcr.microsoft.com/windows/servercore temel değilse (bkz [Microsoft syndicates kapsayıcı Kataloğu](https://azure.microsoft.com/blog/microsoft-syndicates-container-catalog/)), .NET Framework düzgün yüklemeyebilir ve hiçbir yükleme hatası gösterilir. Yükleme tamamlandıktan sonra yönetilen kod çalışmayabilir. Görüntünüzü bunun yerine, temel [microsoft/dotnet-framework:4.7.2](https://hub.docker.com/r/microsoft/dotnet-framework) veya üzeri. Ayrıca görüntüleri sürüm 4.7.2 etiketli dikkat edin veya daha sonra PowerShell varsayılan olarak kullanabilir `SHELL`, neden olacak `RUN` ve `ENTRYPOINT` başarısız için yönergeler.
   >
   > Visual Studio 2017 sürüm 15,8 veya öncesi (herhangi bir ürünü) mcr.microsoft.com/windows/servercore:1809 veya sonraki sürümlerde düzgün yüklenmez. Herhangi bir hata görüntülenir.
   >
   > Bkz: [Windows kapsayıcı sürümü uyumluluğu](https://docs.microsoft.com/virtualization/windowscontainers/deploy-containers/version-compatibility) hangi konak işletim sistemi sürümlerinde, hangi kapsayıcı işletim sistemi sürümlerin desteklendiğini görmek için ve [bilinen sorunlar kapsayıcılar için](build-tools-container-issues.md) bilinen sorunlara yönelik çözümler.

   ::: moniker-end

   ::: moniker range="vs-2019"

   ```dockerfile
   # escape=`

   # Use the latest Windows Server Core image with .NET Framework 4.8.
   FROM mcr.microsoft.com/dotnet/framework/sdk:4.8-windowsservercore-ltsc2019

   # Restore the default Windows shell for correct batch processing.
   SHELL ["cmd", "/S", "/C"]

   # Download the Build Tools bootstrapper.
   ADD https://aka.ms/vs/16/release/vs_buildtools.exe C:\TEMP\vs_buildtools.exe

   # Install Build Tools excluding workloads and components with known issues.
   RUN C:\TEMP\vs_buildtools.exe --quiet --wait --norestart --nocache `
       --installPath C:\BuildTools `
       --all `
       --remove Microsoft.VisualStudio.Component.Windows10SDK.10240 `
       --remove Microsoft.VisualStudio.Component.Windows10SDK.10586 `
       --remove Microsoft.VisualStudio.Component.Windows10SDK.14393 `
       --remove Microsoft.VisualStudio.Component.Windows81SDK `
    || IF "%ERRORLEVEL%"=="3010" EXIT 0

   # Start developer command prompt with any other commands specified.
   ENTRYPOINT C:\BuildTools\Common7\Tools\VsDevCmd.bat &&

   # Default to PowerShell if no other command specified.
   CMD ["powershell.exe", "-NoLogo", "-ExecutionPolicy", "Bypass"]
   ```

   > [!WARNING]
   > Görüntünüzü doğrudan microsoft/windowsservercore üzerinde temel alıyorsa, .NET Framework düzgün yüklemeyebilir ve herhangi bir yükleme hata gösterilir. Yükleme tamamlandıktan sonra yönetilen kod çalışmayabilir. Görüntünüzü bunun yerine, temel [microsoft/dotnet-framework: 4.8](https://hub.docker.com/r/microsoft/dotnet-framework) veya üzeri. Görüntüleri 4,8 veya sonraki bir sürümü etiketli Not Varsayılan olarak PowerShell de kullanabilirsiniz `SHELL`, neden olacak `RUN` ve `ENTRYPOINT` başarısız için yönergeler.
   >
   > Bkz: [Windows kapsayıcı sürümü uyumluluğu](https://docs.microsoft.com/virtualization/windowscontainers/deploy-containers/version-compatibility) hangi konak işletim sistemi sürümlerinde, hangi kapsayıcı işletim sistemi sürümlerin desteklendiğini görmek için ve [bilinen sorunlar kapsayıcılar için](build-tools-container-issues.md) bilinen sorunlara yönelik çözümler.

   ::: moniker-end

1. Bu dizinin içinde aşağıdaki komutu çalıştırın.

   ::: moniker range="vs-2017"

   ```shell
   docker build -t buildtools2017:latest -m 2GB .
   ```

   Bu komut Dockerfile 2 GB bellek kullanarak geçerli dizinde oluşturur. Bazı iş yükleri yüklenirken varsayılan 1 GB yeterli değildir; ancak yalnızca 1 GB bellek, derleme gereksinimlerinize bağlı olarak ile derlemeniz mümkün olabilir.

   Son görüntü etiketli "buildtools2017:latest" olduğundan, hiçbir etiket belirtilirse "son" etiketi varsayılan olduğundan kolayca bir kapsayıcıda "buildtools2017" çalıştırabilirsiniz. Daha belirli bir Visual Studio derleme araçları 2017 sürümüne kullanmak istiyorsanız [Gelişmiş senaryo](advanced-build-tools-container.md), bunun yerine belirli bir kapsayıcıda etiketi Visual Studio, sayı olarak "son" belirli bir kapsayıcı kullanabilmeniz için derleme Sürüm tutarlı bir şekilde.

   ::: moniker-end

   ::: moniker range="vs-2019"

   ```shell
   docker build -t buildtools2019:latest -m 2GB .
   ```

   Bu komut Dockerfile 2 GB bellek kullanarak geçerli dizinde oluşturur. Bazı iş yükleri yüklenirken varsayılan 1 GB yeterli değildir; ancak yalnızca 1 GB bellek, derleme gereksinimlerinize bağlı olarak ile derlemeniz mümkün olabilir.

   Son görüntü etiketli "buildtools2019:latest" olduğundan, hiçbir etiket belirtilirse "son" etiketi varsayılan olduğundan kolayca bir kapsayıcıda "buildtools2019" çalıştırabilirsiniz. Visual Studio derleme araçları 2019 daha içinde belirli bir sürümünü kullanmak istiyorsanız [Gelişmiş senaryo](advanced-build-tools-container.md), bunun yerine belirli bir kapsayıcıda etiketi Visual Studio, sayı olarak "son" belirli bir kapsayıcı kullanabilmeniz için derleme Sürüm tutarlı bir şekilde.

   ::: moniker-end

## <a name="using-the-built-image"></a>Oluşturulan görüntüyü kullanarak

Görüntü oluşturduğunuza göre etkileşimli ve otomatik yapılara yapmak için bir kapsayıcı içinde çalıştırabilirsiniz. Örneğin, yol ve diğer ortam değişkenlerine zaten yapılandırılmış Geliştirici komut istemi kullanır.

1. Bir komut istemi açın.

1. Kapsayıcı tüm geliştirici ile bir PowerShell ortamı başlatmak için ayarlanan ortam değişkenlerine çalıştırın:

   ::: moniker range="vs-2017"

   ```shell
   docker run -it buildtools2017
   ```

   ::: moniker-end

   ::: moniker range="vs-2019"

   ```shell
   docker run -it buildtools2019
   ```

   ::: moniker-end

CI/CD akışınız için bu görüntüyü kullanmak için kendi değerlerinizle yayımlayabilirsiniz [Azure Container Registry](https://azure.microsoft.com/services/container-registry) veya diğer iç [Docker kayıt defteri](https://docs.docker.com/registry/deploying) sunucuları yalnızca çekme gerekmez.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Kapsayıcılar için İleri Düzey Örnek](advanced-build-tools-container.md)
* [Kapsayıcılar için Bilinen Sorunlar](build-tools-container-issues.md)
* [Visual Studio derleme araçları iş yükü ve Bileşen kimlikleri](workload-component-id-vs-build-tools.md)
