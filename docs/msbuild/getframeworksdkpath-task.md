---
title: GetFrameworkSdkPath görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#GetFrameworkSdkPath
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- GetFrameworkSdkPath task [MSBuild]
- MSBuild, GetFrameworkSdkPath task
ms.assetid: 2ef82b98-02b6-40cf-a9b5-f0e882fb5064
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fb1ca2a4c77471f4b6767269e511d690c6c094a1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54947276"
---
# <a name="getframeworksdkpath-task"></a>GetFrameworkSdkPath görevi
Yolunu alır [!INCLUDE[winsdklong](../deployment/includes/winsdklong_md.md)].  
  
## <a name="task-parameters"></a>Görev parametreleri  
 Parametreleri aşağıdaki tabloda açıklanmıştır `GetFrameworkSdkPath` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`FrameworkSdkVersion20Path`|İsteğe bağlı `String` salt okunur çıkış parametresi.<br /><br /> Yol varsa, .NET SDK'sı sürüm 2.0, döndürür. Aksi halde döndürür `String.Empty`.|  
|`FrameworkSdkVersion35Path`|İsteğe bağlı `String` salt okunur çıkış parametresi.<br /><br /> Yol varsa, sürüm 3.5, .NET SDK döndürür. Aksi halde döndürür `String.Empty`.|  
|`FrameworkSdkVersion40Path`|İsteğe bağlı `String` salt okunur çıkış parametresi.<br /><br /> Yol varsa, .NET SDK'sı sürüm 4.0 döndürür. Aksi halde döndürür `String.Empty`.|  
|`Path`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Herhangi bir sürümü varsa, en son .NET SDK yolunu içerir. Aksi halde döndürür `String.Empty`.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `GetFrameworkSdkPath` yolunu depolamak için görev [!INCLUDE[winsdkshort](../debugger/debug-interface-access/includes/winsdkshort_md.md)] içinde `SdkPath` özelliği.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="GetPath">  
        <GetFrameworkSdkPath>  
            <Output  
                TaskParameter="Path"  
                PropertyName="SdkPath" />  
        </GetFrameworkSdkPath>  
        <Message Text="$(SdkPath)"/>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)