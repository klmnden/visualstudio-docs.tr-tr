---
title: Eşitleme zamanı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.synchronization
helpviewer_keywords:
- Concurrency Visualizer, Synchronization Time
ms.assetid: affa04cc-8bba-4848-9301-b19846d3c2cb
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f6d97f1b46041578279d5d170f8ce0fd33b81cf3
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55030840"
---
# <a name="synchronization-time"></a>Eşitleme saati
Bu segmentlerde faaliyet zaman çizelgesi, eşitleme sınıflandırılmış bir kez engelleme ile ilişkilidir. Bir iş parçacığı eşitlemede engellendi olarak işaretlendiğinde, bunlardan birini gösterilir:  
  
- İş parçacığının yürütülmesini iyi bilinen bir iş parçacığı eşitleme API çağrısında gibi neden olmuş olabilir `EnterCriticalSection()` veya `WaitForSingleObject()`.  
  
- API eşleştirme algoritmasını tamamen kapsamlı olamaz ve eşitleme, ilkel engelleyen bir temel çekirdek ulaştığından çağrısında bir çerçeve yığın çünkü sonunda bu nedenle diğer kategorilere eşleştirilebilir bazı API'leri de görünebilir Bu kategoriyi eşlendi.  
  
  Bir iş parçacığı engelleme olayı temel nedenini anlamak için engelleme çağrı yığınları ve profil raporlarını dikkatle inceleyin.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [İş Parçacıkları görünümü](../profiling/threads-view-parallel-performance.md)