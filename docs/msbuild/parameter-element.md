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
ms.openlocfilehash: 83f713382b0f767d966276807b1d10fac39c4bcd
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54982747"
---
# <a name="parameter-element"></a>Parameter öğesi
Tarafından oluşturulan bir görev için belirli bir parametre hakkında bilgi içeren bir `UsingTask` `TaskFactory`.  Öğe adı parametrenin adıdır.  Daha fazla bilgi için [UsingTask öğesi (MSBuild)](../msbuild/usingtask-element-msbuild.md).  

 \<Proje >  
 \<UsingTask >  
 \<ParameterGroup >  
 \<Parametresi >  

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
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)
