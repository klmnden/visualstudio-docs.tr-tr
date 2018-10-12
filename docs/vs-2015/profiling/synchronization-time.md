---
title: Eşitleme zamanı | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.cv.threads.timeline.synchronization
helpviewer_keywords:
- Concurrency Visualizer, Synchronization Time
ms.assetid: affa04cc-8bba-4848-9301-b19846d3c2cb
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6d7fe50e8b678e6baa02deeab5f111c71645dbb4
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49219732"
---
# <a name="synchronization-time"></a>Eşitleme Zamanı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu segmentlerde faaliyet zaman çizelgesi, eşitleme sınıflandırılmış bir kez engelleme ile ilişkilidir. Bir iş parçacığı eşitlemede engellendi olarak işaretlendiğinde, bunlardan birini gösterilir:  
  
-   İş parçacığının yürütülmesini iyi bilinen bir iş parçacığı eşitleme API çağrısında gibi neden olmuş olabilir `EnterCriticalSection()` veya `WaitForSingleObject()`.  
  
-   API eşleştirme algoritmasını tamamen kapsamlı olamaz ve eşitleme, ilkel engelleyen bir temel çekirdek ulaştığından çağrısında bir çerçeve yığın çünkü sonunda bu nedenle diğer kategorilere eşleştirilebilir bazı API'leri de görünebilir Bu kategoriyi eşlendi.  
  
 Bir iş parçacığı engelleme olayı temel nedenini anlamak için engelleme çağrı yığınları ve profil raporlarını dikkatle inceleyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)



