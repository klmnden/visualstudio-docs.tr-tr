---
title: Visual Studio'da çok iş parçacıklı uygulamalarda hata ayıklama | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.gputthreads
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- threading [Visual Studio], debugging
- debugging [Visual Studio], high-performance computing
- debugging [Visual Studio], multithreaded
- multithreaded debugging
- high-performance debugging
ms.assetid: 9d175bc2-1d95-4c47-9bc3-9755af968a9c
caps.latest.revision: 28
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4d841456ab95d06a7b586f7a8566f8530acbb021
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49897504"
---
# <a name="debug-multithreaded-applications-in-visual-studio"></a>Visual Studio'da Çok İş Parçacıklı Uygulamalarda Hata Ayıklama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir iş parçacığı, işletim sisteminin işlemci süresi ayırdığı yönergeler sırasıdır. İşletim sisteminde çalışan her işlem en az bir iş parçacığından oluşur. Birden fazla iş parçacığı bulunan işlemler birden çok iş parçacıklı çağrılır.  
  
 Bilgisayarlar birden çok işlemci, çok çekirdekli işlemcisi veya hiper iş parçacıklı işlemler birden çok iş parçacığı aynı anda çalıştırabilirsiniz. Paralel işleme birden çok iş parçacığı sayısı büyük ölçüde program performansı artırabilir, ancak birden çok iş parçacığı izlemek gereği getirdiği için aynı zamanda hata ayıklamayı daha zor hale getirebilir.  
  
 Ayrıca, çoklu iş parçacığı olası hataların bazı yeni türlerini tanıtır. Genellikle, örneğin, iki veya daha fazla iş parçacığı aynı kaynağa erişmek zorundaysa, ancak aynı anda yalnızca bir iş parçacığı güvenli bir şekilde kaynaklara erişebilir. Çeşit karşılıklı dışlama, yalnızca bir iş parçacığının aynı anda kaynak erişim emin olmak gereklidir. Karşılıklı dışlama yanlış şekilde gerçekleştirilirse oluşturabilirsiniz bir *kilitlenme* koşul burada iş parçacığı yürütebilir. Kilitlenmeler, hata ayıklama için özellikle zor bir sorun olabilir.  
  
 Visual Studio sağlar bir **iş parçacıkları** penceresi, bir GPU iş parçacıkları penceresi, paralel İzleme penceresi ve kolay bir şekilde hata ayıklama çok iş parçacıklı diğer özellikleri. İş parçacığı özellikleri hakkında bilgi edinmenin en iyi yolu, izlenecek yollar yaparak ' dir. Bkz: [izlenecek yol: çok iş parçacıklı uygulamada hata ayıklama](../debugger/walkthrough-debugging-a-multithreaded-application.md) ve [izlenecek yol: C++ AMP uygulamasında hata ayıklama](http://msdn.microsoft.com/library/40e92ecc-f6ba-411c-960c-b3047b854fb5).  
  
 Visual Studio ayrıca güçlü kesme noktaları ve izleme noktaları, çok iş parçacıklı uygulamaların hatalarını ayıklarken çok kullanışlı olabilen sağlar. Tek tek iş parçacıkları üzerinde kesme noktaları yerleştirmek için kesme noktası filtrelerini kullanabilirsiniz. Bkz: [kesme noktalarını kullanma](../debugger/using-breakpoints.md)  
  
 Bir kullanıcı arabirimine sahip birden çok iş parçacıklı bir uygulamada hata ayıklama özellikle zor olabilir. Bu durumda, ikinci bir bilgisayarda uygulamayı çalıştıran ve uzaktan hata ayıklama kullanmayı düşünebilirsiniz. Bilgi için [uzaktan hata ayıklama](../debugger/remote-debugging.md).  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [İş Parçacıklarında ve İşlemlerde Hata Ayıklama](../debugger/debug-threads-and-processes.md)  
 İş parçacıklarında ve işlemlerde hata ayıklama temelleri açıklanır.  
  
 [Birden Çok İşlemde Hata Ayıklama](../debugger/debug-multiple-processes.md)  
 Birden çok işlemde hata ayıklama açıklanmaktadır.  
  
 [Nasıl Yapılır: İş Parçacıkları Penceresini Kullanma](../debugger/how-to-use-the-threads-window.md)  
 İş parçacıkları ile hata ayıklama için kullanışlı yordamlar **iş parçacıkları** penceresi.  
  
 [Nasıl Yapılır: Hata Ayıklarken Başka Bir İş Parçacığına Geçme](../debugger/how-to-switch-to-another-thread-while-debugging.md)  
 Hata ayıklama içeriğini başka bir iş parçacığına geçirmek için üç yol.  
  
 [Nasıl Yapılır: İş Parçacıklarını Bayrakla İşaretleme ve İşareti Geri Alma](../debugger/how-to-flag-and-unflag-threads.md)  
 Hata ayıklarken özel dikkat vermek istediğiniz işaretleyin veya bayrak iş parçacıkları.  
  
 [Nasıl Yapılır: Yerel Kodda İş Parçacığı Adı Ayarlama](../debugger/how-to-set-a-thread-name-in-native-code.md)  
 İş parçacığınıza görüntülediğiniz bir ad verin **iş parçacıkları** penceresi.  
  
 [Nasıl Yapılır: Yönetilen Kodda İş Parçacığı Adı Ayarlama](../debugger/how-to-set-a-thread-name-in-managed-code.md)  
 İş parçacığınıza görüntülediğiniz bir ad verin **iş parçacıkları** penceresi.  
  
 [İzlenecek yol: çok iş parçacıklı uygulamada hata ayıklama](../debugger/walkthrough-debugging-a-multithreaded-application.md).  
 İş parçacığı nasıl yapılacağına ilişkin özelliklerin vurgulandığı özellikleri hata ayıklama için Kılavuzlu bir turu için [!INCLUDE[vs_orcas_long](../includes/vs-orcas-long-md.md)].  
  
 [Nasıl Yapılır: Yüksek Performanslı Kümede Hata Ayıklama](../debugger/how-to-debug-on-a-high-performance-cluster.md)  
 Yüksek performanslı küme üzerinde çalışan bir uygulamada hata ayıklama teknikleri.  
  
 [Yerel Kod İş Parçacıklarında Hata Ayıklama İpuçları](../debugger/tips-for-debugging-threads-in-native-code.md)  
 Yerel iş parçacığı hata ayıklama için yararlı olabilicek basit yöntemler.  
  
 [Görevleri Penceresini Kullanma](../debugger/using-the-tasks-window.md)  
 Durumları ve diğer yararlı bilgiler de dahil olmak üzere tüm yönetilen veya yerel görev nesnelerinin bir listesini gösterir.  
  
 [Paralel Yığınlar Penceresini Kullanma](../debugger/using-the-parallel-stacks-window.md)  
 Gösterir çağrı yığınlarını, birden çok iş parçacığı (veya görevler) tek bir görünüm ve iş parçacıkları (veya görevler) arasında ortak olan yığın kesimlerini de birleştirir.  
  
 [İzlenecek Yol: Paralel Uygulamada Hata Ayıklama](../debugger/walkthrough-debugging-a-parallel-application.md)  
 Paralel Görevler ve Paralel Yığınlar pencerelerinin nasıl kullanılacağını gösteren izlenecek yol.  
  
 [Nasıl Yapılır: Paralel İzleme Penceresini Kullanma](../debugger/how-to-use-the-parallel-watch-window.md)  
 Çoklu iş parçacıkları arasında değerleri ve ifadeleri inceleyin.  
  
 [Nasıl Yapılır: GPU İş Parçacıkları Penceresini Kullanma](../debugger/how-to-use-the-gpu-threads-window.md)  
 İnceleyin ve hata ayıklama sırasında GPU'da çalışan iş parçacıklarının çalışın.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Kesme Noktalarını Kullanma](../debugger/using-breakpoints.md)  
 -   Tek bir iş parçacığında bir kesme noktası yerleştirmek istediğinizde kesme noktası filtrelerini kullanın.  
  
- İzleme noktaları olmadan, programınızın yürütülmesini izlemek için etkinleştirin. Bu, kilitlenmeler gibi sorunları incelemek için yararlı olabilir.  
  
  [İş parçacığı oluşturma](http://msdn.microsoft.com/library/7b46a7d9-c6f1-46d1-a947-ae97471bba87)  
  İş parçacığı kavramları [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] programlama, örnek kod dahil.  
  
  [Bileşenlerinde çoklu iş parçacığı kullanımı](http://msdn.microsoft.com/library/2fc31e68-fb71-4544-b654-0ce720478779)  
  Nasıl kullanılacağını parçacığı [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] bileşenleri.  
  
  [Eski Kod için Çoklu İş Parçacığı Kullanma Desteği (Visual C++)](http://msdn.microsoft.com/library/24425b1f-5031-4c6b-aac7-017115a40e7c)  
  MFC kullanan C++ programcıları için iş parçacığı oluşturma kavramları ve örnek kod.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş parçacıklarında ve işlemlerde hata ayıklama](../debugger/debug-threads-and-processes.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)



