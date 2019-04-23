---
title: 'Nasıl yapılır: Satır düzeyi örnekleme verileri toplama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- performance tools, line-level sampling
ms.assetid: 44803aad-dd39-4c2e-9209-d35185d44983
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2e447b0b15a7a541567932a72dffd7abfc9851e7
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60072389"
---
# <a name="how-to-collect-line-level-sampling-data"></a>Nasıl yapılır: Satır düzeyi örnekleme verileri toplama
Satır düzeyi örnekleme nerede yüksek dışlamalı örnekleri olan bir işlev gibi yoğun işlemci işlevinin kodundaki işlemci zamanının çoğunu harcama belirlemek için profil oluşturucu özelliğidir.

## <a name="overview"></a>Genel Bakış
 Satır düzeyi örnekleme profil oluşturucu programı çağrı yığınını belirlenen aralıklarla size yol gösterir ve bu sonuçları toplar. Bu sonuçları örnekleri durumdayken işlemci çağırılma yürütüldüğü hangi yönergeleri gösterir. Dışlamalı örnekler hakkında toplanan verileri satırlık bir kod ve yönerge işaretçisi (IP) belirlemek için analiz edilir.

 Satır düzeyi örnekleme yönetilen hem de yerel kod için çalışır. Satırlar görünümü ve modüller görünümü bu verileri görüntüleyen performans raporları içerir.

 Karakter başlamak son bilgileri yerel kod için kullanılabilir değil. Çok satırlı ifadeleri için satırın başında bilgi yerel kod için; mevcut değil yalnızca satır sonu bilgileri kullanılabilir.

### <a name="available-data"></a>Kullanılabilir veri
 Kullanılabilir satır düzeyi örnekleme verileri aşağıdaki bilgileri içerir:

- İşlev adı.

- İşlev adresi.

- Satırları başlayın - örnek kod satır sayısı.

- Satır sonu - kaynak satırı numarasını bitiş. Bu genellikle "Satırın başında" verileri tek bir program ifadesi birden çok kaynak kod satırlarına yayıldığında dışında aynıdır.

- Karakter başlayın - toplama örneği başlangıç sütunu. Bu genellikle tek bir satır birden fazla program deyimleri içerdiğinde dışında 0'dır.

- Karakter sonu - toplam örnek sütunun bitiş.

- IP - adresi toplama örneği (yalnızca IP görünümü) nereden alındığı.

  İçinde **modülleri** görüntülemek için bir işlevi satır düzeyi istatistikleri varsa, her işlevin altında istatistikleri yerleştirilir. Ayrıca, her satırı altında iç içe geçmiş IP düzeyi İstatistikler gösterilir.

### <a name="turn-off-line-level-sampling-for-managed-code"></a>Yönetilen kod için satır düzeyi örnekleme devre dışı bırakma
 Varsayılan olarak, satır düzeyi örnekleme etkinleştirilir. Aşağıdaki komutlardan birini kullanarak yönetilen kod için satır düzeyinde veri toplamayı kapatabilirsiniz:

- Profil oluşturmadan önce yazın **VSPerfCLREnv /samplelineoff**. Bu işlem, uygulamaları ve hizmetleri hem de etkiler.

     — veya —

- Bir uygulama başlatma sırasında yazın **VSPerfCmd/lineoff \<diğer bağımsız değişkenleri >**.

## <a name="see-also"></a>Ayrıca bkz.
- [Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)
- [Performans araçları verilerini analiz etme](../profiling/analyzing-performance-tools-data.md)