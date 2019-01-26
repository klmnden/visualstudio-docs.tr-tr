---
title: Generatetrustınfo görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, GenerateTrustInfo task
- GenerateTrustInfo task [MSBuild]
ms.assetid: 3ca60816-4bb0-4fef-ae43-ca0bfb63def3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3a476027333b648d175dbe54c487dd2081aecae7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54978106"
---
# <a name="generatetrustinfo-task"></a>GenerateTrustInfo görevi
Uygulama güvenini taban bildirimini ve gelen oluşturur `TargetZone` ve `ExcludedPermissions` parametreleri.  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `GenerateTrustInfo` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`ApplicationDependencies`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametresi.<br /><br /> Bağımlı derlemelerini belirtir.|  
|`BaseManifest`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Uygulama güveni oluşturmak için temel bildirimini belirtir.|  
|`ExcludedPermissions`|İsteğe bağlı `String` parametresi.<br /><br /> Bölge varsayılan izni kümeden hariç tutulacak bir veya daha fazla izni noktalı virgülle ayrılmış kimlik değerleri belirtir.|  
|`TargetZone`|İsteğe bağlı `String` parametresi.<br /><br /> Makine İlkesi'nden elde edilen bir bölgeye varsayılan izin kümesi belirtir.|  
|`TrustInfoFile`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> çıkış parametresi.<br /><br /> Uygulama güvenlik güven bilgilerini içeren dosyayı belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)