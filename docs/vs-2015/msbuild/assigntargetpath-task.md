---
title: AssignTargetPath görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
ms.assetid: 0e830e31-3bcf-4259-b2a8-a5df49b92d51
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: f7bf12e9f6c90ce544205370a8ed26440388b0a6
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59670062"
---
# <a name="assigntargetpath-task"></a>AssignTargetPath Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu görev listesini dosyaları ve ekler kabul `<TargetPath>` zaten belirtilmezse, öznitelikleri.  
  
## <a name="task-parameters"></a>Görev parametreleri  
 Parametreleri aşağıdaki tabloda açıklanmıştır `AssignTargetPath` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`RootFolder`|İsteğe bağlı `string` giriş parametresi.<br /><br /> Hedef bağlantıları içeren klasörün yolunu içerir.|  
|`Files`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` giriş parametresi.<br /><br /> Gelen dosya listesini içerir.|  
|`AssignedFiles`|İsteğe Bağlı<br /><br /> <xref:Microsoft.Build.Framework.ITaskItem> `[]` Çıkış parametresi.<br /><br /> Dosyaların sonuç listesini içerir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek yürütür `AssignTargetPath` bir proje yapılandırma görevi.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="MyProject">  
        <AssignTargetPath  
RootFolder="Resources"  
            Files="@(ResourceFiles)"  
            <Output TaskParameter="AssignedFiles"  
                ItemName="OutAssignedFiles"/>  
        </AssignTargetPath>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
