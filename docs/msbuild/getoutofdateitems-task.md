---
title: GetOutOfDateItems görev | Microsoft Docs
ms.date: 03/10/2019
ms.topic: reference
f1_keywords:
- vc.task.getoutofdateitems
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), GetOutOfDateItems task
- GetOutOfDateItems task (MSBuild (Visual C++))
author: mikeblome
ms.author: Michael.Blome
ms.workload:
- multiple
ms.openlocfilehash: 668dddcd0854869c9ede7bf96c092d415f41dd17
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58071150"
---
# <a name="getoutofdateitems-task"></a>GetOutOfDateItems task

Eski tlogs okuyan Yardımcısı görev yeni tlogs yazar ve güncel olmayan öğeleri kümesini döndürür.

## <a name="parameters"></a>Parametreler

Parametreleri aşağıdaki tabloda açıklanmıştır **GetOutOfDateItems** görev.

|Parametre|Açıklama|
|---------------|-----------------|
|**CheckForInterdependencies**|İsteğe bağlı **bool** parametresi.|
|**CommandMetadataName**|İsteğe bağlı **dize** parametresi.|
|**DependenciesMetadataName**|İsteğe bağlı **dize** parametresi.|
|**HasInterdependencies**|İsteğe bağlı **bool** çıkış parametresi.|
|**OutOfDateSources**|İsteğe bağlı **Itaskıtem []** çıkış parametresi.|
|**OutputsMetadataName**|Gerekli **dize** parametresi.|
|**Kaynakları**|İsteğe bağlı **Itaskıtem []** parametresi.|
|**TLogDirectory**|Gerekli **dize** parametresi.|
|**TLogNamePrefix**|Gerekli **dize** parametresi.|

## <a name="see-also"></a>Ayrıca bkz.

[Görev başvurusu](../msbuild/msbuild-task-reference.md)