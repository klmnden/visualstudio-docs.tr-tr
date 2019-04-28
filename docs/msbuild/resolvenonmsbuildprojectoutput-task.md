---
title: ResolveNonMSBuildProjectOutput görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, ResolveNonMSBuildProjectOutput task
- ResolveNonMSBuildProjectOutput task [MSBuild]
ms.assetid: a0b8fcec-8c8d-4867-85ac-5304c5108e5e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7060141f81054bf5daa27cdd09a07639be6e0ae8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62996712"
---
# <a name="resolvenonmsbuildprojectoutput-task"></a>ResolveNonMSBuildProjectOutput görevi
MSBuild dışındaki proje başvuruları için çıkış dosyalarının belirler.

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır `ResolveNonMSBuildProjectOutput` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`PreresolvedProjectOutputs`|İsteğe bağlı `String` parametresi.<br /><br /> Proje çıkışları içeren bir XML dizesi çözümlenen belirtir.|
|`ProjectReferences`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Proje başvurularını belirtir.|
|`ResolvedOutputPaths`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Çözümlenen başvuru yollarının listesini içerir (ve özgün proje başvuru öznitelikleri korur).|
|`UnresolvedProjectReferences`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Çıkışlar preresolved listesini kullanarak çözümlenemedi proje başvuru öğelerinin listesini içerir.<br /><br /> Visual Studio MSBuild olmayan projeleri yalnızca preresolves çünkü bu, bu listedeki proje başvuruları MSBuild biçiminde olduğunu anlamına gelir.|

## <a name="remarks"></a>Açıklamalar
 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)