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
ms.author: mblome
ms.workload:
- multiple
ms.openlocfilehash: e3393dd7e81fa98c49dd09a32457171286f88f18
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62977496"
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