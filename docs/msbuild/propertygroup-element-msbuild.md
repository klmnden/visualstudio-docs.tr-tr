---
title: PropertyGroup öğesi (MSBuild) | Microsoft Docs
ms.date: 03/13/2017
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#PropertyGroup
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- <PropertyGroup> element [MSBuild]
- PropertyGroup element [MSBuild]
ms.assetid: ff1e6c68-b9a1-4263-a1ce-dc3b829a64d4
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 607c5f2c3cda64e7407203b0c45287a58342b807
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56622923"
---
# <a name="propertygroup-element-msbuild"></a>PropertyGroup öğesi (MSBuild)
Kullanıcı tanımlı bir dizi içeren [özelliği](../msbuild/property-element-msbuild.md) öğeleri. Her `Property` kullanılan öğesi bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje alt öğesi olmalıdır bir `PropertyGroup` öğesi.

 \<Proje > \<PropertyGroup >

## <a name="syntax"></a>Sözdizimi

```xml
<PropertyGroup Condition="'String A' == 'String B'">
    <Property1>...</Property1>
    <Property2>...</Property2>
</PropertyGroup>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|Koşul|İsteğe bağlı öznitelik.<br /><br /> Değerlendirilecek koşul. Daha fazla bilgi için [koşullar](../msbuild/msbuild-conditions.md).|

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|[Özelliği](../msbuild/property-element-msbuild.md)|İsteğe bağlı öğe.<br /><br /> Özellik değerini içeren bir kullanıcı tanımlı özellik adı. Sıfır veya daha fazla olabilir *özelliği* öğelerinde bir `PropertyGroup` öğesi.|

### <a name="parent-elements"></a>Üst öğeler

| Öğe | Açıklama |
| - | - |
| [Project](../msbuild/project-element-msbuild.md) | Gerekli kök öğesi bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje dosyası. |

## <a name="example"></a>Örnek
 Aşağıdaki kod örneği, bir koşulu temel alarak özelliklerin nasıl ayarlanacağını gösterir. Bu örnekte, değerini `CompileConfig` özelliği `DEBUG`, `Optimization`, `Obfuscate`, ve `OutputPath` içinde özelliklerini `PropertyGroup` öğesi ayarlanır.

```xml
<PropertyGroup Condition="'$(CompileConfig)' == 'DEBUG'" >
    <Optimization>false</Optimization>
    <Obfuscate>false</Obfuscate>
    <OutputPath>$(OutputPath)\debug</OutputPath>
</PropertyGroup>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)
- [MSBuild özellikleri](../msbuild/msbuild-properties.md)
