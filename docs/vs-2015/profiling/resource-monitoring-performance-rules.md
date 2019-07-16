---
title: Kaynak izleme performans kuralları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: f0f77faf-0a05-4718-a2c5-47934be40868
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 09c9e41061564a8ffb0e08e3aba75a0d4355d0d2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68160263"
---
# <a name="resource-monitoring-performance-rules"></a>Kaynak İzleme Performans Kuralları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kaynak İzleme kategorisi içindeki performans iletileri, uygulamanızın performansı ile ilgili ek bilgiler sağlayın. Performans sorunlarını analiz etmek için bu verileri kullanabilirsiniz. Bu, bilgilendirme ve her profil oluşturma için bildirilen kurallardır.  
  
|||  
|-|-|  
|[DA0501: İşlem tarafından ortalama CPU kullanımı profili oluşturuldu.](../profiling/da0501-average-cpu-consumption-by-the-process-being-profiled.md)|Bu ileti bir işlemci yönergeleri uygulamadan çalıştırmakla meşgul olduğu sürenin yüzdesini bildirir. Bildirilen değer profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında bir ortalamadır.|  
|[DA0502: İşlem tarafından en fazla CPU kullanımı profili oluşturuldu](../profiling/da0502-maximum-cpu-consumption-by-the-process-being-profiled.md)|Bu ileti, en yüksek işlemci yönergeleri uygulamadan çalıştırmakla meşgul olduğu süre yüzdesi bildirir. Profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında arasında bildirilen en yüksek değeri bildirilen değerdir.|  
|[DA0503: İşlem için profili oluşturulan Ortalama Çalışma Kümesi (Bayt)](../profiling/da0503-average-working-set-in-bytes-for-the-process-being-profiled.md)|Bu ileti, profil oluşturma etkinken kullanmadan işlemi bayt cinsinden fiziksel bellek miktarını ortalama bildirir. Bu ölçüm, fiziksel bellek çalışma kümesi bilinir.|  
|[DA0504: İşlem için profili oluşturulan En Yüksek Çalışma Kümesi (Bayt)](../profiling/da0504-maximum-working-set-in-bytes-for-the-process-being-profiled.md)|Bu ileti, en fazla profil oluşturma etkinken kullanmadan işlemi bayt cinsinden fiziksel bellek miktarını bildirir.|  
|[DA0505: Ortalama Özel Baytlar profil oluşturulan İşlem için ayırılmış](../profiling/da0505-average-private-bytes-allocated-for-the-process-being-profiled.md)|Bu ileti, ortalama profil oluşturma sırasında bayt cinsinden ayrılan işlem etkin sanal bellek miktarını bildirir. Bu ölçü sanal bellek olarak da bilinen *özel baytlar*. Özel baytlar yalnızca işlem içinde çalışan iş parçacığı tarafından erişilebilir bir işlem tarafından ayrılan sanal bellek konumları temsil eder.|  
|[DA0506: Profil oluşturulan İşlem için ayırılmış En yüksek sayıda Özel Bayt](../profiling/da0506-maximum-private-bytes-allocated-for-the-process-being-profiled.md)|Bu ileti, profil oluşturma sırasında özel bayt cinsinden ayrılan işlem etkin sanal bellek miktarını bildirir.|
