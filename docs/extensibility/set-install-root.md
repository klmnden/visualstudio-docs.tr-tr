---
title: VSIX v3 ile uzantılar klasörünün dışına yükleme | Microsoft Docs
ms.date: 11/09/2016
ms.topic: conceptual
ms.assetid: 913c3745-8aa9-4260-886e-a05aecfb2225
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 847ce9bc55e93f292ffdfe6f237e8c39eeac9fd4
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53968504"
---
# <a name="installing-outside-the-extensions-folder"></a>Uzantılar klasörünün dışına yükleme

Visual Studio 2017 ve VSIX v3 ile başlayan (uzantı varlıklar uzantılar klasörünün dışına yükleme için artık destek sürüm 3). Şu anda, aşağıdaki konumlardan, geçerli yükleme konumlarını (burada [INSTALLDIR] Visual Studio örneğinin yükleme dizinine eşlendi) olarak etkin değil:

* [INSTALLDİR] \MSBuild
* [INSTALLDİR] \Xml\Schemas
* [INSTALLDİR] \Common7\IDE\PublicAssemblies
* [INSTALLDİR] \Licenses
* [INSTALLDİR] \Common7\IDE\ReferenceAssemblies
* [INSTALLDİR] \Common7\IDE\RemoteDebugger
* [INSTALLDİR] \Common7\IDE\VC\VCTargets

>**Not:** VSIX biçimi VS yükleme klasör yapısını dışında yüklemeye izin vermiyor.

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

>**Not:** Tercih ederseniz, .csproj dosyasını doğrudan düzenleyebilirsiniz.

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
