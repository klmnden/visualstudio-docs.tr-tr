---
title: TaskBody öğesi (MSBuild) | Microsoft Docs
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
- TaskBody element [MSBuild]
- <TaskBody> element [MSBuild]
ms.assetid: 49d8741b-f1ea-4470-94fd-a1ac27341a6a
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 6b02616b54c0697f824d53eab978142679e8a358
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752399"
---
# <a name="taskbody-element-msbuild"></a>TaskBody Öğesi (MSBuild)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Geçirilen verileri içeren bir `UsingTask``TaskFactory`. Daha fazla bilgi için [UsingTask öğesi (MSBuild)](../msbuild/usingtask-element-msbuild.md).  
  
 \<Proje >  
 \<UsingTask >  
 \<TaskBody >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<TaskBody Evaluate="true/false" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`Evaluate`|İsteğe bağlı Boolean özniteliği.<br /><br /> Varsa `true`, MSBuild herhangi bir iç öğe değerlendirir ve bilgileri geçirmeden önce öğeleri ve özellikleri genişletir `TaskFactory` görev oluşturulduğunda.|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|Veri|Arasına metin `TaskBody` etiketleri için verbatim gönderilir `TaskFactory`.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[UsingTask](../msbuild/usingtask-element-msbuild.md)|Görevleri kaydetmek için bir yol sağlar [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)]. Sıfır veya daha fazla olabilir `UsingTask` proje öğeleri.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek nasıl kullanılacağını gösterir `TaskBody` öğesi ile bir `Evaluate` özniteliği.  
  
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
