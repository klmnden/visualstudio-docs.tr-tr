---
title: Kapsayıcılar için bilinen sorunlar
description: Visual Studio derleme araçları bir Windows kapsayıcısına yükleme sırasında oluşabilecek bilinen sorunlar hakkında daha fazla bilgi edinin.
ms.date: 07/03/2019
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
ms.openlocfilehash: edaadc6c551a6f138f505dec8fe45c9df570dfd6
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67823315"
---
# <a name="known-issues-for-containers"></a>Kapsayıcılar için bilinen sorunlar

Visual Studio'yu bir Docker kapsayıcısına yüklerken birkaç sorun vardır.

## <a name="windows-container"></a>Windows kapsayıcısı

Aşağıdaki bilinen sorunlar ortaya çıkar Visual Studio derleme araçları bir Windows kapsayıcısına yükleyin.

::: moniker range="vs-2017"

* Visual Studio görüntü microsoft/windowsservercore:10.0.14393.1593 alarak bir kapsayıcı içinde yükleyemezsiniz. Önce veya sonra 10.0.14393 çalışmalıdır Windows sürümleri ile etiketlenmiş görüntüler.

* Windows SDK'sı sürüm 10.0.14393 yükleyemezsiniz veya önceki sürümleri. Bazı paketler yüklenemedi ve bu paketleri kullanan iş yükleri çalışmaz.

::: moniker-end

* Geçirmek `-m 2GB` (veya daha fazlası) görüntü oluşturulurken. Bazı iş yükleri varsayılandan daha fazla belleğe ihtiyaç 1 yüklü olduğunda GB.
* Docker varsayılandan daha büyük diskleri kullanacak şekilde yapılandırma 20 GB.
* Geçirmek `--norestart` komut satırında. Bu yazma olduğu gibi bir Windows kapsayıcı içinden başlatmayı denemeden kapsayıcı döndürür `ERROR_TOO_MANY_OPEN_FILES` konağa.
* Görüntünüzü doğrudan microsoft/windowsservercore üzerinde temel alıyorsa, .NET Framework düzgün yüklemeyebilir ve herhangi bir yükleme hata gösterilir. Yükleme tamamlandıktan sonra yönetilen kod çalışmayabilir. Görüntünüzü bunun yerine, temel [microsoft/dotnet-framework:4.7.1](https://hub.docker.com/r/microsoft/dotnet-framework) veya üzeri. Örneğin, aşağıdakine benzer MSBuild ile derleme yaparken bir hata görebilirsiniz:

  > C:\BuildTools\MSBuild\15.0\bin\Roslyn\Microsoft.CSharp.Core.targets(84,5): error MSB6003: Belirtilen görev yürütülebilir "csc.exe" çalıştırılamadı. Dosya veya derleme yüklenemedi ' System.IO.FileSystem, sürüm 4.0.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a ' veya bağımlılıklarından biri. Sistem belirtilen dosyayı bulamıyor.

::: moniker range="vs-2017"

* Visual Studio 2017 sürüm 15,8 veya önceki bir sürümünü yükleyemezsiniz (herhangi bir ürünü) mcr.microsoft.com/windows/servercore:1809 veya üzeri. Daha fazla bilgi edinmek için bkz. https://aka.ms/setup/containers/servercore1809.

::: moniker-end

## <a name="build-tools-container"></a>Araçlar kapsayıcısı oluşturun

Bir derleme araçları kapsayıcı kullandığınızda, aşağıdaki bilinen sorunlar ortaya çıkabilir. Sorunları düzelttik olup olmadığını görmek için veya diğer bilinen bir sorun varsa ziyaret https://developercommunity.visualstudio.com.

* IntelliTrace çalışmayabilir [bazı senaryolar](https://github.com/Microsoft/vstest/issues/940) bir kapsayıcı içinde.
* Docker için Windows önceki sürümlerinde, varsayılan kapsayıcı görüntü boyutu yalnızca 20 GB'tır ve derleme araçları uygun değildir. İzleyin [görüntü boyutunu değiştirmek için yönergeler](https://docs.microsoft.com/virtualization/windowscontainers/manage-containers/container-storage#image-size) 127 GB veya daha fazla.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Derleme Araçlarını Bir Kapsayıcıya Yükleme](build-tools-container.md)
* [Kapsayıcılar için İleri Düzey Örnek](advanced-build-tools-container.md)
* [Visual Studio derleme araçları iş yükü ve Bileşen kimlikleri](workload-component-id-vs-build-tools.md)
