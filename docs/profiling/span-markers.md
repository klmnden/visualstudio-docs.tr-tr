---
title: Span işaretçileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.markers.span
ms.assetid: 736b7765-9c71-44d7-85e5-79787d13d91c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c69b48a5b1b551e2e29b9aa10e7f68ff0df0e379
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56616189"
---
# <a name="span-markers"></a>Kapsam işaretleyicileri
Aralık işaret uygulama anlamlı bir aşamasını temsil eder. Örneğin, belirli bir çalışma öğesini işleniyor zaman aralığını temsil etmek için bir aralık kullanabilirsiniz. Uzunluğu, karşılık gelen uygulaması aşaması süresince temsil eder. Bu örnekte, bir aralık eşzamanlılık görselleştiricisi içinde gösterilmiştir:

 ![Eşzamanlılık görselleştiricisi de aralık bir işaret](../profiling/media/cvmarkerspan.png "CVMarkerSpan") bir aralık işaretçisi eşzamanlılık görselleştiricisi

## <a name="span-category"></a>Aralık kategorisi
 Aralık işaret kategori bağlı olarak beş farklı renkler biriyle görüntülenir. Beşten fazla kategorileri varsa renkleri yinelenir. Kategori herhangi bir tamsayı olabilir. Bu örnekte, beş renkleri gösterilmiştir:

 ![Farklı kategorilerdeki beş yayılma](../profiling/media/cvmarkerspancategory.png "CVMarkerSpanCategory") ilk beş aralık kategorilerin renkleri

## <a name="span-aggregation-markers"></a>Toplama işaretleyicileri
 Bazen aralık işaretçileri bunu birbirine yakın bunlar ayrı ayrı çekilemez eşzamanlılık görselleştiricisi içinde oluşur. Bu oluştuğunda, bir gri *aralık toplama işaret* temsil olarak temel alınan yayılma gösterilir. Bu simgeler biri üzerinde işaretçiyi getirdiğinizde araç ipucu temsil edilen temel alınan yayılma sayısını görüntüler. Yayılma görüntülemek için yakınlaştırın. Tüm yakınlaştırmak ve yine de aralık toplama işaret alın, temel alınan aralık işaretçilerini görüntüleyebileceğiniz [işaretçiler raporu](../profiling/markers-report.md). Bu örnekte, aralık toplama işaret gösterilmiştir:

 ![Bir toplama eşzamanlılık görselleştiricisi işaretçisi span](../profiling/media/cvmarkerspanaggregate.png "CVMarkerSpanAggregate") aralık toplama işaretçisi

## <a name="see-also"></a>Ayrıca bkz.
- [Eşzamanlılık görselleştiricisi işaretleyicileri](../profiling/concurrency-visualizer-markers.md)
- [Eşzamanlılık Görselleştiricisi SDK](../profiling/concurrency-visualizer-sdk.md)