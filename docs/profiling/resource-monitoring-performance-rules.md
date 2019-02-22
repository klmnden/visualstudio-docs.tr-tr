---
title: Kaynak izleme performans kuralları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: f0f77faf-0a05-4718-a2c5-47934be40868
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6818bab45532aa44b8ed9ed73978df7c3a05a7bf
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56620687"
---
# <a name="resource-monitoring-performance-rules"></a>Kaynak İzleme Performans Kuralları
Kaynak İzleme kategorisi içindeki performans iletileri, uygulamanızın performansı ile ilgili ek bilgiler sağlayın. Performans sorunlarını analiz etmek için bu verileri kullanabilirsiniz. Bu, bilgilendirme ve her profil oluşturma için bildirilen kurallardır.

|||
|-|-|
|[DA0501: İşlem tarafından ortalama CPU kullanımı profili oluşturuldu.](../profiling/da0501-average-cpu-consumption-by-the-process-being-profiled.md)|Bu ileti bir işlemci yönergeleri uygulamadan çalıştırmakla meşgul olduğu sürenin yüzdesini bildirir. Bildirilen değer profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında bir ortalamadır.|
|[DA0502: İşlem tarafından en fazla CPU kullanımı profili oluşturuldu](../profiling/da0502-maximum-cpu-consumption-by-the-process-being-profiled.md)|Bu ileti, en yüksek işlemci yönergeleri uygulamadan çalıştırmakla meşgul olduğu süre yüzdesi bildirir. Profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında arasında bildirilen en yüksek değeri bildirilen değerdir.|
|[DA0503: İşlem için profili oluşturulan Ortalama Çalışma Kümesi (Bayt)](../profiling/da0503-average-working-set-in-bytes-for-the-process-being-profiled.md)|Bu ileti, profil oluşturma etkinken kullanmadan işlemi bayt cinsinden fiziksel bellek miktarını ortalama bildirir. Bu ölçüm, fiziksel bellek çalışma kümesi bilinir.|
|[DA0504: İşlem için profili oluşturulan En Yüksek Çalışma Kümesi (Bayt)](../profiling/da0504-maximum-working-set-in-bytes-for-the-process-being-profiled.md)|Bu ileti, en fazla profil oluşturma etkinken kullanmadan işlemi bayt cinsinden fiziksel bellek miktarını bildirir.|
|[DA0505: Ortalama Özel Baytlar profil oluşturulan İşlem için ayırılmış](../profiling/da0505-average-private-bytes-allocated-for-the-process-being-profiled.md)|Bu ileti, ortalama profil oluşturma sırasında bayt cinsinden ayrılan işlem etkin sanal bellek miktarını bildirir. Bu ölçü sanal bellek olarak da bilinen *özel baytlar*. Özel baytlar yalnızca işlem içinde çalışan iş parçacığı tarafından erişilebilir bir işlem tarafından ayrılan sanal bellek konumları temsil eder.|
|[DA0506: Profil oluşturulan İşlem için ayırılmış En yüksek sayıda Özel Bayt](../profiling/da0506-maximum-private-bytes-allocated-for-the-process-being-profiled.md)|Bu ileti, profil oluşturma sırasında özel bayt cinsinden ayrılan işlem etkin sanal bellek miktarını bildirir.|