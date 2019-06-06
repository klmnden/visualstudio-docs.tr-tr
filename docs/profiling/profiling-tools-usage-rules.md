---
title: Profil Araçları Kullanım Kuralları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: afa7db3b-8c1d-473a-81ac-24ede112a17f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 15b5789a04b4a94156ebec33e525eafe4e22f296
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66745293"
---
# <a name="profiling-tools-usage-rules"></a>Profil Araçları Kullanım Kuralları
Performans kuralları profil oluşturma araçları kullanım kategorisinde en etkili bir şekilde veri toplamak için profil oluşturucu kullanmaya yönelik rehberlik sağlar.

| | |
| - | - |
| [DA0002: VSPerfCorProf.dll eksik](../profiling/da0002-vsperfcorprof-dll-is-missing.md) | Komut satırı profil oluşturma, .NET Framework ikililer için eksik veri içeriyor olabilir. Bu doğru ortam değişkenlerini ayarlanmaması kaynaklanıyor olabilir. |
| [DA0003: Pek çok çekirdek örneği](../profiling/da0003-many-kernel-samples.md) | Hedef ikili yürütülmesini dışında gerçekleşen çok sayıda profil oluşturma örneğinden kaydedilmiş. Daha doğru veriler toplamak için izleme metodunu kullanarak göz önünde bulundurun. |
| [DA0004: Yüksek işlemci kullanımı](../profiling/da0004-high-processor-usage.md) | Profil oluşturma verilerini, profil oluşturma sırasında işlemci sürekli olarak meşgul önerir. Daha doğru veriler toplamak için örnekleme metodu kullanılarak göz önünde bulundurun. |
| [DA0008: Az sayıda örnek toplandı](../profiling/da0008-few-samples-collected.md) | Profil oluşturma çalışmasında toplanan örnek sayısı, istatistiksel açıdan anlamlı olması yeterince yüksek değil. Yeniden profil oluşturma ve uygulama için daha uzun süre çalışan göz önünde bulundurun. Ayrıca, veri toplamak için izleme metodunu kullanarak göz önünde bulundurun. |
| [DA0026: Aşırı çekirdek CPU süresi işlemesi](../profiling/da0026-excessive-kernel-cpu-time-processing.md) | Profil oluşturma çalışma zamanında önemli miktarda işlemci çekirdek modunda oluştu. Örnekleme ölçüm zaman ölçümü kullanmak yerine sistem çağrıları kullanarak göz önünde bulundurun. |
| [DA0029: Desteklenmeyen CLR Sürümü](../profiling/da0029-unsupported-clr-version.md) | Profili oluşturulan ikili bir profil oluşturucu tarafından desteklenmeyen bir .NET Framework sürümü kullanıyor. Profil Oluşturucu raporları sembol adı çözümlenemiyor. |
| [DA0030: Veritabanı projeleri için Katman Etkileşimi ölçüleri toplayın](../profiling/da0030-gather-tier-interaction-measurements-for-database-projects.md) | Çok sayıda yöntemlere çağrıları <xref:System.Data?displayProperty=fullName> ad alanı toplandı. Veritabanı çağrıları ile ilgili verileri içerecek şekilde profilinizde katman etkileşim verileri toplama çalışır göz önünde bulundurun. |
