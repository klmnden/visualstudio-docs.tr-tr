---
title: Hatalı davranan çok iş parçacıklı uygulamalar için ortak desenler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.tools.gallery
helpviewer_keywords:
- Concurrency Visualizer, common patterns for poorly-behaved multithreaded applications
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4aec033266ccb2a6e6dcd0342669b7c31082488a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62788931"
---
# <a name="common-patterns-for-poorly-behaved-multithreaded-applications"></a>Hatalı davranan çok iş parçacıklı uygulamalar için ortak desenler

Eşzamanlılık görselleştiricisi, geliştiricilerin çok iş parçacıklı uygulamanın davranışı görselleştirmek için yardımcı olur. Bu araç, hatalı davranan çok iş parçacıklı uygulamalar için ortak desenler Galerisi içerir. Galeri, aracı, bu sorunu çözmek için büyük olasılıkla sonucunu bu davranışı ve en yaygın yaklaşımı her desen tarafından temsil edilen davranışı açıklaması ile birlikte sunulan tipik ve tanınabilir visual desenleri içerir.

## <a name="lock-contention-and-serialized-execution"></a>Kilit çakışması ve seri hale getirilmiş yürütme

![Kilit çakışması serileştirilmiş yürütülmesine neden](../profiling/media/lockcontention_serialized.png "LockContention_Serialized")

Bazen bir paralel uygulama stubbornly birkaç iş parçacığı vardır ve bilgisayarın yeterli sayıda mantıksal çekirdek olsa bile seri olarak yürütülecek devam eder. Çok iş parçacıklı macos'tan, hatta belki de seri bir uygulama biraz yavaş ilk belirtisidir. İş Parçacıkları görünümü'nde, paralel olarak çalışan birden çok iş parçacığı görmez; Bunun yerine, yalnızca bir iş parçacığı herhangi bir anda yürütülmekte olan bakın. Bu noktada, bir iş parçacığı eşitleme segmente tıklarsanız, engellenen iş parçacığı (engelleme çağrı yığınını) ve engelleme koşulu (engellemeyi kaldırma çağrı yığını) kaldırılan iş parçacığı için bir çağrı yığınını görebilirsiniz. Engellemeyi kaldırma çağrı yığını kullanarak, çözümlediğiniz işleminde meydana gelirse, ayrıca, bir iş parçacığı için hazır bağlayıcı görüntülenir. Bu noktadan itibaren neden serileştirme daha fazla araştırmak için engelleme ve engellemesini kaldırma çağrı yığınlarını koda gidebilirsiniz.

Aşağıdaki çizimde gösterildiği gibi Concurrency Visualizer Ayrıca, birden çok iş parçacığı varlığına rağmen sadece bir mantıksal çekirdek uygulama tüketir. CPU Kullanımı görünümünde Bu belirti kullanıma sunabilirsiniz.

Daha fazla bilgi için MSDN dergisi makalesinde "Başlangıç" sorun bölümüyle bkz [iş parçacığı performans - kaynak çekişmesi eşzamanlılık profil oluşturması Visual Studio 2010'daki](https://msdn.microsoft.com/magazine/ff714587.aspx).

![Kilit çakışması](../profiling/media/lockcontention_2.png "LockContention_2")

## <a name="uneven-workload-distribution"></a>Düzensiz iş yükü dağıtım

![Düzensiz iş yükü](../profiling/media/unevenworkload_1.png "UnevenWorkLoad_1")

Bir uygulamada birden fazla paralel iş parçacıkları arasında düzensiz bir dağıtım iş ortaya çıktığında, her iş parçacığı, iş tamamlandığında tipik Merdiveni adım düzeni önceki resimde gösterildiği gibi görünür. Eşzamanlılık görselleştiricisi, çoğunlukla her eş zamanlı iş parçacığı için çok yakın başlangıç zamanlarını gösterir. Ancak, bu iş parçacıkları genellikle aynı anda bitiş yerine düzensiz bir şekilde bitmelidir. Bu düzen, düzensiz bir dağıtım grubu için performansın yol açabilecek paralel iş parçacıkları arasında iş gösterir. İş tarafından paralel iş parçacıkları arasında bölünmüş algoritması yeniden değerlendirmek için en iyi yaklaşım ilgili bir sorun var.

Aşağıdaki çizimde gösterildiği gibi Concurrency Visualizer CPU kullanımı, aşamalı bir step-down olarak da CPU Kullanımı görünümünde Bu belirti kullanıma sunabilirsiniz.

![Düzensiz iş yükü](../profiling/media/unevenworkload_2.png "UnevenWorkload_2")

## <a name="oversubscription"></a>Aşırı abonelik

![Aşırı abonelik](../profiling/media/oversubscription.png "aşırı abonelik")

Gecikmeyi söz konusu olduğunda, bir işlemde etkin iş parçacığı sayısını sistem üzerindeki kullanılabilir mantıksal çekirdek sayısından büyüktür. Önceki çizimde, tüm etkin iş parçacığı sayısı önemli önalım gösterilmeyen gecikmeyi, sonuçları gösterilmektedir. Ayrıca, gösterge, Önalım (Bu örnekte 84 yüzde) olarak harcanan zamanı büyük bir yüzdesini gösterir. Bu işlem mantıksal çekirdek sayısından daha fazla eşzamanlı iş parçacığının sistem isteyen olduğunu gösteriyor olabilir. Ancak, bu sistemdeki diğer işlemler için bu işlem kullanılabilir kabul edildiği kaynakları kullanıyorsanız da gösterebilir.

Bu sorunu değerlendirirken aşağıdakileri dikkate almanız gerekir:

- Genel sistem oversubscribed. Sistemdeki diğer işlemler, iş parçacığı öncelik verme, göz önünde bulundurun. İş Parçacıkları görünümü önalım segmente üzerine geldiğinizde, araç ipucu iş parçacığı ve iş parçacığı etkisiz işlemi tanımlayın. Bu işlem mutlaka işleminizi boşaltıldı çalıştınız sırasında yürütülen bir değildir, ancak ne işleminizi karşı önalım baskısı oluşturulan hakkında bir ipucu sağlar.

- İşleminizi iş parçacıkları bu aşamada iş yürütme için uygun sayıda nasıl belirlediğini değerlendirin. İşleminizi doğrudan active paralel iş parçacığı sayısını hesaplar, sistem üzerindeki kullanılabilir mantıksal çekirdek sayısı için daha iyi hesabına bu algoritmayı değiştirme göz önünde bulundurun. Eşzamanlılık Çalışma zamanı, görev paralel kitaplığı veya PLINQ kullanırsanız, bu kitaplıklara iş parçacığı sayısını hesaplama işini gerçekleştirir.

## <a name="inefficient-io"></a>Verimli g/ç

![Verimsiz miyim&#47;O](../profiling/media/inefficient_io.png "Inefficient_IO")

Aşırı kullanımı veya kötüye kullanımı g/ç verimsizlikleri uygulamalarında ortak bir nedeni var. Önceki çizimde göz önünde bulundurun. Görünür zaman çizelgesi profili görünür iş parçacığı süresinin yüzde 44 g/ç tarafından tüketilmesi gösterir. Zaman Çizelgesi profili oluşturulan uygulama sık sık g/ç tarafından engellendiğini gösterir g/ç, büyük miktarlarda gösterir. G/ç ve programınızın burada engellendi türleri hakkında daha fazla ayrıntı görmek için sorunlu bölgelere yakınlaştırma, görünür zaman çizelgesi profili inceleyin ve geçerli çağrı yığınlarını görmek için belirli bir g/ç blok'ye tıklayın.

## <a name="lock-convoys"></a>Kilit Konvoyları

![Kilitleme Konvoyları](../profiling/media/lock_convoys.png "Lock_Convoys")

Kilit Konvoyları uygulama kilitlenmeden önce gelen, ilk olarak sunulan bir sırada alır ve kilit alma hızı edinme hızından daha yüksek olduğunda oluşur. Bu iki koşul birleşimi için yedekleme başlatmak kilit isteklerin neden olur. Bu sorunu combat yollarından biri, "haksız" kilitler veya kilidi açılmış durumda bulunacak ilk iş parçacığında erişmesini kilitleri kullanmaktır. Önceki çizimde, bu konvoy davranış gösterir. Sorunu çözmek için eşitleme nesneleri için Çekişme azaltmayı deneyin ve haksız kilitleri kullanmayı deneyin.

## <a name="see-also"></a>Ayrıca bkz.

[İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)