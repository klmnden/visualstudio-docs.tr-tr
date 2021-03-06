---
title: TaskBody öğesi (MSBuild) | Microsoft Docs
ms.date: 03/13/2017
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- TaskBody element [MSBuild]
- <TaskBody> element [MSBuild]
ms.assetid: 49d8741b-f1ea-4470-94fd-a1ac27341a6a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8f788df1dd3cad2baddd6d2966b04195af01fe7d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62938967"
---
# <a name="taskbody-element-msbuild"></a>TaskBody öğesi (MSBuild)
Geçirilen verileri içeren bir `UsingTask` `TaskFactory`. Daha fazla bilgi için [UsingTask öğesi (MSBuild)](../msbuild/usingtask-element-msbuild.md).

 \<Proje > \<UsingTask > \<TaskBody >

## <a name="syntax"></a>Sözdizimi

```xml
<TaskBody Evaluate="true/false" />
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|`Evaluate`|İsteğe bağlı Boolean özniteliği.<br /><br /> Varsa `true`, MSBuild herhangi bir iç öğe değerlendirir ve bilgileri geçirmeden önce öğeleri ve özellikleri genişletir `TaskFactory` görev oluşturulduğunda.|

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|Veri|Arasına metin `TaskBody` etiketleri için verbatim gönderilir `TaskFactory`.|

### <a name="parent-elements"></a>Üst öğeler

| Öğe | Açıklama |
| - | - |
| [UsingTask](../msbuild/usingtask-element-msbuild.md) | Görevleri kaydetmek için bir yol sağlar [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]. Sıfır veya daha fazla olabilir `UsingTask` proje öğeleri. |

## <a name="example"></a>Örnek
 Aşağıdaki örnek nasıl kullanılacağını gösterir `TaskBody` öğesi ile bir `Evaluate` özniteliği.

```xml
<UsingTask TaskName="MyTask" AssemblyName="My.Assembly" TaskFactory="MyTaskFactory">
       <ParameterGroup>
              <Parameter1 ParameterType="System.String" Required="False" Output="False"/>
              <Parameter2 ParameterType="System.Int" Required="True" Output="False"/>
              ...
</ParameterGroup>
       <TaskBody Evaluate="true">
      ... Task factory-specific data ...
       </TaskBody>
</UsingTask>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)
