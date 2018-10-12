---
title: CPU kullanım grafiği | Microsoft Docs
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
- vs.cv.cpu.graph
helpviewer_keywords:
- CPU Utilization GraphConcurrency Visualizer, CPU Utilization Graph
ms.assetid: 5332fd38-622d-47a3-874f-8c2fd7a30f95
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fc7dace6156cbb0909c2a54294a82f848fcb5b5e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49292236"
---
# <a name="cpu-utilization-graph"></a>CPU Kullanım Grafiği
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

CPU kullanım grafiği, zaman içinde bir uygulamada kullanım düzeyini gösterir. X ekseni izleme süresini ve y ekseni sistemdeki mantıksal çekirdek sayısını temsil eder. Graf, hangi belirli çekirdek herhangi bir zamanda etkin göstermez. Örneğin, iki çekirdek her belirli bir süre için yüzde 50 kapasitesine çalıştırıyorsanız, bu görünüm kullanılan bir mantıksal çekirdek gösterir.  
  
## <a name="cpu-utilization-graph-colors"></a>CPU kullanım grafiği renkleri  
  
-   Yeşil, geçerli bir işlem tarafından sistemdeki mantıksal Çekirdek kullanımını gösterir.  
  
-   Açık gri sistem üzerinde başka işlemler tarafından mantıksal Çekirdek kullanımını gösterir. Yüksek CPU grafiği açık gri yüzdesi sistem yoğun başka işlemler tarafından yüklenen ve işleminizi bunlara erine olası olduğunu gösterir. Başka işlemler tarafından mantıksal Çekirdek kullanımını azaltmak için sistemde çalışan sayısını azaltın.  
  
-   Koyu gri sistem işlemi tarafından mantıksal Çekirdek kullanımını gösterir. Bu doğrudan denetleyemezsiniz ancak süreciniz için mantıksal çekirdek kullanılabilirliğini etkileyebilir çünkü oluştuğunu bilmek yararlıdır.  
  
-   Beyaz sistemdeki kullanılmayan mantıksal çekirdek kullanılabilirliğini gösterir. Paralellik için daha fazla fırsatı bulursanız, bu çekirdek süreciniz için kullanılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kullanım Görünümü](../profiling/utilization-view.md)   
 [Ortalama CPU Kullanımı](../profiling/average-cpu-utilization.md)



