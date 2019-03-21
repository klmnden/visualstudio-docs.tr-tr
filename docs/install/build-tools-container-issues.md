---
title: Kapsayıcılar için bilinen sorunlar
description: Visual Studio derleme araçları bir Windows kapsayıcısına yükleme sırasında oluşabilecek bilinen sorunlar hakkında daha fazla bilgi edinin.
ms.date: 04/18/2018
ms.custom: seodec18
ms.topic: conceptual
ms.assetid: 140083f1-05bc-4014-949e-fb5802397c7a
author: heaths
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: e5dc37eb38bf0d474e2a701bc79b8d4866be4aef
ms.sourcegitcommit: 3d37c2460584f6c61769be70ef29c1a67397cf14
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2019
ms.locfileid: "58323659"
---
# <a name="known-issues-for-containers"></a>Kapsayıcılar için bilinen sorunlar

Visual Studio'yu bir Docker kapsayıcısına yüklerken birkaç sorun vardır.

::: moniker range="vs-2017"

## <a name="windows-container"></a>Windows kapsayıcısı

Aşağıdaki bilinen sorunlar ortaya çıkar Visual Studio derleme araçları 2017 Windows kapsayıcısına yükleyin.

* Visual Studio görüntü microsoft/windowsservercore:10.0.14393.1593 alarak bir kapsayıcı içinde yükleyemezsiniz. Önce veya sonra 10.0.14393 çalışmalıdır Windows sürümleri ile etiketlenmiş görüntüler.
* Windows SDK'sı sürüm 10.0.14393 yükleyemezsiniz veya önceki sürümleri. Bazı paketler yüklenemedi ve bu paketleri kullanan iş yükleri çalışmaz.
* Geçirmek `-m 2GB` (veya daha fazlası) görüntü oluşturulurken. Bazı iş yükleri varsayılandan daha fazla belleğe ihtiyaç 1 yüklü olduğunda GB.
* Docker varsayılandan daha büyük diskleri kullanacak şekilde yapılandırma 20 GB.
* Geçirmek `--norestart` komut satırında. Bu yazma olduğu gibi bir Windows kapsayıcı içinden başlatmayı denemeden kapsayıcı döndürür `ERROR_TOO_MANY_OPEN_FILES` konağa.
* Görüntünüzü doğrudan microsoft/windowsservercore üzerinde temel alıyorsa, .NET Framework düzgün yüklenmeyebilir ve herhangi bir yükleme hata gösterilir. Yükleme tamamlandıktan sonra yönetilen kod çalışmayabilir. Görüntünüzü bunun yerine, temel [microsoft/dotnet-framework:4.7.1](https://hub.docker.com/r/microsoft/dotnet-framework) veya üzeri. Örneğin, gibi MSBuild ile derleme yaparken bir hata görebilirsiniz:

  > C:\BuildTools\MSBuild\15.0\bin\Roslyn\Microsoft.CSharp.Core.targets(84,5): error MSB6003: Belirtilen görev yürütülebilir "csc.exe" çalıştırılamadı. Dosya veya derleme yüklenemedi ' System.IO.FileSystem, sürüm 4.0.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a ' veya bağımlılıklarından biri. Sistem belirtilen dosyayı bulamıyor.

* Visual Studio 2017 sürüm 15,8 veya önceki bir sürümünü yükleyemezsiniz (herhangi bir ürünü) mcr.microsoft.com/windows/servercore:1809 veya üzeri. Daha fazla bilgi edinmek için bkz. https://aka.ms/setup/containers/servercore1809.

::: moniker-end

## <a name="build-tools-container"></a>Araçlar kapsayıcısı oluşturun

Bir derleme araçları kapsayıcı kullandığınızda, aşağıdaki bilinen sorunlar ortaya çıkabilir. Sorunları düzelttik olup olmadığını görmek için veya diğer bilinen bir sorun varsa ziyaret https://developercommunity.visualstudio.com.

* IntelliTrace çalışmayabilir [bazı senaryolar](https://github.com/Microsoft/vstest/issues/940) bir kapsayıcı içinde.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Derleme Araçlarını Bir Kapsayıcıya Yükleme](build-tools-container.md)
* [Kapsayıcılar için İleri Düzey Örnek](advanced-build-tools-container.md)
* [Visual Studio derleme araçları iş yükü ve Bileşen kimlikleri](workload-component-id-vs-build-tools.md)
