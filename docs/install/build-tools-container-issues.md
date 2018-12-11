---
title: Kapsayıcılar için bilinen sorunlar
description: Visual Studio derleme araçları 2017 Windows kapsayıcısına yükleme sırasında oluşabilecek bilinen sorunlar hakkında daha fazla bilgi edinin.
ms.date: 04/18/2018
ms.technology: vs-acquisition
ms.custom: seodec18
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 140083f1-05bc-4014-949e-fb5802397c7a
author: heaths
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 529d967f34a5c99c8416058acad317cdc47d1053
ms.sourcegitcommit: 0cdd8e8a53fb4fd5e869f07c35204419fa12783d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53158625"
---
# <a name="known-issues-for-containers"></a>Kapsayıcılar için bilinen sorunlar

Visual Studio'yu bir Docker kapsayıcısına yüklerken birkaç sorun vardır.

## <a name="windows-container"></a>Windows kapsayıcısı

Aşağıdaki bilinen sorunlar ortaya çıkar Visual Studio derleme araçları 2017 Windows kapsayıcısına yükleyin.

* Visual Studio görüntü microsoft/windowsservercore:10.0.14393.1593 alarak bir kapsayıcı içinde yükleyemezsiniz. Daha eski veya yeni Windows sürümleri ile etiketlenmiş resimleri çalışması gerekir.
* Windows SDK sürümlerine 10.0.14393 eski yükleyemezsiniz. Bazı paketler yüklenemedi ve bu paketleri kullanan iş yükleri çalışmaz.
* Geçirmek `-m 2GB` (veya daha fazlası) görüntü oluşturulurken. Bazı iş yükleri varsayılandan daha fazla belleğe ihtiyaç 1 yüklü olduğunda GB.
* Docker varsayılandan daha büyük diskleri kullanacak şekilde yapılandırma 20 GB.
* Geçirmek `--norestart` komut satırında. Bu yazma olduğu gibi bir Windows kapsayıcı içinden başlatmayı denemeden kapsayıcı döndürür `ERROR_TOO_MANY_OPEN_FILES` konağa.
* Görüntünüzü doğrudan microsoft/windowsservercore üzerinde temel alıyorsa, .NET Framework düzgün yüklenmeyebilir ve herhangi bir yükleme hata gösterilir. Yükleme tamamlandıktan sonra yönetilen kod çalışmayabilir. Görüntünüzü bunun yerine, temel [microsoft/dotnet-framework:4.7.1](https://hub.docker.com/r/microsoft/dotnet-framework) ya da daha yeni. Örneğin, gibi MSBuild ile derleme yaparken bir hata görebilirsiniz:

  > C:\BuildTools\MSBuild\15.0\bin\Roslyn\Microsoft.CSharp.Core.targets(84,5): hata MSB6003: Belirtilen görev yürütülebilir "csc.exe" çalıştırılamadı. Dosya veya derleme yüklenemedi ' System.IO.FileSystem, sürüm 4.0.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a ' veya bağımlılıklarından biri. Sistem belirtilen dosyayı bulamıyor.

## <a name="build-tools-container"></a>Araçlar kapsayıcısı oluşturun

Bir derleme araçları kapsayıcı kullandığınızda, aşağıdaki bilinen sorunlar ortaya çıkabilir. Sorunları düzelttik olup olmadığını görmek için veya diğer bilinen bir sorun varsa ziyaret https://developercommunity.visualstudio.com.

* IntelliTrace çalışmayabilir [bazı senaryolar](https://github.com/Microsoft/vstest/issues/940) bir kapsayıcı içinde.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Derleme Araçlarını Bir Kapsayıcıya Yükleme](build-tools-container.md)
* [Kapsayıcılar için İleri Düzey Örnek](advanced-build-tools-container.md)
* [Visual Studio derleme araçları 2017 iş yükü ve Bileşen kimlikleri](workload-component-id-vs-build-tools.md)
