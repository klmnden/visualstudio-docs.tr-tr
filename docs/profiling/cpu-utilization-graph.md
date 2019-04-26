---
title: CPU kullanım grafiği | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.cpu.graph
helpviewer_keywords:
- CPU Utilization GraphConcurrency Visualizer, CPU Utilization Graph
ms.assetid: 5332fd38-622d-47a3-874f-8c2fd7a30f95
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e09526930bf98141ae4f9d4d204b20383763c208
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62552882"
---
# <a name="cpu-utilization-graph"></a>CPU kullanım grafiği
CPU kullanım grafiği, zaman içinde bir uygulamada kullanım düzeyini gösterir. X ekseni izleme süresini ve y ekseni sistemdeki mantıksal çekirdek sayısını temsil eder. Graf, hangi belirli çekirdek herhangi bir zamanda etkin göstermez. Örneğin, iki çekirdek her belirli bir süre için yüzde 50 kapasitesine çalıştırıyorsanız, bu görünüm kullanılan bir mantıksal çekirdek gösterir.

## <a name="cpu-utilization-graph-colors"></a>CPU kullanım grafiği renkleri

- Yeşil, geçerli bir işlem tarafından sistemdeki mantıksal Çekirdek kullanımını gösterir.

- Açık gri sistem üzerinde başka işlemler tarafından mantıksal Çekirdek kullanımını gösterir. Yüksek CPU grafiği açık gri yüzdesi sistem yoğun başka işlemler tarafından yüklenen ve işleminizi bunlara erine olası olduğunu gösterir. Başka işlemler tarafından mantıksal Çekirdek kullanımını azaltmak için sistemde çalışan sayısını azaltın.

- Koyu gri sistem işlemi tarafından mantıksal Çekirdek kullanımını gösterir. Bu doğrudan denetleyemezsiniz ancak süreciniz için mantıksal çekirdek kullanılabilirliğini etkileyebilir çünkü oluştuğunu bilmek yararlıdır.

- Beyaz sistemdeki kullanılmayan mantıksal çekirdek kullanılabilirliğini gösterir. Paralellik için daha fazla fırsatı bulursanız, bu çekirdek süreciniz için kullanılabilir.

## <a name="see-also"></a>Ayrıca bkz.
- [Kullanım Görünümü](../profiling/utilization-view.md)
- [Ortalama CPU Kullanımı](../profiling/average-cpu-utilization.md)