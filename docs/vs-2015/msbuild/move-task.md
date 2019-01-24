---
title: Taşıma görevi | Microsoft Docs
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
- MSBuild, Move task
- Move task [MSBuild]
ms.assetid: d1405347-1309-4f18-b565-905408093d59
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2919d139e48f6e08845dc3990b0df5a8591283c0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54791387"
---
# <a name="move-task"></a>Taşıma Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Dosyalarını yeni konuma taşır.  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `Move` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`DestinationFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Kaynak dosyaların dosyaların listesini belirtir. Bu liste belirtilen listesine bire bir eşleme olması beklenir `SourceFiles` parametresi. Diğer bir deyişle, belirtilen ilk dosya `SourceFiles` içinde belirtilen ilk konuma taşınır `DestinationFiles`ve böyle devam eder.|  
|`DestinationFolder`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Dosyaları taşımak istediğiniz dizini belirtir.|  
|`MovedFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Başarıyla taşındı öğeleri içerir.|  
|`OverwriteReadOnlyFiles`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, salt okunur dosyalar işaretlenmiş olsa bile dosyaların üzerine yazar.|  
|`SourceFiles`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Dosyaların belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Her iki `DestinationFolder` parametresi veya `DestinationFiles` parametresi belirtilen, ancak ikisi birden değil olmalıdır. Eğer her ikisi de belirtilirse görev başarısız olur ve bir hata günlüğe kaydedilir.  
  
 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
