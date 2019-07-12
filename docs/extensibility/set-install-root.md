---
title: VSIX v3 ile uzantılar klasörünün dışına yükleme | Microsoft Docs
ms.date: 11/09/2016
ms.topic: conceptual
ms.assetid: 913c3745-8aa9-4260-886e-a05aecfb2225
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2d5fc36c1244edd0988b6b76f8106020369cd90b
ms.sourcegitcommit: da4079f5b6ec884baf3108cbd0519d20cb64c70b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "67852196"
---
# <a name="install-outside-the-extensions-folder"></a>Uzantılar klasörünün dışına yükleme

Visual Studio 2017 ve VSIX v3 ile (sürüm 3), uzantı varlıklar başlangıç uzantılar klasörünün dışına yüklenebilir. Şu anda, aşağıdaki konumlardan, geçerli yükleme konumlarını (burada [INSTALLDIR] Visual Studio örneğinin yükleme dizinine eşlendi) olarak etkin değil:

* [INSTALLDİR] \MSBuild
* [INSTALLDİR] \Xml\Schemas
* [INSTALLDIR]\Common7\IDE\PublicAssemblies
* [INSTALLDİR] \Licenses
* [INSTALLDİR] \Common7\IDE\ReferenceAssemblies
* [INSTALLDIR]\Common7\IDE\RemoteDebugger
* [INSTALLDİR] \Common7\IDE\VC\VCTargets (yalnızca Visual Studio 2017 için desteklenir; Visual Studio 2019 için kullanım dışı ve üzeri)

> [!NOTE]
> VSIX biçimi Visual Studio yükleme klasör yapısını dışında yüklemeye izin vermez. 

Bu dizinleri yüklemeyi desteklemek için VSIX "makine başına örnek başına" yüklenmelidir. Bu extension.vsixmanifest Tasarımcısı'nda "tüm kullanıcılar" onay kutusunu işaretleyerek etkin hale getirilebilir:

![tüm kullanıcılar](media/check-all-users.png)

## <a name="how-to-set-the-installroot"></a>InstallRoot ayarlama

Yükleme dizinleri belirlemek üzere kullanabileceğiniz **özellikleri** Visual Studio'daki. Örneğin, ayarlayabilirsiniz `InstallRoot` yukarıdaki konumlardan birine yapılan proje başvurusunun özelliği:

![kök özellikleri yükleme](media/install-root-properties.png)

Bu ilgili bazı meta veriler ekler `ProjectReference` içinde VSIX proje .csproj dosyasını özelliği:

```xml
 <ProjectReference Include="..\ClassLibrary1\ClassLibrary1.csproj">
        <Project>{69a979f1-eba2-43e7-9346-0e56e803508b}</Project>
        <Name>ClassLibrary1</Name>
        <InstallRoot>PublicAssemblies</InstallRoot>
 </ProjectReference>
```

> [!NOTE]
> Tercih ederseniz, .csproj dosyasını doğrudan düzenleyebilirsiniz.

## <a name="how-to-set-a-subpath-under-the-installroot"></a>Bir yükleme kökü altında InstallRoot ayarlama

Bir yükleme kökü altında yüklemek isteyip istemediğinizi `InstallRoot`, bunu ayarlayarak yapabilirsiniz `VsixSubPath` özelliği olduğu gibi `InstallRoot` özelliği. Örneği için yüklemek için proje başvurusunun çıkış istediğimizi varsayalım. ' [INSTALLDIR]\MSBuild\MyCompany\MySDK\1.0'. Kolayca özellik Tasarımcısı ile bunu yapabilirsiniz:

![set-yükleme kökü](media/set-subpath.png)

Karşılık gelen .csproj değişiklikleri şöyle görünür:

```xml
<ProjectReference Include="..\ClassLibrary1\ClassLibrary1.csproj">
       <Project>{69a979f1-eba2-43e7-9346-0e56e803508b}</Project>
       <Name>ClassLibrary1</Name>
       <InstallRoot>MSBuild</InstallRoot>
       <VSIXSubPath>MyCompany\MySDK\1.0</VSIXSubPath>
</ProjectReference>
```

## <a name="extra-information"></a>Ek bilgi

Özellik Tasarımcısı değişiklikleri daha fazlasını proje başvuruları için geçerlidir; ayarlayabileceğiniz `InstallRoot` meta verileri de, projedeki öğeleri için (yukarıda açıklanan aynı yöntemleri kullanarak).
