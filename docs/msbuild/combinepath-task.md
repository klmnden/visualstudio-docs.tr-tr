---
title: CombinePath görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, CombinePath task
- CombinePath task [MSBuild]
ms.assetid: c20edbf4-3d4f-4f66-b1d5-753a0d858ed8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6b73ddd4715d3abd29f87d7ef38a269d821733ba
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56610296"
---
# <a name="combinepath-task"></a>CombinePath görevi
Belirtilen yolu tek yola birleştirir.

## <a name="task-parameters"></a>Görev parametreleri
 Parametreleri aşağıdaki tabloda açıklanmıştır [CombinePath görevi](../msbuild/combinepath-task.md).

|Parametre|Açıklama|
|---------------|-----------------|
|`BasePath`|Gerekli `String` parametresi.<br /><br /> Diğer yollar ile birleştirmek için temel yol. Bir göreli yol, mutlak yolu ya da boş olabilir.|
|`Paths`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Birleşik yolun oluşturmak üzere BasePath ile birleştirmek için tek yol listesi. Göreli veya mutlak yol olabilir.|
|`CombinedPaths`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Bu görev tarafından oluşturulan birleşik yolu.|

## <a name="remarks"></a>Açıklamalar
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)