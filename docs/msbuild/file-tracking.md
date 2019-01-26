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
ms.openlocfilehash: 878d4d7e56c51d8a41a0e3cf3e78d6c83ed5d0b5
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55027678"
---
# <a name="file-tracking"></a>Dosya izleme
Dosya izleme bir işlem ve onun alt işlemleri için Windows dosya sistemi çağrıları günlüğe kaydeder. Aşağıda listelenen işlevleri çağırarak, programlar bu oturum açıp kapatmak ve kullanmak için günlük dosyasını belirtmek ne zaman denetler.  
  
 [EndTrackingContext](../msbuild/endtrackingcontext.md)  
 Geçerli bağlamı İzlemeyi Durdur.  
  
 [ResumeTracking](../msbuild/resumetracking.md)  
 Çağrısı yapıldıktan sonra izlemeyi Sürdür [SuspendTracking](../msbuild/suspendtracking.md).  
  
 [SetThreadCount](../msbuild/setthreadcount.md)  
 İzleme için kullanılacak iş parçacığı sayısını ayarlayın.  
  
 [StartTrackingContext](../msbuild/starttrackingcontext.md)  
 Yeni bir izleme bağlamına başlayın.  
  
 [StartTrackingContextWithRoot](../msbuild/starttrackingcontextwithroot.md)  
 Belirtilen kök ile yeni bir izleme bağlamına başlayın.  
  
 [StopTrackingAndCleanup](../msbuild/stoptrackingandcleanup.md)  
 İzleme ve kullanılan yayın kaynaklarını sonlandır.  
  
 [SuspendTracking](../msbuild/suspendtracking.md)  
 Geçici olarak askıya alma izleme.  
  
 [WriteAllTLogs](../msbuild/writealltlogs.md)  
 Tüm Bağlamlar için izleme günlüklerini dışarı yazın.  
  
 [WriteContextTLogs](../msbuild/writecontexttlogs.md)  
 Geçerli bağlam için izleme günlüğünü dışarı yazın.