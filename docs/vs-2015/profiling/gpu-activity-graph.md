---
title: GPU Etkinlik Grafiği | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.cpu.graph.gpu
ms.assetid: d7c769af-95fb-49a3-b5ab-deafecee46fa
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: f4546c3be480349f3e2cb36f483fa8711bc2ac49
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54769054"
---
# <a name="gpu-activity-graph"></a>GPU Etkinlik Grafiği
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Eşzamanlılık görselleştiricisi'ndeki GPU Etkinlik Grafiği sistem zaman içinde kullanılmakta olan DirectX altyapıları sayısına göre ölçülen DirectX etkinliği düzeyini görüntüler.  Graf, hangi belirli altyapıları kullanılan göstermez.  Altyapının herhangi bir GPU iş işliyorsa kullanımda olarak kabul edilir.  
  
## <a name="gpu-activity-graph-colors"></a>GPU Etkinlik Grafiği renkleri  
 Yeşil, geçerli işlemin DirectX altyapılarının kullanımının gösterir.  
  
 Açık gri sistem üzerinde başka işlemler tarafından DirectX altyapıları tüketimini gösterir. Diğer işlemler tarafından DirectX altyapıları tüketimini azaltmak için sistem üzerinde çalışan diğer işlemlerin sayısını azaltın.  
  
 Ayrıntılı sistem kullanılmayan DirectX motorlarına kullanılabilirliğini gösterir. Daha fazla kötüye fırsatı bulursanız, bu altyapıları süreciniz için kullanılabilir. Bazı altyapıları yalnızca belirli türde görevleri için kullanılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kullanım Görünümü](../profiling/utilization-view.md)
