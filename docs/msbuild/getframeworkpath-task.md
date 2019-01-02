---
title: GetFrameworkPath görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#GetFrameworkPath
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- GetFrameworkPath task [MSBuild]
- MSBuild, GetFrameworkPath task
ms.assetid: 5b7bcdd7-d4a0-442d-af29-8aadb3b10598
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2eeee3865a9b2a607df48ca6d9ade1990401f759
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53944872"
---
# <a name="getframeworkpath-task"></a>GetFrameworkPath görevi
Yolunu alır [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] derlemeler.  
  
## <a name="task-parameters"></a>Görev parametreleri  
 Parametreleri aşağıdaki tabloda açıklanmıştır `GetFrameworkPath` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`FrameworkVersion11Path`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Framework sürüm 1.1 derlemeleri için yolu varsa içeriyor. Aksi halde döndürür `null`.|  
|`FrameworkVersion20Path`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Framework sürüm 2.0 derlemeleri için yolu varsa içeriyor. Aksi halde döndürür `null`.|  
|`FrameworkVersion30Path`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Framework sürüm 3.0 derlemeleri için yolu varsa içeriyor. Aksi halde döndürür `null`.|  
|`FrameworkVersion35Path`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Framework sürüm 3.5 derlemeleri için yolu varsa içeriyor. Aksi halde döndürür `null`.|  
|`FrameworkVersion40Path`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Framework sürüm 4.0 derlemeleri için yolu varsa içeriyor. Aksi halde döndürür `null`.|  
|`Path`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Varsa, son framework derlemeleri için yolu içerir. Aksi halde döndürür `null`.|  
  
## <a name="remarks"></a>Açıklamalar  
 Çeşitli sürümlerini [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] olan yüklüyse, bu görev sürümü döndürür [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] üzerinde çalışmak üzere tasarlanmıştır.  
  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `GetFrameworkPath` yolunu depolamak için görev [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] içinde `FrameworkPath` özelliği.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="GetPath">  
        <GetFrameworkPath>  
            <Output  
                TaskParameter="Path"  
                PropertyName="FrameworkPath" />  
        </GetFrameworkPath>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)