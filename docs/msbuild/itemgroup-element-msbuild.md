---
title: ItemGroup öğesi (MSBuild) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#ItemGroup
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- ItemGroup element [MSBuild]
- <ItemGroup> element [MSBuild]
ms.assetid: aac894e3-a9f1-4bbc-a796-6ef07001f35b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f77da33dbc89a56284206599468455083c99ef55
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53850849"
---
# <a name="itemgroup-element-msbuild"></a>ItemGroup öğesi (MSBuild)
Kullanıcı tanımlı bir dizi içeren [öğesi](../msbuild/item-element-msbuild.md) öğeleri. Kullanılan her öğe bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] alt öğesi olarak proje belirtilen bir `ItemGroup` öğesi.  
  
 \<Proje >  
 \<ItemGroup >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<ItemGroup Condition="'String A' == 'String B'">  
    <Item1>... </Item1>  
    <Item2>... </Item2>  
</ItemGroup>  
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
|[Öğesi](../msbuild/item-element-msbuild.md)|Yapı işlemi için girişler tanımlar. Sıfır veya daha fazla olabilir `Item` öğelerinde bir `ItemGroup`.|  
  
### <a name="parent-elements"></a>Üst öğeler  
  
| Öğe | Açıklama |
| - | - |
| [Project](../msbuild/project-element-msbuild.md) | Gerekli kök öğesi bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje dosyası. |
| [Hedef](../msbuild/target-element-msbuild.md) | .NET Framework 3.5 ile başlayan `ItemGroup` öğe içindeki görünebilir bir `Target` öğesi. Daha fazla bilgi için [hedefleri](../msbuild/msbuild-targets.md). |
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği kullanıcı tarafından tanımlanan öğe koleksiyonlarını gösterir `Res` ve `CodeFiles` içinde bildirilen bir `ItemGroup` öğesi. Her bir öğe içinde `Res` içeren kullanıcı tanımlı bir alt öğe koleksiyonu [Itemmetadata](../msbuild/itemmetadata-element-msbuild.md) öğesi.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <ItemGroup>  
        <Res Include = "Strings.fr.resources" >  
            <Culture>fr</Culture>  
        </Res>  
        <Res Include = "Dialogs.fr.resources" >  
            <Culture>fr</Culture>  
        </Res>  
  
        <CodeFiles Include="**\*.cs" Exclude="**\generated\*.cs" />  
        <CodeFiles Include="..\..\Resources\Constants.cs" />  
    </ItemGroup>  
...  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)   
 [Öğeleri](../msbuild/msbuild-items.md)   
 [Yaygın MSBuild proje öğeleri](../msbuild/common-msbuild-project-items.md)