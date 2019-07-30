---
title: MSBuild hedef çerçevesi ve hedef platform | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: df6517c5-edd6-4cc4-97ad-b3cdfc78e799
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 00874c8fd7ded67c380de1166d7e9753a3bd3c24
ms.sourcegitcommit: 044bb54cb4552c8f4651feb11d62e52726117e75
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68662047"
---
# <a name="msbuild-target-framework-and-target-platform"></a>MSBuild hedef çerçevesi ve hedef platform
Bir proje, .NET Framework belirli bir sürümü ve belirli bir yazılım mimarisi olan bir *hedef platform*olan bir *hedef çerçeve*üzerinde çalışmak üzere oluşturulabilir.  Örneğin, 2,0 bitlik bir platformda .NET Framework ' de çalışacak bir uygulamayı, 802x86 işlemci ailesi ("x86") ile uyumlu 32 bir şekilde hedefleyebilirsiniz. Hedef Framework ve hedef platformun birleşimi *hedef bağlam*olarak bilinir.

> [!IMPORTANT]
> Bu makalede, hedef çerçeve belirtmenin eski yolu gösterilmektedir. SDK stilindeki projeler Netstandard gibi farklı Targetçerçeveleri etkinleştirir. Daha fazla bilgi için bkz. [hedef çerçeveler](/dotnet/standard/frameworks).

## <a name="target-framework-and-profile"></a>Hedef çerçeve ve profil
 Hedef çerçeve, projenizin üzerinde çalışmak üzere oluşturulduğu .NET Framework belirli sürümüdür. Bir hedef Framework belirtimi, bu Framework sürümü için özel derleyici özellikleri ve derleme başvuruları sağladığından gereklidir.

 Şu anda .NET Framework aşağıdaki sürümleri kullanılabilir:

- .NET Framework 2,0 (Visual Studio 2005 ' de bulunur)

- .NET Framework 3,0 (içinde [!INCLUDE[wiprlhext](../debugger/includes/wiprlhext_md.md)]bulunur)

- .NET Framework 3,5 (içinde [!INCLUDE[vs_orcas_long](../debugger/includes/vs_orcas_long_md.md)]bulunur)

- .NET Framework 4.5.2

- .NET Framework 4,6 (içinde [!INCLUDE[vs_dev14](../misc/includes/vs_dev14_md.md)]bulunur)

- .NET Framework 4.6.1

- .NET Framework 4.6.2

- .NET Framework 4,7

- .NET Framework 4.7.1

- .NET Framework 4.7.2

- .NET Framework 4,8

.NET Framework sürümleri, her birinin başvuru için kullanılabilir hale getiren derlemeler listesinde diğerinden farklıdır. Örneğin, projeniz .NET Framework sürüm 3,0 veya üzerini hedeflediğinden, Windows Presentation Foundation (WPF) uygulamaları derlenemez.

Hedef çerçeve, proje dosyasındaki `TargetFrameworkVersion` özelliğinde belirtilmiştir. Visual Studio tümleşik geliştirme ortamındaki (IDE) proje özelliği sayfalarını kullanarak bir projenin hedef çerçevesini değiştirebilirsiniz. Daha fazla bilgi için [nasıl yapılır: .NET Framework](../ide/how-to-target-a-version-of-the-dotnet-framework.md)bir sürümünü hedefleyin. `TargetFrameworkVersion` İçin kullanılabilirdeğerler`v4.6.1`, `v3.0` ,,`v4.7.2`,,,,, ,ve`v4.7.1` `v3.5` `v2.0` `v4.5.2` `v4.6` `v4.6.2` `v4.7` `v4.8`.

```xml
<TargetFrameworkVersion>v4.0</TargetFrameworkVersion>
```

 *Hedef profil* , hedef Framework 'ün bir alt kümesidir. Örneğin, .NET Framework 4 Istemci profili MSBuild derlemelerine başvuruları içermez.

 Hedef profil, bir proje dosyasındaki `TargetFrameworkProfile` özelliğinde belirtilmiştir. IDE 'deki proje özelliği sayfalarında Target-Framework denetimini kullanarak hedef profilini değiştirebilirsiniz. Daha fazla bilgi için [nasıl yapılır: .NET Framework](../ide/how-to-target-a-version-of-the-dotnet-framework.md)bir sürümünü hedefleyin.

```xml
<TargetFrameworkVersion>v4.0</TargetFrameworkVersion>
<TargetFrameworkProfile>Client</TargetFrameworkProfile>
```

## <a name="target-platform"></a>Hedef platform
 *Platform* , belirli bir çalışma zamanı ortamını tanımlayan donanım ve yazılım birleşimidir. Örneğin,

- `x86`Intel 80x86 işlemcisi üzerinde veya eşdeğeri olan 32 bitlik bir Windows işletim sistemi belirler.

- `x64`Intel x64 işlemci veya BT eşdeğeri üzerinde çalışan 64 bitlik bir Windows işletim sistemi belirler.

- `Xbox`Microsoft Xbox 360 platformunu belirtir.

*Hedef platform* , projenizin üzerinde çalışmak üzere oluşturulduğu özel platformdur. Hedef platform bir proje dosyasındaki `PlatformTarget` Build özelliğinde belirtilmiştir. Hedef platformu, proje özelliği sayfalarını veya IDE 'deki **Configuration Manager** kullanarak değiştirebilirsiniz.

```xml
<PropertyGroup>
   <PlatformTarget>x86</PlatformTarget>
</PropertyGroup>

```

*Hedef yapılandırma* , hedef platformun bir alt kümesidir. Örneğin, `x86``Debug` yapılandırma çoğu kod iyileştirmesini içermez. Hedef yapılandırma bir proje dosyasındaki `Configuration` Build özelliğinde belirtilir. Proje özellik sayfaları veya **Configuration Manager**kullanarak hedef yapılandırmayı değiştirebilirsiniz.

```xml
<PropertyGroup>
   <PlatformTarget>x86</PlatformTarget>
   <Configuration>Debug</Configuration>
<PropertyGroup>

```

## <a name="see-also"></a>Ayrıca bkz.
- [Çoklu Sürüm Desteği](../msbuild/msbuild-multitargeting-overview.md)
