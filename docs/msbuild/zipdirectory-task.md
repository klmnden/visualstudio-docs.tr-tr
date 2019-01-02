---
title: ZipDirectory görev | Microsoft Docs
ms.date: 11/04/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#ZipDirectory
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- ZipDirectory task [MSBuild]
- MSBuild, ZipDirectory task
ms.assetid: 916bb2e3-3017-4828-ae27-c0b5c99bbb48
caps.latest.revision: 16
author: Mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 320fd3a62c3283b0c442f0f7bbc3df5512eb7bcc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53930966"
---
# <a name="zipdirectory-task"></a>ZipDirectory görevi
Oluşturur bir *.zip* bir dizinin içeriklerini arşivden.

>[!NOTE]
>`ZipDirectory` Görevdir MSBuild 15,8 ve yalnızca üzerinde kullanılabilir.
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `ZipDirectory` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`DestinationFile`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi<br /><br /> Tam yolu *.zip* oluşturmak için dosya.|
|`Overwrite`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, hedef dosyanın üzerine varsa atlar. Varsayılan olarak `false`.|
|`SourceDirectory`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Oluşturulacak dizinin belirtir bir *.zip* gelen arşivleyin.|
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, oluşturur bir *.zip* arşivden bir projeyi oluşturduktan sonra çıktı dizini.
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">

    <Target Name="ZipOutputPath" AfterTargets="Build">
        <ZipDirectory
            SourceDirectory="$(OutputPath)"
            DestinationFile="$(MSBuildProjectDirectory)\output.zip" />
    </Target>

</Project>
```
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)
