---
title: Visual Studio'da çok iş parçacıklı uygulamalarda hata ayıklama | Microsoft Docs
ms.custom: ''
ms.date: 09/05/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.gputthreads
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- threading [Visual Studio], debugging
- debugging [Visual Studio], high-performance computing
- debugging [Visual Studio], multithreaded
- multithreaded debugging
- high-performance debugging
ms.assetid: 9d175bc2-1d95-4c47-9bc3-9755af968a9c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 1d238f1c6be12753fe87cece03139185e1c24ad6
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49854781"
---
# <a name="debug-multithreaded-applications-in-visual-studio"></a>Visual Studio'da Çok İş Parçacıklı Uygulamalarda Hata Ayıklama
Bir iş parçacığı, işletim sisteminin işlemci süresi ayırdığı yönergeler sırasıdır. İşletim sisteminde çalışan her işlem en az bir iş parçacığından oluşur. Birden fazla iş parçacığı bulunan işlemler birden çok iş parçacıklı çağrılır.  
  
Bilgisayarlar birden çok işlemci, çok çekirdekli işlemcisi veya hiper iş parçacıklı işlemler birden çok iş parçacığı aynı anda çalıştırabilirsiniz. Paralel işleme birden çok iş parçacığı sayısı büyük ölçüde program performansı artırabilir, ancak birden çok iş parçacığı izlemek gereği getirdiği için aynı zamanda hata ayıklamayı daha zor hale getirebilir.  
  
Ayrıca, çoklu iş parçacığı olası hataların bazı yeni türlerini tanıtır. Genellikle, örneğin, iki veya daha fazla iş parçacığı aynı kaynağa erişmek zorundaysa, ancak aynı anda yalnızca bir iş parçacığı güvenli bir şekilde kaynaklara erişebilir. Çeşit karşılıklı dışlama, yalnızca bir iş parçacığının aynı anda kaynak erişim emin olmak gereklidir. Karşılıklı dışlama yanlış şekilde gerçekleştirilirse oluşturabilirsiniz bir *kilitlenme* koşul burada iş parçacığı yürütebilir. Kilitlenmeler, hata ayıklama için özellikle zor bir sorun olabilir.

Visual Studio hata ayıklama çok iş parçacıklı uygulamalar için farklı araçlar sağlar.

- İş parçacığı için iş parçacıklarında hata ayıklama için kullanılan birincil Araçlar olan **iş parçacıkları** penceresinde, kaynak pencerelerdeki iş parçacığı işaretçileri **Paralel Yığınlar** penceresinde **paralel izleme** penceresinde ve **hata ayıklama konumu** araç çubuğu. Hakkında bilgi edinmek için **iş parçacıkları** penceresi ve **hata ayıklama konumu** araç bkz [izlenecek yol: iş parçacıkları penceresini kullanarak hata ayıklama](../debugger/how-to-use-the-threads-window.md). Nasıl kullanılacağını öğrenmek için **Paralel Yığınlar** ve **paralel izleme** windows bkz [birden çok iş parçacıklı bir uygulamanın hatalarını ayıklamaya başlama](../debugger/get-started-debugging-multithreaded-apps.md). Her iki konuları, iş parçacığı işaretçileri kullanmayı göstermektedir.
  
- Kullanan kod için [görev paralel kitaplığı (TPL)](/dotnet/standard/parallel-programming/task-parallel-library-tpl) veya [eşzamanlılık çalışma zamanı](/cpp/parallel/concrt/concurrency-runtime/), hata ayıklama için kullanılan birincil Araçlar **Paralel Yığınlar** penceresinde, **Paralel izleme** penceresinde ve **görevleri** penceresi ( **görevleri** penceresi JavaScript da destekler). Başlamak için bkz: [izlenecek yol: paralel uygulamada hata ayıklama](../debugger/walkthrough-debugging-a-parallel-application.md) ve [izlenecek yol: C++ AMP uygulamasında hata ayıklama](/cpp/parallel/amp/walkthrough-debugging-a-cpp-amp-application). 

- GPU iş parçacıklarında hata ayıklama için birincil araçtır **GPU iş parçacıkları** penceresi. Bkz: [nasıl yapılır: GPU iş parçacıkları penceresini kullanma](../debugger/how-to-use-the-gpu-threads-window.md).  

- İşlemler için birincil araçlardır **iliştirme** iletişim kutusu, **işlemleri** penceresinde ve **hata ayıklama konumu** araç çubuğu.  
  
Visual Studio ayrıca güçlü kesme noktaları ve izleme noktaları, çok iş parçacıklı uygulamaların hatalarını ayıklarken çok kullanışlı olabilen sağlar. Tek tek iş parçacıkları üzerinde kesme noktaları yerleştirmek için kesme noktası koşulları ve filtreleri kullanabilirsiniz. Bkz: [kesme noktalarını kullanma](../debugger/using-breakpoints.md). 
  
Bir kullanıcı arabirimine sahip birden çok iş parçacıklı bir uygulamada hata ayıklama özellikle zor olabilir. Bu durumda, ikinci bir bilgisayarda uygulamayı çalıştıran ve uzaktan hata ayıklama kullanmayı düşünebilirsiniz. Bilgi için [uzaktan hata ayıklama](../debugger/remote-debugging.md).  
  
## <a name="in-this-section"></a>Bu Bölümde
 [Çok iş parçacıklı bir uygulamanın hatalarını ayıklamaya başlama](../debugger/get-started-debugging-multithreaded-apps.md).  
 İş parçacığı hata ayıklama özellikleriyle özelliklerinde indirimlere Kılavuzlu bir Turu **Paralel Yığınlar** penceresi ve **paralel izleme** penceresi.

 [İş parçacıklarında ve işlemlerde hata ayıklama araçları](../debugger/debug-threads-and-processes.md)  
 İş parçacıklarında ve işlemlerde hata ayıklama araçları'nın özellikleri listeler.  
  
 [Birden Çok İşlemde Hata Ayıklama](../debugger/debug-multiple-processes.md)  
 Birden çok işlemde hata ayıklama açıklanmaktadır.

 [İzlenecek yol: iş parçacıkları penceresini kullanarak hata ayıklama](../debugger/how-to-use-the-threads-window.md).  
 Nasıl kullanılacağını gösteren izlenecek yol **iş parçacıkları** penceresi ve **hata ayıklama konumu** araç çubuğu. 

 [İzlenecek yol: paralel uygulamada hata ayıklama](../debugger/walkthrough-debugging-a-parallel-application.md)  
 Nasıl kullanılacağını gösteren izlenecek yol **Paralel Yığınlar** ve **görevleri** windows.  
  
 [Nasıl Yapılır: Hata Ayıklarken Başka Bir İş Parçacığına Geçme](../debugger/how-to-switch-to-another-thread-while-debugging.md)  
 Hata ayıklama içeriğini başka bir iş parçacığına geçirmek için üç yol.  
  
 [Nasıl Yapılır: İş Parçacıklarını Bayrakla İşaretleme ve İşareti Geri Alma](../debugger/how-to-flag-and-unflag-threads.md)  
 Hata ayıklarken özel dikkat vermek istediğiniz işaretleyin veya bayrak iş parçacıkları.    
  
 [Nasıl Yapılır: Yüksek Performanslı Kümede Hata Ayıklama](../debugger/how-to-debug-on-a-high-performance-cluster.md)  
 Yüksek performanslı küme üzerinde çalışan bir uygulamada hata ayıklama teknikleri.  

 [Yerel Kod İş Parçacıklarında Hata Ayıklama İpuçları](../debugger/tips-for-debugging-threads-in-native-code.md)  
 Yerel iş parçacığı hata ayıklama için yararlı olabilicek basit yöntemler. 

 [Nasıl Yapılır: Yerel Kodda İş Parçacığı Adı Ayarlama](../debugger/how-to-set-a-thread-name-in-native-code.md)  
 İş parçacığınıza görüntülediğiniz bir ad verin **iş parçacıkları** penceresi.  
  
 [Nasıl Yapılır: Yönetilen Kodda İş Parçacığı Adı Ayarlama](../debugger/how-to-set-a-thread-name-in-managed-code.md)  
 İş parçacığınıza görüntülediğiniz bir ad verin **iş parçacıkları** penceresi. 
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Kesme Noktalarını Kullanma](../debugger/using-breakpoints.md)

- Tek bir iş parçacığı hata ayıklama istediğinizde kesme noktası koşulları veya filtreleri kullanın.  
  
- İzleme noktaları olmadan, programınızın yürütülmesini izlemek için etkinleştirin. Bu, kilitlenmeler gibi sorunları incelemek için yararlı olabilir.  
  
  [İş parçacığı oluşturma](/dotnet/standard/threading/index)  
  İş parçacığı kavramları [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] programlama, örnek kod dahil.  
  
  [Bileşenlerinde çoklu iş parçacığı kullanımı](https://msdn.microsoft.com/Library/2fc31e68-fb71-4544-b654-0ce720478779)  
  Nasıl kullanılacağını parçacığı [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] bileşenleri.  
  
  [Eski Kod için Çoklu İş Parçacığı Kullanma Desteği (Visual C++)](/cpp/parallel/multithreading-support-for-older-code-visual-cpp)  
  MFC kullanan C++ programcıları için iş parçacığı oluşturma kavramları ve örnek kod.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş parçacıklarında ve işlemlerde hata ayıklama](../debugger/debug-threads-and-processes.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)