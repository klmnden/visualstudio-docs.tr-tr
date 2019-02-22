---
title: FindUnderPath görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#FindUnderPath
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, FindUnderPath task
- FindUnderPath task [MSBuild]
ms.assetid: 3c6d58b0-36e8-47aa-bfca-b73dd2045d91
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9c22e2465b79faa68f8789cefeeb181c2e15b73b
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56602198"
---
# <a name="findunderpath-task"></a>FindUnderPath görevi
Belirtilen öğe koleksiyonunda öğelerin veya belirtilen klasörde aşağıdaki yolları olduğunu belirler.

## <a name="parameters"></a>Parametreler
Parametreleri aşağıdaki tabloda açıklanmıştır `FindUnderPath` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`Files`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametresi.<br /><br /> Yolları tarafından belirtilen yol ile karşılaştırılabilir dosyaları belirtir `Path` parametresi.|
|`InPath`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Belirtilen yolun altında bulunan öğeleri içerir.|
|`OutOfPath`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Belirtilen yolun altındaki bulunmayan öğeleri içerir.|
|`Path`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Referans olarak kullanılacak bir klasör yolu belirtir.|
|`UpdateToAbsolutePaths`|İsteğe bağlı `Boolean` parametresi.<br /><br /> TRUE ise çıkış öğelerinin yolları mutlak yollar olacak şekilde güncelleştirilir.|

## <a name="remarks"></a>Açıklamalar
Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="example"></a>Örnek
Aşağıdaki örnekte `FindUnderPath` dosyaları içinde yer alan olmadığını belirlemek için görev `MyFiles` öğesi tarafından belirtilen yolun altındaki mevcut yolları sahip `SearchPath` özelliği. Görevi tamamlandıktan sonra `FilesNotFoundInPath` öğeyi içeren *Dosya1.ref* dosyasını ve `FilesFoundInPath` öğeyi içeren *File2.txt* dosya.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
    <ItemGroup>
        <MyFiles Include="C:\File1.txt" />
        <MyFiles Include="C:\Projects\MyProject\File2.txt" />
    </ItemGroup>

    <PropertyGroup>
        <SearchPath>C:\Projects\MyProject</SearchPath>
    </PropertyGroup>

    <Target Name="FindFiles">
        <FindUnderPath
            Files="@(MyFiles)"
            Path="$(SearchPath)">
            <Output
                TaskParameter="InPath"
                ItemName="FilesFoundInPath" />
            <Output
                TaskParameter="OutOfPath"
                ItemName="FilesNotFoundInPath" />
        </FindUnderPath>
    </Target>

</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Görevler](../msbuild/msbuild-tasks.md)
- [MSBuild kavramları](../msbuild/msbuild-concepts.md)
