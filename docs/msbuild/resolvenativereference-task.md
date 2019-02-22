---
title: ResolveNativeReference görevi | Microsoft Docs
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0f18549fece2db8a4a758dee17f6b4b1283d97e4
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56617762"
---
# <a name="resolvenativereference-task"></a>ResolveNativeReference görevi
Yerel başvurular çözümleniyor. Implements <xref:Microsoft.Build.Tasks.ResolveNativeReference> sınıfı. Bu sınıf doğrudan sizin kodunuzdan kullanılmak üzere tasarlanmamıştır .NET Framework altyapısını destekler.

## <a name="task-parameters"></a>Görev parametreleri
 Parametreleri aşağıdaki tabloda açıklanmıştır `ResolveNativeReference` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`AdditionalSearchPaths`|Gerekli <xref:System.String?displayProperty=fullName>`[]` parametresi.<br /><br /> Alır veya arama yollarını derleme kimliklerini yerel başvurular çözmek için ayarlar.|
|`ContainedComComponents`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya yerel derleme COM bileşenlerini ayarlar.|
|`ContainedLooseEtcFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya ayarlar gevşek *vb.* dosyaları yerel bir bildirim listelenir.|
|`ContainedLooseTlbFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya ayarlar gevşek *.tlb* yerel derleme dosyaları.|
|`ContainedPrerequisiteAssemblies`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya ayarlar bildirimde kullanılabilmesi için önce mevcut olmalıdır derlemeler.|
|`ContainedTypeLibraries`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya yerel derleme tür kitaplıklarının ayarlar.|
|`ContainingReferenceFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alır veya ayarlar başvuru dosyaları.|
|`NativeReferences`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Alır veya ayarlar Win32 yerel bütünleştirilmiş kod başvuruları.|

## <a name="remarks"></a>Açıklamalar
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)