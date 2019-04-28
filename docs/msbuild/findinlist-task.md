---
title: Findınlist görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- FindInList task [MSBuild]
- MSBuild, FindInList task
ms.assetid: d49b9f84-52a2-4242-9269-b741a7a7e9f7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7c2f6c5f14f6eff818a265e097f02e2bc76c7372
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62996659"
---
# <a name="findinlist-task"></a>FindInList görevi
Belirtilen bir listede eşleşen itemspec sahip bir öğe bulur.

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır [Findınlist görevi](../msbuild/findinlist-task.md).

|Parametre|Açıklama|
|---------------|-----------------|
|`CaseSensitive`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`arama büyük/küçük harfe; Aksi takdirde, bu değildir. Varsayılan değer `true`.|
|`FindLastMatch`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, son eşleşmenin döndürür; Aksi takdirde, ilk eşleşmeyi döndürür. Varsayılan değer `false`.|
|`ItemFound`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` salt okunur çıkış parametresi.<br /><br /> İlk eşleşen öğe listesinde varsa bulunamadı.|
|`ItemSpecToFind`|Gerekli `String` parametresi.<br /><br /> Aranacak itemspec.|
|`List`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> İtemspec için aranacak listesi.|
|`MatchFileNameOnly`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, yalnızca dosya adı kısmını itemspec karşı eşleşen; Aksi takdirde, tüm itemspec karşı ile eşleşen. Varsayılan değer `true`.|

## <a name="remarks"></a>Açıklamalar
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)