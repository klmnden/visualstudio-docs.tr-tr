---
title: Parametre öğesi | Microsoft Docs
ms.date: 03/13/2017
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
- xml
helpviewer_keywords:
- Parameter element [MSBuild]
- <Parameter> element [MSBuild]
ms.assetid: b273afff-b500-4e97-8cfd-31f39fa64a51
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fc410948f3869de5ca3059cba703e5381f93d7eb
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56603590"
---
# <a name="parameter-element"></a>Parameter öğesi
Tarafından oluşturulan bir görev için belirli bir parametre hakkında bilgi içeren bir `UsingTask` `TaskFactory`.  Öğe adı parametrenin adıdır.  Daha fazla bilgi için [UsingTask öğesi (MSBuild)](../msbuild/usingtask-element-msbuild.md).

 \<Proje > \<UsingTask > \<ParameterGroup > \<parametresi >

## <a name="syntax"></a>Sözdizimi

```xml
<ParameterGroup ParameterType="SystemType"
    Output="true/false"
    Required="true/false" />
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|`ParameterType`|İsteğe bağlı öznitelik.<br /><br /> Parametresi, örneğin, .NET türü `System.String`.|
|`Output`|İsteğe bağlı Boolean özniteliği.<br /><br /> Varsa `true`, bu parametre görev için bir çıktı parametresidir. Varsayılan değer olan `false`.|
|`Required`|İsteğe bağlı Boolean özniteliği.<br /><br /> Varsa `true`, bu parametre bir görev için gerekli bir parametredir. Varsayılan değer olan `false`.|

### <a name="child-elements"></a>Alt öğeleri
 Yok.

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[ParameterGroup](../msbuild/parametergroup-element.md)|İsteğe bağlı bir liste tarafından oluşturulan bir görev üzerinde mevcut parametreler içeren bir `UsingTask` `TaskFactory`.|

## <a name="example"></a>Örnek
 Aşağıdaki örnek nasıl kullanılacağını gösterir `Parameter` öğesi.

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
