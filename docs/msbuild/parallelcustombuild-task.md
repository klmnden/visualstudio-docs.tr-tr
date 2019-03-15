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
ms.author: Michael.Blome
ms.workload:
- multiple
ms.openlocfilehash: 506ead6680bd9a0aaaf38d6959da02a14dfee337
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58071149"
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