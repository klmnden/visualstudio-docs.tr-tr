---
title: Parametre öğesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Parameter element [MSBuild]
- <Parameter> element [MSBuild]
ms.assetid: b273afff-b500-4e97-8cfd-31f39fa64a51
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a815d2ef623a35030469fa631cae65653c2fe2d1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68185222"
---
# <a name="parameter-element"></a>Parameter Öğesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tarafından oluşturulan bir görev için belirli bir parametre hakkında bilgi içeren bir `UsingTask``TaskFactory`.  Öğe adı parametrenin adıdır.  Daha fazla bilgiler için bkz. [UsingTask öğesi (MSBuild)](../msbuild/usingtask-element-msbuild.md).  
  
 \<Proje >  
 \<UsingTask >  
 \<ParameterGroup >  
 \<Parametresi >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<ParameterGroup ParameterType="SystemType"  
    Output="true/false"  
    Required="true/false" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`ParameterType`|İsteğe bağlı öznitelik.<br /><br /> Örneğin, "System.String" parametresinin .NET türü.|  
|`Output`|İsteğe bağlı Boolean özniteliği.<br /><br /> Varsa `true`, bu parametre görev için bir çıktı parametresidir. Varsayılan değer olan `false`.|  
|`Required`|İsteğe bağlı Boolean özniteliği.<br /><br /> Varsa `true`, bu parametre bir görev için gerekli bir parametredir. Varsayılan değer olan `false`.|  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[ParameterGroup](../msbuild/parametergroup-element.md)|İsteğe bağlı bir liste tarafından oluşturulan bir görev üzerinde mevcut parametreler içeren bir `UsingTask``TaskFactory`.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek nasıl kullanılacağını gösterir `Parameter` öğesi.  
  
```  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [Proje Dosyası Şema Başvurusu](../msbuild/msbuild-project-file-schema-reference.md)
