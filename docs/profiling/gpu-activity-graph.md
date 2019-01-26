---
title: GPU Etkinlik Grafiği | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.cpu.graph.gpu
ms.assetid: d7c769af-95fb-49a3-b5ab-deafecee46fa
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0be66a847628cc5968f4cb636066c937e3433c0e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54974873"
---
# <a name="gpu-activity-graph"></a>GPU Etkinlik Grafiği
Eşzamanlılık görselleştiricisi'ndeki GPU Etkinlik Grafiği sistem zaman içinde kullanılmakta olan DirectX altyapıları sayısına göre ölçülen DirectX etkinliği düzeyini görüntüler.  Graf, hangi belirli altyapıları kullanılan göstermez.  Altyapının herhangi bir GPU iş işliyorsa kullanımda olarak kabul edilir.  
  
## <a name="gpu-activity-graph-colors"></a>GPU Etkinlik Grafiği renkleri  
 Yeşil, geçerli işlemin DirectX altyapılarının kullanımının gösterir.  
  
 Açık gri sistem üzerinde başka işlemler tarafından DirectX altyapıları tüketimini gösterir. Diğer işlemler tarafından DirectX altyapıları tüketimini azaltmak için sistem üzerinde çalışan diğer işlemlerin sayısını azaltın.  
  
 Ayrıntılı sistem kullanılmayan DirectX motorlarına kullanılabilirliğini gösterir. Daha fazla kötüye fırsatı bulursanız, bu altyapıları süreciniz için kullanılabilir. Bazı altyapıları yalnızca belirli türde görevleri için kullanılabilir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Kullanım Görünümü](../profiling/utilization-view.md)