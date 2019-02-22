---
title: WriteLinesToFile görevi | Microsoft Docs
ms.date: 09/20/2018
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#WriteLinesToFile
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- WriteLinesToFile task [MSBuild]
- MSBuild, WriteLinesToFile task
ms.assetid: 9c8862ac-8da5-4437-9430-ecc30421f1c9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8cfe294e94acce70f48b96265b3edc491b37e668
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56653885"
---
# <a name="writelinestofile-task"></a>WriteLinesToFile görevi
Belirtilen öğe yolları, belirtilen bir metin dosyasına yazar.

## <a name="task-parameters"></a>Görev parametreleri
 Parametreleri aşağıdaki tabloda açıklanmıştır `WriteLinestoFile` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`File`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Öğeleri yazmak için dosyayı belirtir.|
|`Lines`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametresi.<br /><br /> Dosyaya yazmak için öğeleri belirtir.|
|`Overwrite`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, görev dosyasındaki varolan içeriğin üzerine yazar.|
|`Encoding`|İsteğe bağlı `String` parametresi.<br /><br /> Örneğin, "Unicode" kodlama karakter seçer.  Ayrıca bkz: <xref:System.Text.Encoding>.|
|`WriteOnlyWhenDifferent`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, hedef dosya varsa, belirtilen görev ne yazardı karşı Karşılaştırılacak ilk okunacak. Aynı dosyaya yazılan değil, disk ve zaman damgası korunur.|

## <a name="remarks"></a>Açıklamalar
 Varsa `Overwrite` olduğu `true`, yeni bir dosya oluşturur, içeriği dosyaya yazın ve ardından dosyayı kapatır. Hedef dosya zaten varsa üzerine yazılır. Varsa `Overwrite` olduğu `false`, dosyaya içerik ekler, hedef dosya zaten yoksa, oluşturma.

 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="example"></a>Örnek
 Aşağıdaki örnekte `WriteLinesToFile` yazma yollarının öğeler için görev `MyItems` öğesi tarafından belirtilen dosya koleksiyonuna `MyTextFile` öğe koleksiyonu.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">

    <ItemGroup>
        <MyTextFile Include="Items.txt"/>
        <MyItems Include="*.cs"/>
    </ItemGroup>

    <Target Name="WriteToFile">
        <WriteLinesToFile
            File="@(MyTextFile)"
            Lines="@(MyItems)"
            Overwrite="true"
            Encoding="Unicode"/>
    </Target>

</Project>
```

Bu örnekte, bir özellik ile katıştırılmış yeni satırlardan birden fazla satır içeren bir metin dosyası yazmak için kullanırız. Bir girdi varsa `Lines` yeni satır karakterleri, katıştırılmış yeni satırlar çıktı dosyasına dahil edilir. Bu şekilde, çok satırlı özelliklerine başvurabilirsiniz.

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp2.1</TargetFramework>
  </PropertyGroup>

  <Target Name="WriteLaunchers" AfterTargets="CopyFilesToOutputDirectory">
      <PropertyGroup>
        <LauncherCmd>
@ECHO OFF
dotnet %~dp0$(AssemblyName).dll %*
        </LauncherCmd>
      </PropertyGroup>

      <WriteLinesToFile
        File="$(OutputPath)$(AssemblyName).cmd"
        Overwrite="true"
        Lines="$(LauncherCmd)" />
  </Target>
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
