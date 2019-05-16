---
title: SignFile görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
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
caps.latest.revision: 23
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 08db6a5d22cacc348a9ef36fd9e9857d5b55642a
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65703731"
---
# <a name="signfile-task"></a>SignFile Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

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
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [görev temel sınıf](../msbuild/task-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `SignFile` belirtilen dosyaları imzalamak için görev `FilesToSign` koleksiyon öğesi tarafından belirtilen sertifika ile `Certificate` özelliği.  
  
```  
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
> Sertifika parmak izini sertifika SHA-1 karmasını ' dir. Daha fazla bilgi için [güvenilen kök CA sertifikasının SHA-1 karması elde](https://msdn.microsoft.com/dd641990-9a88-4228-a245-017797131a87).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `Exec` belirtilen dosyaları imzalamak için görev `FilesToSign` koleksiyon öğesi tarafından belirtilen sertifika ile `Certificate` özelliği. Derleme işlemi sırasında Windows Installer dosyaları imzalamak için bunu kullanabilirsiniz.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <ItemGroup>  
        <FileToSign Include="File.msi" />  
    </ItemGroup>  
    <PropertyGroup>  
        <Certificate>Cert.cer</Certificate>  
    </PropertyGroup>  
    <Target Name="Sign">  
        <Exec Command="signtool.exe sign /f CertFile /p Password "@(FileToSign)" "/>  
        <SignFile  
            CertificateThumbprint="$(CertificateThumbprint)"  
            SigningTarget="@(FileToSign)"   
            TargetFrameworkVersion="v4.0" />  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [Görevler](../msbuild/msbuild-tasks.md)
