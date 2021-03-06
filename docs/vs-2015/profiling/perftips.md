---
title: PerfTips | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 509d2d4f-48a5-4cdf-acad-6f7b75421303
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: aac7068fae27e2f0ba699f404374859ef7b91d1a
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65675308"
---
# <a name="perftips"></a>PerfTips
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio hata ayıklayıcı *PerfTips* ve hata ayıklayıcıyla tümleştirilmiş **tanılama araçları** izleme ve hata ayıklarken uygulamanızın performansını analiz yardımcı olur.  
  
 Hata ayıklayıcıyla tümleştirilmiş tanılama araçları, geliştirirken, performans sorunlarından haberdar olma harika bir yol olsa da, hata ayıklayıcı uygulamanızın performansı üzerinde önemli bir etkisi olabilir. Daha doğru performans verilerini toplamak için hata ayıklayıcı dışında çok performans araştırmalarınıza ek bir parçası olarak çalışan Visual Studio tanılama araçları kullanmayı düşünün. Bkz: [hata ayıklama olmadan profil oluşturma araçları çalıştırma](https://msdn.microsoft.com/library/e97ce1a4-62d6-4b8e-a2f7-61576437ff01).  
  
## <a name="perftips"></a>PerfTips  
 Hata ayıklayıcı bir kesme noktası veya atlama işlemi yürütmeyi sona erdiğinde, kesme ve önceki kesme noktası arasında geçen süre düzenleyici penceresinde bir ipucu olarak görüntülenir. Daha fazla bilgi için [PerfTips: Performans bilgileri bir Visual Studio ile hata ayıklarken bakışta](http://blogs.msdn.com/b/visualstudioalm/archive/2014/08/18/perftips-performance-information-at-a-glance-while-debugging-with-visual-studio.aspx).  
  
 ![PerfTip](../profiling/media/dbgdiag-perf-perftip.png "DBGDIAG_PERF_PerfTip")  
  
## <a name="diagnostics-tools-window"></a>Tanılama araçları penceresi  
 Tanılama Araçları penceresinde kesme noktaları ve ilişkili zamanlama verileri zamanlama verileri kaydedilir  
  
 Aşağıdaki grafikte, tanılama araçları penceresi Visual Studio 2015 güncelleştirme 1'de gösterilmektedir:  
  
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
