---
title: CreateProperty görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#CreateProperty
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- CreateProperty task [MSBuild]
- MSBuild, CreateProperty task
ms.assetid: fbc31a88-62d4-43d2-b739-68ef3fac38f5
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: ea16950e47760e89204503413fd98811e781d059
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68184054"
---
# <a name="createproperty-task"></a>CreateProperty Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Özellikler, geçirilen değerlerle doldurur. Bu, bir özellik veya dize diğerine kopyalanması için değerler sağlar.  
  
## <a name="attributes"></a>Öznitelikler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `CreateProperty` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`Value`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Yeni özelliğe kopyalamak için bir değer belirtir.|  
|`ValueSetByTask`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Aynı değeri içeren `Value` parametresi. Belirlediği çıktı özelliği kaçınmak istiyorsanız bu parametreyi kullanın [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] zaman bunu atlar kapsayan hedef çıkışları güncel olduğundan.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `CreateProperty` oluşturmak için görev `NewFile` özellik değerlerinin birleşimini kullanarak `SourceFilename` ve `SourceFileExtension` özelliği.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <PropertyGroup>  
        <SourceFilename>Module1</SourceFilename>  
        <SourceFileExtension>vb</SourceFileExtension>  
    </PropertyGroup>  
  
    <Target Name="CreateProperties">  
  
        <CreateProperty  
            Value="$(SourceFilename).$(SourceFileExtension)">  
            <Output  
                TaskParameter="Value"  
                PropertyName="NewFile" />  
        </CreateProperty>  
  
    </Target>  
  
</Project>  
```  
  
 Proje değerini çalıştırdıktan sonra `NewFile` özelliği `Module1.vb`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [Görevler](../msbuild/msbuild-tasks.md)
