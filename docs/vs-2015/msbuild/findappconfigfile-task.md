---
title: FindAppConfigFile görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- FindAppConfigFile task [MSBuild]
- MSBuild, FindAppConfigFile task
ms.assetid: e292de3e-7482-4426-83ce-d921061808bf
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: fb9e1f3fbdc1a6f4d7c4e2c589f620f331a904ed
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59663196"
---
# <a name="findappconfigfile-task"></a>FindAppConfigFile Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Sağlanan listelerinde app.config dosyasına bulur  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `FindAppConfigFile` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`AppConfigFile`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Varsa listesinde bulunan eşleşen ilk öğeyi belirtir.|  
|`PrimaryList`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Arama için birincil listesini belirtir.|  
|`SecondaryList`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Arama için ikincil listesini belirtir.|  
|`TargetPath`|Gerekli `String` parametresi.<br /><br /> Meta veri olarak eklemek için bir değer belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
