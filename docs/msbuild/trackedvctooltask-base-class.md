---
title: TrackedVCToolTask sınıfı | Microsoft Docs
ms.date: 03/10/2019
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
author: mikeblome
ms.author: mblome
ms.workload:
- multiple
ms.openlocfilehash: 4a4044416131a27ca313d10d02404094c5f5e219
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62938875"
---
# <a name="trackedvctooltask-base-class"></a>TrackedVCToolTask taban sınıfı

Birçok görevi sonuçta devralınacak <xref:Microsoft.Build.Utilities.Task> sınıfı ve [ToolTask](/dotnet/api/microsoft.build.utilities.tooltask) sınıfı. Bu sınıf türetmek görevleri birkaç parametre ekler [VCToolTask](../msbuild/vctooltask-base-class.md). Bu parametreler, bu belgede listelenir.

## <a name="parameters"></a>Parametreler

Parametreleri aşağıdaki tabloda açıklanmıştır **TrackedVCToolTask** temel sınıfı.

|Parametre|Açıklama|
|---------------|-----------------|
|**DeleteOutputOnExecute**|İsteğe bağlı **bool** parametresi.|
|**EnableExecuteTool**|İsteğe bağlı **bool** parametresi.|
|**ExcludedInputPaths**|İsteğe bağlı **Itaskıtem []** parametresi.|
|**MinimalRebuildFromTracking**|İsteğe bağlı **bool** parametresi.|
|**PathOverride**|İsteğe bağlı **dize** parametresi.|
|**PostBuildTrackingCleanup**|İsteğe bağlı **bool** parametresi.|
|**RootSource**|İsteğe bağlı **dize** parametresi.|
|**SkippedExecution**|İsteğe bağlı **bool** çıkış parametresi.|
|**SourcesCompiled**|İsteğe bağlı **Itaskıtem []** çıkış parametresi.|
|**TLogCommandFile**|İsteğe bağlı **Itaskıtem** parametresi.|
|**TLogReadFiles**|İsteğe bağlı **Itaskıtem []** parametresi.|
|**TLogWriteFiles**|İsteğe bağlı **Itaskıtem []** parametresi.|
|**ToolArchitecture**|İsteğe bağlı **dize** parametresi.|
|**TrackCommandLines**|İsteğe bağlı **bool** parametresi.|
|**TrackFileAccess**|İsteğe bağlı **bool** parametresi.|
|**TrackedInputFilesToIgnore**|İsteğe bağlı **Itaskıtem []** parametresi.|
|**TrackedOutputFilesToIgnore**|İsteğe bağlı **Itaskıtem []** parametresi.|
|**TrackerFrameworkPath**|İsteğe bağlı **dize** parametresi.|
|**TrackerSdkPath**|İsteğe bağlı **dize** parametresi.|

## <a name="see-also"></a>Ayrıca bkz.

[Görev başvurusu](../msbuild/msbuild-task-reference.md)<br/>
[Görevler](../msbuild/msbuild-tasks.md)