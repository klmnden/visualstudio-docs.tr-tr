---
title: Dosya izleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
helpviewer_keywords:
- msbuild, file tracking
ms.assetid: e6c66ac0-3464-451f-9192-3b98dca21b4a
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d8d999d65b207f72542b732842f6eb984df40764
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59656823"
---
# <a name="file-tracking"></a>Dosya İzleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Dosya izleme bir işlem ve onun alt işlemleri için Windows dosya sistemi çağrıları günlüğe kaydeder. Aşağıda listelenen işlevleri çağırarak, programlar bu oturum açıp kapatmak ve kullanmak için günlük dosyasını belirtmek ne zaman denetler.  
  
## <a name="in-this-section"></a>Bu Bölümde  
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
