---
title: CustomBuild görev | Microsoft Docs
ms.date: 03/10/2019
ms.topic: reference
f1_keywords:
- vc.task.custombuild
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), CustomBuild task
- CustomBuild task (MSBuild (Visual C++))
author: mikeblome
ms.author: mblome
ms.workload:
- multiple
ms.openlocfilehash: 04f33f3852f051e1f492cb2b6dca44fcdb260e11
ms.sourcegitcommit: 32144a09ed46e7223ef7dcab647a9f73afa2dd55
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/05/2019
ms.locfileid: "67587014"
---
# <a name="custombuild-task"></a>CustomBuild görevi

Visual C++ Derleyici aracı sarmalar cmd.exe. Bu sınıfın türetildiği [TrackedVCToolTask](../msbuild/trackedvctooltask-base-class.md), ancak dosya izleme dosyası bağımlılıkları bulmak için kullanmaz. Tüm bağımlılıkları AdditionalDependencies düzgün çalışmasını Artımlı derleme için açıkça belirtilmelidir.

## <a name="parameters"></a>Parametreler

Parametreleri aşağıdaki tabloda açıklanmıştır **CustomBuild** görev.

|Parametre|Açıklama|
|---------------|-----------------|
|**BuildSuffix**|İsteğe bağlı **dize** parametresi.|
|**Kaynakları**|Gerekli **Itaskıtem []** parametresi.|
|**TrackerLogDirectory**|İsteğe bağlı **dize** parametresi.|

## <a name="see-also"></a>Ayrıca bkz.

[Görev başvurusu](../msbuild/msbuild-task-reference.md)
