---
title: Itemdefinitiongroup öğesi (MSBuild) | Microsoft Docs
ms.date: 03/13/2017
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#ItemDefinitionGroup
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- ItemDefinitionGroup Element [MSBuild]
- <ItemDefinitionGroup> Element [MSBuild]
ms.assetid: 4e9fb04b-5148-4ae5-a394-42861dd62371
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 89fba35aeef3b4e71494081dd1776c7a4248a05e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53919501"
---
# <a name="itemdefinitiongroup-element-msbuild"></a>Itemdefinitiongroup öğesi (MSBuild)
`ItemDefinitionGroup` Öğesi varsayılan olarak uygulanır, projedeki tüm öğeleri meta verileri değerler öğesi tanımları kümesini tanımlamak olanak tanır. Itemdefinitiongroup yerini gerek [CreateItem görevi](../msbuild/createitem-task.md) ve [CreateProperty görevi](../msbuild/createproperty-task.md). Daha fazla bilgi için [öğesi tanımları](../msbuild/item-definitions.md).  

 \<Proje >  
 \<Itemdefinitiongroup >  

## <a name="syntax"></a>Sözdizimi  

```xml  
<ItemDefinitionGroup Condition="'String A' == 'String B'">  
    <Item1>... </Item1>  
    <Item2>... </Item2>  
</ItemDefinitionGroup>  
```  

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  

### <a name="attributes"></a>Öznitelikler  

|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`Condition`|İsteğe bağlı öznitelik. Değerlendirilecek koşul. Daha fazla bilgi için [koşullar](../msbuild/msbuild-conditions.md).|  

### <a name="child-elements"></a>Alt öğeleri  

|Öğe|Açıklama|  
|-------------|-----------------|  
|[Öğesi](../msbuild/item-element-msbuild.md)|Yapı işlemi için girişler tanımlar. Sıfır veya daha fazla olabilir `Item` öğelerinde bir `ItemDefinitionGroup`.|  

### <a name="parent-elements"></a>Üst öğeler  

| Öğe | Açıklama |
| - | - |
| [Project](../msbuild/project-element-msbuild.md) | Gerekli kök öğesi bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje dosyası. |

## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği, iki meta veri öğeleri, m ve n, içinde bir Itemdefinitiongroup tanımlar. "M" meta veri öğesi "i" tarafından açıkça tanımlanmadığından Bu örnekte, "m" varsayılan meta veri "i" öğesine uygulanır. Ancak, varsayılan meta veri "n", "n" meta veri öğesi "i" tarafından zaten tanımlı olduğundan, "i" öğesine uygulanmaz.  

```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <ItemDefinitionGroup>  
        <i>  
            <m>m1</m>  
            <n>n1</n>  
        </i>        
    </ItemDefinitionGroup>  
    <ItemGroup>  
        <i Include="a">  
            <o>o1</o>  
            <n>n2</n>  
        </i>  
    </ItemGroup>  
    ...  
</Project>  
```  

## <a name="see-also"></a>Ayrıca bkz.  
 [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)   
 [Öğeler](../msbuild/msbuild-items.md)
