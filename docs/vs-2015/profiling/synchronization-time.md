---
title: Eşitleme zamanı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.synchronization
helpviewer_keywords:
- Concurrency Visualizer, Synchronization Time
ms.assetid: affa04cc-8bba-4848-9301-b19846d3c2cb
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 218f333f97e8252993f87893238a0f51f964d6c1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68151393"
---
# <a name="synchronization-time"></a>Eşitleme Zamanı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu segmentlerde faaliyet zaman çizelgesi, eşitleme sınıflandırılmış bir kez engelleme ile ilişkilidir. Bir iş parçacığı eşitlemede engellendi olarak işaretlendiğinde, bunlardan birini gösterilir:  
  
- İş parçacığının yürütülmesini iyi bilinen bir iş parçacığı eşitleme API çağrısında gibi neden olmuş olabilir `EnterCriticalSection()` veya `WaitForSingleObject()`.  
  
- API eşleştirme algoritmasını tamamen kapsamlı olamaz ve eşitleme, ilkel engelleyen bir temel çekirdek ulaştığından çağrısında bir çerçeve yığın çünkü sonunda bu nedenle diğer kategorilere eşleştirilebilir bazı API'leri de görünebilir Bu kategoriyi eşlendi.  
  
  Bir iş parçacığı engelleme olayı temel nedenini anlamak için engelleme çağrı yığınları ve profil raporlarını dikkatle inceleyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)
