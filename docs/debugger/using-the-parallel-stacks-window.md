---
title: Paralel Yığınlar penceresini kullanarak iş parçacıklarını görüntüleme | Microsoft Docs
ms.custom: ''
ms.date: 04/25/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.parallelstacks
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugger, parallel tasks window
ms.assetid: f50efb78-5206-4803-bb42-426ef8133f2f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d344cc8cd30d250c441788a7920d05086c38ca5f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49940014"
---
# <a name="view-threads-and-tasks-using-the-parallel-stacks-window"></a>Görünüm iş parçacıkları ve görevler Paralel Yığınlar penceresini kullanma
**Paralel Yığınlar** penceresi, çok iş parçacıklı uygulamalarda hata ayıklama işlemi yaparken yararlıdır. Kendi **iş parçacıkları görünümü** gösterir, uygulamanızdaki tüm iş parçacıkları için yığın bilgileri çağırın. İş parçacıkları ve bu iş parçacıkları üzerinde yığın çerçevelerini arasında gezinmenize olanak tanır. Yönetilen kodda **Görevler görünümü** gösterir çağrı yığını <xref:System.Threading.Tasks.Task?displayProperty=fullName> nesneleri. Yerel kodda **Görevler görünümü** gösterir çağrı yığını [görev grupları](/cpp/parallel/concrt/task-parallelism-concurrency-runtime), [paralel algoritmalar](/cpp/parallel/concrt/parallel-algorithms), [zaman uyumsuz aracılar](/cpp/parallel/concrt/asynchronous-agents)ve [Basit görevler](/cpp/parallel/concrt/task-scheduler-concurrency-runtime).  
  
## <a name="threads-view"></a>İş Parçacıkları Görünümü  
 A B ve dış kod ana gittiğiniz tek bir iş parçacığı aşağıda gösterilmiştir. Diğer iki iş parçacığı bazı dış koddan çalışmaya ve B ve dış kod devam iş parçacıkları ve C ve ardından bazı AnonymousMethod devam diğer iş parçacığı biri, bir sorun oluştu.  
  
 ![İş parçacıkları, Paralel Yığınlar penceresini görünümünde](../debugger/media/parallel_stacksthread.png "Parallel_StacksThread")  
  
 Çizimde, geçerli iş parçacığı arama yolunu mavi renkle vurgulanır ve iş parçacığının geçerli konumu (etkin yığın çerçevesini), sarı bir ok ile belirtilir. Geçerli yığın çerçevesi, farklı bir yöntemde seçerek değiştirebilirsiniz **Paralel Yığınlar** penceresi. Ayrıca seçtiğiniz yönteme geçerli iş parçacığı zaten başka bir iş parçacığı veya bir parçası olup olmamasına bağlı olarak geçerli iş parçacığı, geçiş de neden olabilir. Aşağıdaki tabloda ana özelliklerini açıklayan **Paralel Yığınlar** çizimde gösterildiği gibi penceresi.  
  
|Belirtme çizgisi harf|Öğe adı|Açıklama|  
|-|-|-|  
|BİR|Çağrı yığını Segment veya düğüm|Bir dizi yöntem için bir veya daha fazla iş parçacıklarını içerir. Ardından ona bağlı ok satır düğüm yok, iş parçacıkları için tüm arama yolunu temsil eder.|  
|B|Mavi Vurgu|Geçerli iş parçacığı arama yolunu belirtir.|  
|C|Satırları oku|İş parçacıkları için tüm arama yolu oluşturan düğümlerin bağlanın.|  
|D|Düğüm üst araç ipucu|Bu düğüm, arama yolu paylaşan her bir iş parçacığı kullanıcı tanımlı adını ve Kimliğini gösterir.|  
|E|Yöntem|Aynı yöntem bir veya daha fazla yığın çerçevelerini temsil eder.|  
|F|Araç İpucu yöntemi|İş Parçacıkları görünümü'nde, tüm iş parçacıkları tabloda benzer gösterir **iş parçacıkları** penceresi. Görev Görünümü'nde, tüm görevleri bir tablodaki benzer gösterir **görevleri** penceresi.|  
  
 Ayrıca, Paralel Yığınlar penceresini gösteren bir **Kuşbakışı Görünüm** graf pencereye sığdırmak için çok büyük olduğunda ana bölmede simgesi. Grafın tamamında penceresinde görmek için simgesine tıklayabilirsiniz.  
  
## <a name="stack-frame-icons"></a>Yığın çerçeve simgeleri  
 Aşağıdaki tabloda, etkin ve geçerli yığın çerçevesi hakkında bilgi sağlayan simgeleri açıklanmaktadır:  
  
|Simge|Açıklama|  
|-|-|  
|![Paralel Yığınlar sarı ok](../debugger/media/icon_parallelyellowarrow.gif "Icon_ParallelYellowArrow")|Yöntem geçerli iş parçacığının geçerli konumu (etkin yığın çerçevesini) içerdiğini gösterir.|  
|![Paralel Yığınlar İş parçacıkları simgesi](../debugger/media/icon_parallelthreads.gif "Icon_ParallelThreads")|Yöntem, geçerli olmayan bir iş parçacığı geçerli konumunu (etkin yığın çerçevesini) içerdiğini gösterir.|  
|![Paralel Yığınlar yeşil ok](../debugger/media/icon_parallelgreenarrow.gif "Icon_ParallelGreenArrow")|Yöntem geçerli yığın çerçevesi (geçerli hata ayıklayıcı bağlamı) içerdiğini gösterir. Bu yöntem adı göründüğü tüm düğümlerin bold olarak belirlenmiştir.|  
  
## <a name="toolbar-controls"></a>Araç çubuğu denetimleri  
 Aşağıdaki şekil ve tabloda Paralel Yığınlar araç çubuğundaki denetimleri açıklanmaktadır.  
  
 ![Paralel Yığınlar penceresi araç çubuğu](../debugger/media/parallel_stackstoolbar.png "Parallel_StacksToolbar")  
  
|Belirtme çizgisi harf|Denetim|Açıklama|  
|-|-|-|  
|BİR|İş parçacıklarının/görevlerin birleşik giriş kutusu|Görünüm arasında iş parçacığı yığınları çağırın ve çağrı yığınları görevlerin geçiş yapar. Görevler görünümü ve iş parçacıkları görünümü daha fazla bilgi için bkz.|  
|B|Yalnızca bayrak eklenmiş olanları göster|Gösterir gibi diğer hata ayıklama pencerelerinde bayrağı yalnızca iş parçacığı için yığınları çağırın **GPU iş parçacıkları** penceresi ve **paralel izleme** penceresi.|  
|C|Metot görünümünü Aç/Kapat|Yığın görünümü ve yöntem görünümü arasında geçiş yapar. Daha fazla bilgi için yöntemi görmek.|  
|D|Geçerli yığın çerçevesine otomatik Kaydır|Geçerli yığın çerçevesi Autoscrolls diyagram görünümünde olduğunu. Geçerli yığın çerçevesi başka windows değiştirirken veya büyük diyagramlarında yeni kesme noktasına ulaşma bu özellik yararlıdır.|  
|E|Yakınlaştırma denetimini Aç/Kapat|Yakınlaştırma denetimini gizler veya gösterir. CTRL tuşuna basarak ve fare tekerleğini yakınlaştırma denetimi görünürlüğünü bakılmaksızın kapatma ya da CTRL + SHIFT kullanarak yakınlaştırma yapabilirsiniz + '+' yakınlaştırmak için ve CTRL + SHIFT +'-' uzaklaştırmak için. CTRL + F8 tuşuna basarak ekrana sığacak şekilde Yakınlaştır.|  
  
### <a name="context-menu-items"></a>Bağlam menüsü öğeleri  
 Aşağıdaki şekil ve tabloda bir yöntem iş parçacıkları görünümü veya Görevler görünümü sağ tıkladığınızda kullanılabilir kısayol menü öğelerini açıklar. Son altı öğe, doğrudan çağrı yığını penceresinden ödünç ve yeni bir davranış sunar.  
  
 ![Paralel Yığınlar penceresi kısayol menüsü](../debugger/media/parallel_contmenu.png "Parallel_ContMenu")  
  
|Menü Öğesi|Açıklama|  
|-|-|  
|Bayrağı|Seçili öğeyi işaretler.|  
|İşaretini kaldır|Seçili öğeyi unflags.|  
|Dondurma|Seçili öğeyi donuyor.|  
|Çözme|Seçili öğeyi thaws.|  
|Görev (iş parçacığı) geçin|Araç çubuğunda birleşik giriş kutusu aynı işlevi gerçekleştirir, ancak aynı yığın çerçevesini vurgulanmış halde tutar.|  
|Kaynak koduna Git|Kullanıcı sağ yığın çerçevesi için karşılık gelen kaynak kodu konumuna gider.|  
|Çerçeveye geçiş yap|Çağrı yığını penceresinde karşılık gelen menü komutu ile aynıdır. Ancak, Paralel Yığınlar ile birden çok çerçeve bir yönteme karşılık gelebilir. Bu nedenle, her biri belirli bir yığın çerçevesini temsil eden alt menüler, menü öğesi vardır. Yığın çerçevelerini biri geçerli iş parçacığı üzerinde olduğunda, ardından bu yığın çerçevesi için karşılık gelen menü seçilir.|  
|Ayrıştırma için Git|Kullanıcı sağ yığın çerçevesi için karşılık gelen ayrıştırma penceresinde konumuna gider.|  
|Dış Kodu Göster|Dış kodu gizler veya gösterir.|  
|Onaltılık gösterim|Ondalık ve onaltılık görünen arasında geçiş yapar.|  
|Sembol Yükleme Bilgisi|Karşılık gelen iletişim kutusunu görüntüler.|  
|Sembol ayarları|Karşılık gelen iletişim kutusunu görüntüler.|  
  
## <a name="tasks-view"></a>Görevler görünümü  
 Uygulamanızı kullanıyorsa <xref:System.Threading.Tasks.Task?displayProperty=fullName> nesneleri (yönetilen kod için) veya `task_handle` paralellik ifade etmek için (yerel kod için) nesneleri, geçiş yapmak Paralel Yığınlar penceresi araç çubuğu birleşik giriş kutusunda kullanabilirsiniz *Görevler görünümü*. Görev Görünümü görevleri yerine iş parçacığı çağrı yığınlarını gösterir. Görevler görünümü iş parçacıkları Görünümü'ndeki aşağıdaki şekilde farklıdır:  
  
- Görevler ile çalışan iş parçacığı çağrı yığınlarını gösterilmez.  
  
- Görevleri çalıştıran iş parçacığı çağrı yığınlarını görsel olarak göster görevlere ait ilgilendiren çerçeveleri için altındaki ve üstündeki atılır.  
  
- Birden çok görev bir iş parçacığı üzerinde olduğunda, bu görevlerin çağrı yığınları farklı düğümlere bölünür.  
  
  Paralel Yığınlar Görevler görünümü sağ ve sol taraftaki karşılık gelen iş parçacıkları görünümü aşağıda gösterilmiştir.  
  
  ![Görevler Paralel Yığınlar penceresini görünümünde](../debugger/media/parallel_tasksview.png "Parallel_TasksView")  
  
  Tüm çağrı yığınını görmek için yalnızca iş parçacığı yığın çerçevesi sağ tıklatıp ardından görünümüne dönebilirsiniz **iş parçacığına Git**.  
  
  Bir yöntem gelerek önceki tabloda açıklandığı gibi ek bilgileri görebilirsiniz. Aşağıdaki görüntüde iş parçacıkları görünümü ve Görevler görünümü için araç ipucunda bilgileri gösterir.  
  
  ![Paralel Yığınlar penceresini araç ipuçlarında](../debugger/media/parallel_stack_tooltips.png "Parallel_Stack_Tooltips")  
  
## <a name="method-view"></a>Metot görüntüle  
 İş Parçacıkları görünümü veya Görevler görünümünde, araç çubuğundaki yöntemi görünümü simgesine tıklayarak geçerli yöntemi grafikte Özet. Yöntemi bir bakışta tüm yöntemleri çağırmak ya da geçerli yöntemi tarafından çağrılır tüm iş parçacıkları üzerinde görüntüler. Aşağıdaki çizimde, iş parçacıkları görünümü ve de aynı bilgileri yöntemi Görünümü'nde nasıl göründüğünü gösterir.  
  
 ![Paralel Yığınlar penceresini yöntemi görünümünde](../debugger/media/parallel_methodview.png "Parallel_MethodView")  
  
 Yeni bir yığın çerçevesine geçiş, bu yöntem geçerli yöntemi olun ve tüm çağıranlar ve çağrılanlar yeni yöntem için gösterilecek yol. Bu, bazı iş parçacıklarının görünmesini veya kaybolmasını bu yöntem çağrı yığınlarıyla görüntülenip bağlı olarak bu görünümden neden olabilir. Yığın görünümüne dönmek için görünümü araç çubuğu düğmesini tıklatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklama çok iş parçacıklı uygulaması ile çalışmaya başlama](../debugger/get-started-debugging-multithreaded-apps.md)   
 [İzlenecek yol: paralel uygulamada hata ayıklama](../debugger/walkthrough-debugging-a-parallel-application.md)   
 [Hata ayıklayıcı temel bilgileri](../debugger/getting-started-with-the-debugger.md)   
 [Yönetilen kodda hata ayıklama](../debugger/debugging-managed-code.md)   
 [Paralel Programlama](/dotnet/standard/parallel-programming/index)   
 [Görevleri penceresini kullanma](../debugger/using-the-tasks-window.md)   
 [Task Sınıfı](../extensibility/debugger/task-class-internal-members.md)
