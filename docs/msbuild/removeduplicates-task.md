---
title: RemoveDuplicates görevi | Microsoft Docs
ms.date: 03/01/2018
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#RemoveDuplicates
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, RemoveDuplicates task
- RemoveDuplicates task [MSBuild]
ms.assetid: 481cbab6-73ff-488c-aba5-2c09f9eb1e04
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5d9e732d55858b713d73cbf1ba4f325f40560503
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54987381"
---
# <a name="removeduplicates-task"></a>RemoveDuplicates görevi
Yinelenen öğeleri belirtilen öğeyi koleksiyondan kaldırır.  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `RemoveDuplicates` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`Filtered`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Bir öğe koleksiyonu kaldırılan tüm yinelenen öğeler içeriyor. Yinelenen her öğenin ilk örneğini tutma girdi öğelerinin sırasını korunur.|  
|`Inputs`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametresi.<br /><br /> Yinelenen öğeleri kaldırmak için öğe koleksiyonu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu görev, büyük/küçük harfe duyarlıdır ve yinelemeleri belirlerken öğe meta verileri karşılaştırmaz.  
  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `RemoveDuplicates` yinelenen öğeleri kaldırmak için görev `MyItems` öğe koleksiyonu. Görev tamamlandığında, `FilteredItems` öğe koleksiyonu içeren bir öğe.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
        <MyItems Include="MyFile.cs"/>  
        <MyItems Include="MyFile.cs">  
            <Culture>fr</Culture>  
        </MyItems>  
        <MyItems Include="myfile.cs"/>  
    </ItemGroup>  
  
    <Target Name="RemoveDuplicateItems">  
        <RemoveDuplicates  
            Inputs="@(MyItems)">  
            <Output  
                TaskParameter="Filtered"  
                ItemName="FilteredItems"/>  
        </RemoveDuplicates>  
    </Target>  
</Project>  
```  

 Aşağıdaki örnek, gösterir `RemoveDuplicates` görev kendi girdi sırasını korur. Görev tamamlandığında, `FilteredItems` öğe koleksiyonu öğeleri içeren *MyFile2.cs*, *MyFile1.cs*, ve *MyFile3.cs* o sırada.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
        <MyItems Include="MyFile2.cs"/>  
        <MyItems Include="MyFile1.cs" />  
        <MyItems Include="MyFile3.cs" />  
        <MyItems Include="myfile1.cs"/>  
    </ItemGroup>  
  
    <Target Name="RemoveDuplicateItems">  
        <RemoveDuplicates  
            Inputs="@(MyItems)">  
            <Output  
                TaskParameter="Filtered"  
                ItemName="FilteredItems"/>  
        </RemoveDuplicates>  
    </Target>  
</Project>  
```  

## <a name="see-also"></a>Ayrıca bkz.  
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [MSBuild kavramları](../msbuild/msbuild-concepts.md)   
 [Görevler](../msbuild/msbuild-tasks.md)
