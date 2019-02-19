---
title: GetFrameworkSdkPath görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
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
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 16a522044188db854b89f87ccba0ef3393ab70fc
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54803942"
---
# <a name="getframeworksdkpath-task"></a>GetFrameworkSdkPath Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Yolunu alır [!INCLUDE[winsdklong](../includes/winsdklong-md.md)].  
  
## <a name="task-parameters"></a>Görev parametreleri  
 Parametreleri aşağıdaki tabloda açıklanmıştır `GetFrameworkSdkPath` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`FrameworkSdkVersion20Path`|İsteğe bağlı `String` salt okunur çıkış parametresi.<br /><br /> Yol varsa, .NET SDK'sı sürüm 2.0, döndürür. Aksi halde döndürür `String.Empty`.|  
|`FrameworkSdkVersion35Path`|İsteğe bağlı `String` salt okunur çıkış parametresi.<br /><br /> Yol varsa, sürüm 3.5, .NET SDK döndürür. Aksi halde döndürür `String.Empty`.|  
|`FrameworkSdkVersion40Path`|İsteğe bağlı `String` salt okunur çıkış parametresi.<br /><br /> Yol varsa, .NET SDK'sı sürüm 4.0 döndürür. Aksi halde döndürür `String.Empty`.|  
|`Path`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Herhangi bir sürümü varsa, en son .NET SDK yolunu içerir. Aksi halde döndürür `String.Empty`.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `GetFrameworkSdkPath` yolunu depolamak için görev [!INCLUDE[winsdkshort](../includes/winsdkshort-md.md)] içinde `SdkPath` özelliği.  
  
```  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
