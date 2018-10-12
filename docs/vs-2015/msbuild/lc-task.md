---
title: LC görevi | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#LC
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, LC task
- LC task [MSBuild]
ms.assetid: d5a53472-6f2a-42b8-a6db-593ca99c9790
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e7331e5ad14c52b6056c7e636d2d48e7f86a9b5e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49305805"
---
# <a name="lc-task"></a>LC Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Bir .licx dosyasından .license dosyası oluşturur, LC.exe sarmalar. LC.exe hakkında daha fazla bilgi için bkz. [Lc.exe (lisans derleyici)](http://msdn.microsoft.com/library/2de803b8-495e-4982-b209-19a72aba0460).  
  
## <a name="parameters"></a>Parametreler  
 Aşağıdaki tablo için parametrelerinin açıklar `LC` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`LicenseTarget`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> .Licenses dosyaları oluşturulan yürütülebilir dosyayı belirtir.|  
|`NoLogo`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Microsoft başlangıç başlığı görüntüsünü bastırır.|  
|`OutputDirectory`|İsteğe bağlı `String` parametresi.<br /><br /> Çıkış .licenses dosyalarının yerleştirileceği dizini belirtir.|  
|`OutputLicense`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> çıkış parametresi.<br /><br /> .Licenses dosyasının adını belirtir. Bir ad belirtmezseniz, .licx dosyası adı kullanılır ve .licenses dosyasını .licx dosyasını içeren dizine yerleştirilir.|  
|`ReferencedAssemblies`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametresi.<br /><br /> .License dosyası oluşturulurken yüklemek için başvurulan bileşenlerini belirtir.|  
|`SdkToolsPath`|İsteğe bağlı `String` parametresi.<br /><br /> Resgen.exe gibi SDK Araçları yolunu belirtir.|  
|`Sources`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> .licenses dosyasına eklenecek lisanslı bileşenleri içeren öğeleri belirtir. Daha fazla bilgi için belgelerine bakın `/complist` anahtarının [Lc.exe (lisans derleyici)](http://msdn.microsoft.com/library/2de803b8-495e-4982-b209-19a72aba0460).|  
  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.ToolTaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.ToolTask> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [ToolTaskExtension temel sınıfı](../msbuild/tooltaskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `LC` lisansları derlemek için bir görev.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
<!-- Item declarations, etc -->  
  
    <Target Name="CompileLicenses">  
        <LC  
            Sources="@(LicxFile)"  
            LicenseTarget="$(TargetFileName)"  
            OutputDirectory="$(IntermediateOutputPath)"  
            OutputLicenses="$(IntermediateOutputPath)$(TargetFileName).licenses"  
            ReferencedAssemblies="@(ReferencePath);@(ReferenceDependencyPaths)">  
  
            <Output  
                TaskParameter="OutputLicenses"  
                ItemName="CompiledLicenseFile"/>  
        </LC>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)



