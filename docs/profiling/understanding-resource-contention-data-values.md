---
title: Kaynak çakışması veri değerlerini anlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- concurrency profiling method
- Profiling Tools, concurrency method
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 3d62b21e83f057c2a1d2e4347b3d7bcf6dbc22ad
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53896636"
---
# <a name="understand-resource-contention-data-values"></a>Kaynak çakışması veri değerlerini anlama

Kaynak Çekişme profil oluşturma, paylaşılan bir kaynağa erişim için beklenecek rakip iş parçacığı bir uygulamada zorlanan ayrıntılı çağrı yığını bilgileri her zaman toplar.

Kaynak Çekişme raporları Çekişme ve modüller, İşlevler, kaynak kod satırlarına ve yönergeleri bekleniyor gerçekleştiği için bir kaynak beklerken geçen toplam süre toplam sayısını görüntüler.

- Kapsamlı değerleri bir işlev tarafından kaynak çakışmaları beklenecek zorunlu Çekişme ve işlev beklenen toplam süre toplam sayısını görüntüler.  İşlev tarafından çağrılan alt işlevler kaynaklanan Çekişme kapsamlı değerleri dahil edilir.

- Özel değeri yalnızca, zorlamalı beklenecek bir işlev ve işlev gövdesindeki kod tarafından neden çekişmelerin sayısı görüntüler. Çekişme alt işlevlerin neden dahil edilmez. Dışlamalı süre işlevi, işlev gövdesindeki deyimleri kaynaklanan bekleme süresini de içerir.

Kaynak çakışması rapor görünümleri Ayrıca, zaman içindeki tek tek Çekişme olayları Göster zaman çizelgesi grafikleri içerir ve belirli olay oluşturulan çağrı yığınları göster. Daha fazla bilgi için aşağıdaki konulardan birine bakın:

- [İş parçacığı Ayrıntıları görünümü](../profiling/thread-details-view-contention-data.md)

- [Kaynak Ayrıntıları görünümü](../profiling/resource-details-view-contention-data.md)

Eşzamanlılık profil oluşturması ikinci modu hakkında daha fazla bilgi için bkz: [eşzamanlılık görselleştiricisi](../profiling/concurrency-visualizer.md).