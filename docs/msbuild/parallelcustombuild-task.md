---
title: ParallelCustomBuild görev | Microsoft Docs
ms.date: 03/10/2019
ms.topic: reference
f1_keywords:
- vc.task.parallelcustombuild
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), ParallelCustomBuild task
- ParallelCustomBuild task (MSBuild (Visual C++))
author: mikeblome
ms.author: mblome
ms.workload:
- multiple
ms.openlocfilehash: 54623ab1c58d85de55c5b8a24384bf0be46f1a61
ms.sourcegitcommit: d78821f8c353e0102b1554719f549f32dffac71b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2019
ms.locfileid: "58515132"
---
# <a name="parallelcustombuild-task"></a>ParallelCustomBuild görevi

Paralel örneklerini çalıştırmak [CustomBuild görev](../msbuild/custombuild-task.md).

## <a name="parameters"></a>Parametreler

Parametreleri aşağıdaki tabloda açıklanmıştır **ParallelCustomBuild** görev.

|Parametre|Açıklama|
|---------------|-----------------|
|**BreakOnFirstFailure**|İsteğe bağlı **bool** parametresi.|
|**MaxItemsInBatch**|İsteğe bağlı **int** parametresi.|
|**MaxProcesses**|İsteğe bağlı **int** parametresi.|
|**Kaynakları**|Gerekli **Itaskıtem []** parametresi.|

## <a name="see-also"></a>Ayrıca bkz.

[Görev başvurusu](../msbuild/msbuild-task-reference.md)