---
title: SignFile görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#SignFile
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, SignFile task
- SignFile task [MSBuild]
ms.assetid: edef1819-ddeb-4e09-95de-fc7063ba9388
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 496017f386e731e553bfce237bd1d2eabea46f49
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62976449"
---
# <a name="signfile-task"></a>SignFile görevi

Belirtilen dosyayı belirtilen sertifikayı kullanarak imzalar.

## <a name="parameters"></a>Parametreler

 Parametreleri aşağıdaki tabloda açıklanmıştır `SignFile` görev.

 SHA-256'yı sertifikaları izin verilen .NET 4.5 olan makinelere ve daha yüksek olduğunu unutmayın.

> [!WARNING]
> Visual Studio 2013 güncelleştirme 3'te başlayarak, bu görevin dosyası için hedef framework sürümünü belirtmenizi sağlayan yeni bir imzası vardır. SHA-256'yı MSBuild işleminde kullandığı için mümkün olan karma yere yalnızca hedef Framework'ü .NET 4.5 olduğunda yeni imza kullanmak için kullanmaları ya da daha yüksek olursunuz. Aşağıda veya .NET 4.0 hedef çerçeve ise SHA-256 karma kullanılmayacak.

|Parametre|Açıklama|
|---------------|-----------------|
|`CertificateThumbprint`|Gerekli `String` parametresi.<br /><br /> İmzalama için kullanılacak sertifikayı belirtir. Bu sertifika, geçerli kullanıcının kişisel deposunda olmalıdır.|
|`SigningTarget`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Sertifika ile imzalamak için dosyaları belirtir.|
|`TimestampUrl`|İsteğe bağlı `String` parametresi.<br /><br /> Zaman damgası sunucusunun URL'sini belirtir.|
|`TargetFrameworkVersion`|Hedef için kullanılan .NET Framework sürümü.|

## <a name="remarks"></a>Açıklamalar

 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [görev taban sınıfı](../msbuild/task-base-class.md).

## <a name="example"></a>Örnek

 Aşağıdaki örnekte `SignFile` belirtilen dosyaları imzalamak için görev `FilesToSign` koleksiyon öğesi tarafından belirtilen sertifika ile `Certificate` özelliği.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
    <ItemGroup>
        <FileToSign Include="File.exe" />
    </ItemGroup>
    <PropertyGroup>
        <Certificate>Cert.cer</Certificate>
    </PropertyGroup>
    <Target Name="Sign">
        <SignFile
            CertificateThumbprint="$(CertificateThumbprint)"
            SigningTarget="@(FileToSign)"
            TargetFrameworkVersion="v4.5" />
    </Target>
</Project>
```

> [!NOTE]
> Sertifika parmak izini sertifika SHA-1 karmasını ' dir. Daha fazla bilgi için [SHA-1 karmasını bir güvenilen kök CA sertifikası elde](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc733076\(v\=ws.10\)). Sertifika ayrıntıları parmak izini kopyalayıp, ek (3F) içermez emin engelleyebilir görünmez karakter `SignFile` gelen sertifikayı bulma.

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Görevler](../msbuild/msbuild-tasks.md)