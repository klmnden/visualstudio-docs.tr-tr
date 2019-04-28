---
title: Dosya izleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- msbuild, file tracking
ms.assetid: e6c66ac0-3464-451f-9192-3b98dca21b4a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7770da734143b2b6185b266137eeb46ba25bd32a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62968073"
---
# <a name="file-tracking"></a>Dosya izleme
Dosya izleme bir işlem ve onun alt işlemleri için Windows dosya sistemi çağrıları günlüğe kaydeder. Aşağıda listelenen işlevleri çağırarak, programlar bu oturum açıp kapatmak ve kullanmak için günlük dosyasını belirtmek ne zaman denetler.

- [EndTrackingContext](../msbuild/endtrackingcontext.md) geçerli bağlamı İzlemeyi Durdur.

- [ResumeTracking](../msbuild/resumetracking.md) çağrısı yapıldıktan sonra izlemeyi Sürdür [SuspendTracking](../msbuild/suspendtracking.md).

- [SetThreadCount](../msbuild/setthreadcount.md) izleme için kullanılacak iş parçacığı sayısını ayarlayın.

- [StartTrackingContext](../msbuild/starttrackingcontext.md) yeni bir izleme bağlamına başlayın.

- [StartTrackingContextWithRoot](../msbuild/starttrackingcontextwithroot.md) belirtilen kök ile yeni bir izleme bağlamına başlayın.

- [StopTrackingAndCleanup](../msbuild/stoptrackingandcleanup.md) kullanılan son izleme ve yayın kaynaklarını.

- [SuspendTracking](../msbuild/suspendtracking.md) izlemeyi geçici olarak askıya alın.

- [WriteAllTLogs](../msbuild/writealltlogs.md) tüm Bağlamlar için izleme günlüklerini dışarı yazın.

- [WriteContextTLogs](../msbuild/writecontexttlogs.md) geçerli bağlam için izleme günlüğünü dışarı yazın.