---
title: CreateProperty görevi | Microsoft Docs
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 71c36b19b0fd44d6668cb497dccafaf12843a492
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53884743"
---
# <a name="createproperty-task"></a>CreateProperty görevi
Özellikler, geçirilen değerlerle doldurur. Bu, bir özellik veya dize diğerine kopyalanması için değerler sağlar.  

## <a name="attributes"></a>Öznitelikler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `CreateProperty` görev.  


| Parametre | Açıklama |
|------------------| - |
| `Value` | İsteğe bağlı `String` çıkış parametresi.<br /><br /> Yeni özelliğe kopyalamak için bir değer belirtir. |
| `ValueSetByTask` | İsteğe bağlı `String` çıkış parametresi.<br /><br /> Aynı değeri içeren `Value` parametresi. Belirlediği çıktı özelliği kaçınmak istiyorsanız bu parametreyi kullanın [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] zaman bunu atlar kapsayan hedef çıkışları güncel olduğundan. |

## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).  

## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `CreateProperty` oluşturmak için görev `NewFile` özellik değerlerinin birleşimini kullanarak `SourceFilename` ve `SourceFileExtension` özelliği.  

```xml  
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

 Proje değerini çalıştırdıktan sonra `NewFile` özelliği *Module1.vb*.  

## <a name="see-also"></a>Ayrıca bkz.  
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [Görevler](../msbuild/msbuild-tasks.md)