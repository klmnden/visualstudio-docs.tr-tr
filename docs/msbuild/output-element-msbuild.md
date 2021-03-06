---
title: Çıktı öğesi (MSBuild) | Microsoft Docs
ms.date: 03/13/2017
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Output
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- <Output> Element [MSBuild]
- Output Element [MSBuild]
ms.assetid: 34bc7cd1-efd3-4b57-b691-4584eeb6a0e9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cb8f7a02183fe34dcd882e23ee7bf8b90f9a2cc6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62963931"
---
# <a name="output-element-msbuild"></a>Çıktı öğesi (MSBuild)
Öğeleri ve özellikleri depoları Görev çıkış değerleri.

 \<Proje > \<hedef > \<görev > \<çıkış >

## <a name="syntax"></a>Sözdizimi

```xml
<Output TaskParameter="Parameter"
    PropertyName="PropertyName"
    Condition = "'String A' == 'String B'" />
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|`TaskParameter`|Gerekli öznitelik.<br /><br /> Görev adı çıkış parametresi.|
|`PropertyName`|Ya da `PropertyName` veya `ItemName` özniteliği gereklidir.<br /><br /> Parametre değeri çıkış görev alan özelliği. Projenizi ardından $ özelliğiyle başvuruda bulunabilir (\<PropertyName >) söz dizimi. Bu özellik adı ya da yeni bir özellik adı veya projede zaten tanımlı bir ad olabilir.<br /><br /> Bu öznitelik, kullanılamaz `ItemName` da kullanılıyor.|
|`ItemName`|Ya da `PropertyName` veya `ItemName` özniteliği gereklidir.<br /><br /> Parametre değeri çıkış görev alan öğesi. Projenizi ardından öğeyle başvurabilirsiniz @(\<ItemName >) söz dizimi. Öğe adı ya da yeni bir öğe adı veya projede zaten tanımlı bir ad olabilir. Öğe adı, var olan bir öğe olduğunda, çıkış parametresi değerleri varolan öğesine eklenir. <br /><br /> Bu öznitelik, kullanılamaz `PropertyName` da kullanılıyor.|
|`Condition`|İsteğe bağlı öznitelik.<br /><br /> Değerlendirilecek koşul. Daha fazla bilgi için [koşullar](../msbuild/msbuild-conditions.md).|

### <a name="child-elements"></a>Alt öğeleri
 Yok.

### <a name="parent-elements"></a>Üst öğeler

| Öğe | Açıklama |
| - | - |
| [Görev](../msbuild/task-element-msbuild.md) | Oluşturur ve yürütür örneği bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] görev. |

## <a name="example"></a>Örnek
 Aşağıdaki örnekte gösterildiği kod `Csc` görev içinde yürütülen bir `Target` öğesi. Bu örnekte kapsamı dışında öğeleri ve görev parametrelerine geçirilen özellikleri bildirilir. Çıkış parametresi değerinden `OutputAssembly` depolanan `FinalAssemblyName` öğesi ve çıkış parametresi değerinden `BuildSucceeded` depolanan `BuildWorked` özelliği. Daha fazla bilgi için [görevleri](../msbuild/msbuild-tasks.md).

```xml
<Target Name="Compile" DependsOnTargets="Resources">
    <Csc  Sources="@(CSFile)"
            TargetType="library"
            Resources="@(CompiledResources)"
            EmitDebugInformation="$(includeDebugInformation)"
            References="@(Reference)"
            DebugType="$(debuggingType)"
            OutputAssembly="$(builtdir)\$(MSBuildProjectName).dll" >
        <Output TaskParameter="OutputAssembly"
                  ItemName="FinalAssemblyName" />
        <Output TaskParameter="BuildSucceeded"
                  PropertyName="BuildWorked" />
    </Csc>
</Target>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)
- [Görevler](../msbuild/msbuild-tasks.md)
