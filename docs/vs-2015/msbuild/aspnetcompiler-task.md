---
title: AspNetCompiler görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#AspNetCompiler
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, AspNetCompiler task
- AspNetCompiler task [MSBuild]
ms.assetid: f811c019-a67b-4d54-82e6-e29549496f6e
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3a82e80f0b23915c30dd491d3986f4a9c765503e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54756542"
---
# <a name="aspnetcompiler-task"></a>AspNetCompiler Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
`AspNetCompiler` Görev sarmalar aspnet_compiler.exe, önceden derlemek için bir yardımcı program [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] uygulamalar.  
  
## <a name="task-parameters"></a>Görev parametreleri  
 Parametreleri aşağıdaki tabloda açıklanmıştır `AspNetCompiler` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`AllowPartiallyTrustedCallers`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Bu parametre `true`, tanımlayıcı ad bütünleştirilmiş kod kısmen güvenilen arayanlara izin verir.|  
|`Clean`|İsteğe bağlı `Boolean` parametresi<br /><br /> Bu parametre `true`, uygulamanın temiz oluşturulacaktır. Önceden derlenmiş bileşenler yeniden derlenecek. Varsayılan değer `false` şeklindedir. Bu parametre için karşılık gelen **- c** aspnet_compiler.exe üzerinde geçin.|  
|`Debug`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Bu parametre `true`, hata ayıklama bilgileri (. PDB dosyası), derleme sırasında yayınlanır. Varsayılan değer `false` şeklindedir. Bu parametre için karşılık gelen **-d** aspnet_compiler.exe üzerinde geçin.|  
|`DelaySign`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Bu parametre `true`, derlemenin tam olarak oluştururken imzalı değil.|  
|`FixedNames`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Bu parametre `true`, derlenmiş bütünleştirilmiş sabit adlar verilir...|  
|`Force`|İsteğe bağlı `Boolean` parametresi<br /><br /> Bu parametre `true`, zaten varsa, görev hedef dizine üzerine yazar. Mevcut içerik kaybolur. Varsayılan değer `false` şeklindedir. Bu parametre için karşılık gelen **-f** aspnet_compiler.exe üzerinde geçin.|  
|`KeyContainer`|İsteğe bağlı `String` parametresi.<br /><br /> Tanımlayıcı ad anahtar kapsayıcısı belirtir.|  
|`KeyFile`|İsteğe bağlı `String` parametresi.<br /><br /> Tanımlayıcı ad anahtar dosyası fiziksel yolunu belirtir...|  
|`MetabasePath`|İsteğe bağlı `String` parametresi.<br /><br /> Uygulamanın tam IIS metatabanı yolu belirtir. Bu parametre ile birleştirilemez `VirtualPath` veya `PhysicalPath` parametreleri. Bu parametre için karşılık gelen **-m** aspnet_compiler.exe üzerinde geçin.|  
|`PhysicalPath`|İsteğe bağlı `String` parametresi.<br /><br /> Derlenecek uygulamanın fiziksel yolu belirtir. Bu parametre yoksa, IIS metabase uygulamayı bulmak için kullanılır. Bu parametre için karşılık gelen **-p** aspnet_compiler.exe üzerinde geçin.|  
|`TargetFrameworkMoniker`|İsteğe bağlı `String` parametresi.<br /><br /> Aspnet_compiler.exe hangi .NET Framework sürümü kullanılması gerektiğini belirten TargetFrameworkMoniker belirtir. Yalnızca .NET Framework adlar kabul eder.|  
|`TargetPath`|İsteğe bağlı `String` parametresi.<br /><br /> Uygulamanın derlenmiş olan fiziksel yolunu belirtir. Belirtilmezse, yerinde önceden derlenmiş uygulamasıdır.|  
|`Updateable`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Bu parametre `true`, önceden derlenmiş uygulama güncelleştirilebilir.  Varsayılan değer `false` şeklindedir. Bu parametre için karşılık gelen **-u** aspnet_compiler.exe üzerinde geçin.|  
|`VirtualPath`|İsteğe bağlı `String` parametresi.<br /><br /> Derlenecek uygulamanın sanal yolu. Varsa `PhysicalPath` belirtilen fiziksel yola uygulamayı bulmak için kullanılır. Aksi takdirde, IIS metabase kullanılır ve uygulamanın varsayılan sitenin olduğu varsayılır. Bu parametre için karşılık gelen **- v** aspnet_compiler.exe üzerinde geçin.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.ToolTaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.ToolTask> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [ToolTaskExtension temel sınıfı](../msbuild/tooltaskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneğinde `AspNetCompiler` derleneceği görev bir [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] uygulama.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="PrecompileWeb">  
        <AspNetCompiler  
            VirtualPath="/MyWebSite"  
            PhysicalPath="c:\inetpub\wwwroot\MyWebSite\"  
            TargetPath="c:\precompiledweb\MyWebSite\"  
            Force="true"  
            Debug="true"  
        />  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
