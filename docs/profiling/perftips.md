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
ms.openlocfilehash: 93703bdd4bf2f0046176ceb1f6febd5564f61705
ms.sourcegitcommit: 53bc4c11b82882ab658e34c65ae374060f823531
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71128311"
---
# <a name="perftips"></a>PerfTips
Visual Studio hata ayıklayıcı *PerfTips* ve hata ayıklayıcı ile tümleşik **Tanılama araçları** , hata ayıklarken uygulamanızın performansını izlemenize ve çözümlemenize yardımcı olur.

 Hata ayıklayıcı tümleşik tanılama araçları geliştirilirken performans sorunlarından haberdar olmanın harika bir yoludur, ancak hata ayıklayıcı uygulamanızın performansı üzerinde önemli bir etkiye sahip olabilir. Daha doğru performans verileri toplamak için, hata ayıklayıcının dışında çalışan Visual Studio tanılama araçlarını performans araştırmalarınızın ek bir parçası olarak kullanmayı düşünün. Bkz: [profil oluşturma araçları ile veya hata ayıklayıcı olmadan çalıştırın](../profiling/running-profiling-tools-with-or-without-the-debugger.md).

## <a name="perftips"></a>PerfTips
 Hata ayıklayıcı, bir kesme noktası veya Adımlama işleminde yürütmeyi durdurduktan sonra, kesme ve önceki kesme noktası arasındaki geçen süre, düzenleyici penceresinde bir ipucu olarak görüntülenir. Daha fazla bilgi için bkz [. PerfTips: Visual Studio](https://devblogs.microsoft.com/devops/perftips-performance-information-at-a-glance-while-debugging-with-visual-studio/)ile hata ayıklarken bir bakışta performans bilgileri.

 ![Perftip](../profiling/media/dbgdiag_perf_perftip.png "DBGDIAG_PERF_PerfTip")

## <a name="diagnostics-tools-window"></a>Tanılama Araçları penceresi
 Kesme noktaları ve ilişkili zamanlama verileri **Tanılama araçları** penceresine kaydedilir.

 Aşağıdaki grafikte, Visual Studio 2015 güncelleştirme 1 ' deki **Tanılama araçları** penceresi gösterilmektedir:

 ![DiagnosticTools&#45;güncelleştirme 1](../profiling/media/diagnostictools-update1.png "DiagnosticTools-güncelleştirme 1")

- **Olayları kes** zaman çizelgesi, hata ayıklama oturumunda isabet noktalarını işaret ediyor. **Hata ayıklayıcı** ayrıntıları listesini seçmek için bir olaya tıklayın.

- **CPU kullanımı** grafiği, hata ayıklama oturumunda tüm işlemci çekirdekleri genelinde CPU kullanımı değişikliğini gösterir.

- **Hata ayıklayıcı** ayrıntıları bölmesinin **Olaylar** listesi, her bir kesme olayının öğelerini içerir.

- Bir break olayının **Duration** sütunu, olay ve önceki kesme noktası arasındaki geçen süreyi görüntüler.

## <a name="turn-perftips-on-or-off"></a>PerfTips 'ı aç veya kapat
 PerfTips 'ı etkinleştirmek veya devre dışı bırakmak için:

1. **Hata Ayıkla** menüsünde **Seçenekler**' i seçin.

2. **Hata ayıklama sırasında geçen Perftıp 'Yi göster**veya temizle.

## <a name="turn-the-diagnostic-tools-window-on-or-off"></a>Tanılama Araçları penceresini açma veya kapatma
 Tanılama Araçları penceresini etkinleştirmek veya devre dışı bırakmak için:

1. **Hata Ayıkla** menüsünde **Seçenekler**' i seçin.

2. **Hata ayıklama sırasında tanılama araçlarını etkinleştir**onay kutusunu işaretleyin veya temizleyin.

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio profil oluşturma](../profiling/index.yml)
- [Araçlar profil oluşturmaya ilk bakış](../profiling/profiling-feature-tour.md)
