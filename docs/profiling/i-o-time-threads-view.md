---
title: G / Ç zamanı (iş parçacıkları görünümü) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.io
helpviewer_keywords:
- Concurrency Visualizer, I/O time (Threads View)
ms.assetid: 0c4ec14d-d8dd-49c1-999c-dcbf4e8e1dc8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9d7ba29383ddddc02160967a90b56046128d2f19
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56625458"
---
# <a name="io-time-threads-view"></a>G/Ç zamanı (İş Parçacıkları Görünümü)
Bu segmentlerde faaliyet zaman çizelgesi, g/ç olarak sınıflandırılmış bir kez engelleme ile ilişkilidir. Başka bir deyişle, bir iş parçacığı bir g/ç işlemin tamamlanmasını bekliyor. İş parçacığı eşzamanlılık görselleştiricisi g/ç olarak sayılıyor bir ı GÇ ile ilgili çekirdek bekleyin veya bir API engellenmiş olabilir. API'leri gibi `CreateFile()`, `ReadFile()`, ve `WSARecv()` bu gruba girer.

## <a name="see-also"></a>Ayrıca bkz.
- [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)