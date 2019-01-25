---
title: ResolveNativeReference görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#ResolveNativeReference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, ResolveNativeReference task
- ResolveNativeReference task [MSBuild]
ms.assetid: 56acd101-de77-4eec-92c6-f5c6d2187579
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 31de2c146accd71ae1606be62ab06fa368e7fb89
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54758554"
---
# <a name="resolvenativereference-task"></a>ResolveNativeReference Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Yerel başvurular çözümleniyor. Implements <xref:Microsoft.Build.Tasks.ResolveNativeReference> sınıfı. Bu sınıf doğrudan sizin kodunuzdan kullanılmak üzere tasarlanmamıştır .NET Framework altyapısını destekler.  
  
## <a name="task-parameters"></a>Görev parametreleri  
 Parametreleri aşağıdaki tabloda açıklanmıştır `ResolveNativeReference` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`AdditionalSearchPaths`|[String] gerekli (<!-- TODO: review code entity reference <xref:assetId:///String?qualifyHint=False&amp;autoUpgrade=True>  -->)`[]` parametresi.<br /><br /> Alır veya arama yollarını derleme kimliklerini yerel başvurular çözmek için ayarlar.|  
|`ContainedComComponents`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya yerel derleme COM bileşenlerini ayarlar.|  
|`ContainedLooseEtcFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya ayarlar yerel bildiriminde listelenen gevşek vb. dosyalar.|  
|`ContainedLooseTlbFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya ayarlar yerel derleme gevşek .tlb dosyaları.|  
|`ContainedPrerequisiteAssemblies`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya ayarlar bildirimde kullanılabilmesi için önce mevcut olmalıdır derlemeler.|  
|`ContainedTypeLibraries`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya yerel derleme tür kitaplıklarının ayarlar.|  
|`ContainingReferenceFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya ayarlar başvuru dosyaları.|  
|`NativeReferences`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Alır veya ayarlar Win32 yerel bütünleştirilmiş kod başvuruları.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
