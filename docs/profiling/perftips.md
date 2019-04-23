---
title: PerfTips | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 509d2d4f-48a5-4cdf-acad-6f7b75421303
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0713ae13038991ec65dcbebe350c9085f7d6a94a
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60103426"
---
# <a name="perftips"></a>PerfTips
Visual Studio hata ayıklayıcı *PerfTips* ve hata ayıklayıcıyla tümleştirilmiş **tanılama araçları** izleme ve hata ayıklarken uygulamanızın performansını analiz yardımcı olur.

 Hata ayıklayıcıyla tümleştirilmiş tanılama araçları, geliştirirken, performans sorunlarından haberdar olma harika bir yol olsa da, hata ayıklayıcı uygulamanızın performansı üzerinde önemli bir etkisi olabilir. Daha doğru performans verilerini toplamak için hata ayıklayıcı dışında çok performans araştırmalarınıza ek bir parçası olarak çalışan Visual Studio tanılama araçları kullanmayı düşünün. Bkz: [profil oluşturma araçları ile veya hata ayıklayıcı olmadan çalıştırın](../profiling/running-profiling-tools-with-or-without-the-debugger.md).

## <a name="perftips"></a>PerfTips
 Hata ayıklayıcı bir kesme noktası veya atlama işlemi yürütmeyi sona erdiğinde, kesme ve önceki kesme noktası arasında geçen süre düzenleyici penceresinde bir ipucu olarak görüntülenir. Daha fazla bilgi için [PerfTips: Performans bilgileri bir Visual Studio ile hata ayıklarken bakışta](https://devblogs.microsoft.com/devops/perftips-performance-information-at-a-glance-while-debugging-with-visual-studio/).

 ![PerfTip](../profiling/media/dbgdiag_perf_perftip.png "DBGDIAG_PERF_PerfTip")

## <a name="diagnostics-tools-window"></a>Tanılama araçları penceresi
 Kesme noktaları ve ilişkili zamanlama verileri kaydedilir **tanılama araçları** penceresi.

 Aşağıdaki grafik gösterildiği **tanılama araçları** penceresi Visual Studio 2015 güncelleştirme 1'de:

 ![DiagnosticTools&#45;güncelleştirme 1](../profiling/media/diagnostictools-update1.png "DiagnosticTools-güncelleştirme 1")

- **Kesme olayları** zaman çizelgesi, hata ayıklama oturumunda ziyaret kesme noktaları işaretleyin. ' A tıklayın, seçmek için bir olay **hata ayıklayıcı** details listesi.

- **CPU kullanımı** grafiği gösterir değişiklik CPU kullanımı tüm işlemci çekirdeği arasında hata ayıklama oturumunda.

- **Olayları** listesi **hata ayıklayıcı** Ayrıntılar bölmesinde, her break olayı için öğeleri içerir.

- **Süresi** sütunu bir kesme olayının olay ve önceki kesme noktası arasında geçen süreyi görüntüler.

## <a name="turn-perftips-on-or-off"></a>PerfTips Aç veya kapat
 PerfTips devre dışı bırakmak veya etkinleştirmek için:

1. Üzerinde **hata ayıklama** menüsünde seçin **seçenekleri**.

2. İşaretleyin veya temizleyin **Göster, hata ayıklama sırasında PerfTip geçen**.

## <a name="turn-the-diagnostic-tools-window-on-or-off"></a>Tanılama araçları penceresini aç veya kapat
 Tanılama araçları penceresi devre dışı bırakmak veya etkinleştirmek için:

1. Üzerinde **hata ayıklama** menüsünde seçin **seçenekleri**.

2. İşaretleyin veya temizleyin **tanılama araçlarını hata ayıklama sırasında etkinleştirme**.

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio profil oluşturma](../profiling/index.md)
- [Araçlar profil oluşturmaya ilk bakış](../profiling/profiling-feature-tour.md)
