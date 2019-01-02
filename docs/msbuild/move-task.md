---
title: Taşıma görevi | Microsoft Docs
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 6e2f66ea8b3a2439e3fa5ce481f0af9ec09c8207
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53917520"
---
# <a name="move-task"></a>Taşıma görevi
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

 `Move` Görev istenen hedef dosyaları için gerekli klasörler oluşturur.

 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)
