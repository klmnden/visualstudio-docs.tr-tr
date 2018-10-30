---
title: Çok iş parçacıklı uygulamada hata ayıklama
description: Visual Studio'da iş parçacıkları penceresi ve hata ayıklama konumu araç çubuğu kullanarak hata ayıklama
ms.custom: ''
ms.date: 05/18/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- multithreaded debugging, tutorial
- tutorials, multithreaded debugging
ms.assetid: adfbe002-3d7b-42a9-b42a-5ac0903dfc25
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f82d53d5bbc9d309ba5d7e8710f0afe2023b8965
ms.sourcegitcommit: d462dd10746624ad139f1db04edd501e7737d51e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50219893"
---
# <a name="walkthrough-debug-a-multithreaded-application-in-visual-studio-using-the-threads-window"></a>İzlenecek yol: Visual Studio'da iş parçacıkları penceresini kullanarak birden çok iş parçacıklı bir uygulamada hata ayıklama
Visual Studio sağlar bir **iş parçacıkları** penceresi ve diğer kullanıcı arabirimi çok iş parçacıklı uygulamalarda hata ayıklamanıza yardımcı olması için öğeleri. Bu öğreticide nasıl kullanılacağını gösterir **iş parçacıkları** penceresi ve **hata ayıklama konumu** araç çubuğu. Diğer araçları hakkında daha fazla bilgi için bkz: [birden çok iş parçacıklı uygulamalarda hata ayıklamaya başlama](../debugger/get-started-debugging-multithreaded-apps.md). Bu öğreticide yalnızca birkaç dakika sürer, ancak bunu tamamlamaya, çok iş parçacıklı uygulamalarda hata ayıklama özellikleriyle alışmanızı.   
  
Bu öğreticiye başlamadan bir çok iş parçacıklı uygulaması projesi gerekir. Bu projeyi oluşturmak için burada listelenen adımları izleyin.  
  
#### <a name="to-create-the-multithreaded-app-project"></a>Çok iş parçacıklı bir uygulama projesi oluşturmak için  
  
1.  Üzerinde **dosya** menüsünde seçin **yeni** ve ardından **proje**.  
  
     **Yeni proje** iletişim kutusu görüntülenir.  
  
2.  İçinde **proje türleri** kutusunda, tercih ettiğiniz dili: **Visual Basic**, **Visual C#** , veya **Visual C++**.  
  
3.  Altında **Windows Masaüstü**, seçin **konsol uygulaması**.  
  
4.  İçinde **adı** kutusuna MyThreadWalkthroughApp adı yazın.  
  
5.  **Tamam**'ı tıklatın.  
  
     Yeni bir konsol projesi görünür. Bir kaynak dosyası projeyi oluşturduğunuzda görünür. Seçtiğiniz dile bağlı olarak, kaynak dosya Module1.vb, Program.cs veya MyThreadWalkthroughApp.cpp çağrılabilir  
  
6.  Kaynak dosyada kod silin ve konunun bölümünde "Bir iş parçacığı oluşturulurken" görünen örnek kod ile değiştirin [iş parçacığı oluşturma ve geçirme verilerini başlangıç zamanında](/dotnet/standard/threading/creating-threads-and-passing-data-at-start-time).  
  
7.  Üzerinde **dosya** menüsünü tıklatın **Tümünü Kaydet**.  
  
#### <a name="to-begin-the-tutorial"></a>Öğreticiyi başlamak için  
  
-   Kaynak Kod Düzenleyicisi'nde aşağıdaki kodu bulun:  
  
    ```VB  
    Thread.Sleep(3000)   
    Console.WriteLine()
    ```  
  
    ```csharp  
    Thread.Sleep(3000);  
    Console.WriteLine();  
    ```  
  
    ```C++  
    Thread::Sleep(3000);  
    Console.WriteLine();  
    ```  
  
#### <a name="to-start-debugging"></a>Hata ayıklamayı başlatmak için  
  
1. ' A tıklayın sol kanalda `Console.WriteLine` ifadesi yeni kesme noktası eklemek için.  
  
    Kaynak kod düzenleyicinin sol tarafındaki kanalda, kırmızı bir daire görünür. Bu, bir kesme noktası bu konumda şimdi ayarlandığını gösterir.  
  
2. Üzerinde **hata ayıklama** menüsünü tıklatın **hata ayıklamayı Başlat** (**F5**).  
  
    Hata ayıklama başladığında, çalıştırmak için konsol uygulaması başlar ve kesme noktası sonra durur.  
  
3. Konsol uygulama penceresine odak bu noktada varsa, tıklayın [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Pencere odağı döndürülecek [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
4. Kaynak Kod Düzenleyicisi'nde aşağıdaki kodu içeren satırı bulun:  
  
   ```VB  
   Thread.Sleep(5000)   
   ```  
  
   ```csharp  
   Thread.Sleep(3000);  
   ```  
  
   ```C++  
   Thread::Sleep(3000);  
   ```
  
#### <a name="to-discover-the-thread-marker"></a>İş parçacığı işaret bulmak için  

1.  Hata ayıklama araç çubuğunda **kaynak iş parçacıklarını Göster** düğmesi ![kaynak iş parçacıklarını Göster](../debugger/media/dbg-multithreaded-show-threads.png "ThreadMarker"). 
  
2.  Pencerenin sol tarafındaki cilt payını bakın. Bu satırda göreceğiniz bir *iş parçacığı işaret* simgesi ![iş parçacığı işaret](../debugger/media/dbg-thread-marker.png "ThreadMarker") , iki bez iş parçacığı benzer. İş parçacığı işaretçisi, bir iş parçacığı bu konuma durdurulduğunu gösterir.  
  
3.  İşaretçi iş parçacığı işaret gelin. Bir DataTip görünür. DataTip durdurulmuş her iş parçacığı için adı ve iş parçacığı kimlik numarasını belirtir. Bu durumda, yalnızca bir iş parçacığı adı büyük olasılıkla yoktur `<noname>`.  

    > [!TIP]
    > Adsız iş parçacığı yeniden adlandırarak belirlemek daha yararlı olabilir. İş parçacıkları penceresinde **Yeniden Adlandır** sağ sonra **adı** iş parçacığı satırdaki sütun.
  
4.  Kısayol menüsünde kullanılabilir seçenekleri görmek için iş parçacığı işaret sağ tıklayın. 
    
  
## <a name="flagging-and-unflagging-threads"></a>Bayrak ekleme ve Unflagging iş parçacıkları  
Özel dikkat vermek istediğiniz iş parçacıklarının bayrağını. İş parçacıklarını işaretleme önemli iş parçacığı izlemek ve önem verdiğiniz olmayan iş parçacıkları yok saymak için iyi bir yolu var.  
  
#### <a name="to-flag-threads"></a>İş parçacıklarını için   

1.  Üzerinde **görünümü** menüsünde **araç çubukları**.  
  
    Emin olun **hata ayıklama konumu** araç seçili.

2.  Git **hata ayıklama konumu** araç çubuğu ve tıklatın **iş parçacığı** listesi.  
  
    > [!NOTE]
    >  Bu araç tarafından üç tanınmış listeleri tanıyabilmesi: **işlem**, **iş parçacığı**, ve **yığın çerçevesi**.  
  
3.  Ne kadar iş parçacığı listede göründüğüne dikkat edin.  
  
4.  Kaynak Kod Düzenleyicisi için geri dönün ve iş parçacığı işaretleyicisini sağ ![iş parçacığı işaret](../debugger/media/dbg-thread-marker.png "ThreadMarker") yeniden.  
  
5.  Kısayol menüsünde, işaret **bayrağı**, iş parçacığı adı ve kimlik numarası'ı tıklatın.  
  
6.  Geri Git **hata ayıklama konumu** araç ve bulma **yalnızca bayraklı iş parçacıklarını Göster** simgesi ![bayraklı iş parçacıklarını Göster](../debugger/media/dbg-threads-show-flagged.png "ThreadMarker") için sağ **iş parçacığı** listesi.  
  
    Bayrakları simgesi düğmesine, önce soluk. Şimdi, etkin bir düğmeye geldi.  
  
7.  Tıklayın **yalnızca bayraklı iş parçacıklarını Göster** simgesi.  
  
    Yalnızca bayraklı iş parçacığı listesinde görünür. (Geri geçiş yapmak için tek bayrakla düğmesine tıklayabilirsiniz **tüm iş parçacıklarını Göster** modu.)

8. İş parçacıkları penceresini seçerek açın **hata ayıklama > Windows > iş parçacıkları**.

    ![İş parçacıkları penceresi](../debugger/media/dbg-threads-window.png "ThreadsWindow")  
  
    İçinde **iş parçacıkları** penceresi, bayrak eklenmiş iş parçacığı bağlı bir belirgin kırmızı bayrak simgesine sahip.

    > [!TIP]
    > Bazı iş parçacıklarını bayrakla olduğunda, bir kod düzenleyicisinde kod satırını sağ tıklatın ve seçin **çalıştırma bayraklı iş parçacıklarını imlece kadar** (bayraklı iş parçacıklarını tüm kod ulaşmak seçtiğinizden emin olun). Bu kod tarafından yürütme sırası daha kolay denetim kolaylaştırır, seçilen satırdaki iş parçacıkları duraklatılır [dondurma ve iş parçacıklarını çözme](#bkmk_freeze).
  
11. Kaynak Kod Düzenleyicisi'nde, iş parçacığı işaret tekrar sağ tıklayın.  
  
     Hangi seçenek kısayol menüsünde kullanılabilir dikkat edin. Yerine **bayrağı**, şimdi **Unflag**. Tıklamayın **Unflag**.  

     İş parçacıklarını bayrakla konusunda bilgi edinmek için sonraki yordama gidin.  
  
#### <a name="to-unflag-threads"></a>İş parçacıklarını bayrakla için  
  
1.  İçinde **iş parçacıkları** penceresinde bayraklı iş parçacığına karşılık gelen satıra sağ tıklayın.  
  
     Bir kısayol menüsü görüntülenir. Seçeneklerine sahip **Unflag** ve **tüm iş parçacıklarını bayrakla**.  
  
2.  İş parçacığının işaretini Kaldır için tıklatın **Unflag**.  

    Bakmak **hata ayıklama konumu** yeniden araç çubuğu. **Yalnızca bayraklı iş parçacıklarını Göster** düğmesini tekrar soluk. Yalnızca bayraklı iş parçacığının işaretini kaldıran. Hiçbir işaretli iş parçacığı olduğundan, araç için geri geçti **tüm iş parçacıklarını Göster** modu. Tıklayın **iş parçacığı** listelemek ve tüm iş parçacıklarının görebildiğinizi doğrulayın.  
  
5.  Geri Git **iş parçacıkları** penceresi ve bilgi sütunu inceleyin.  
  
    İlk sütunda bir dizi listesinin her satırında bayrak anahat simgesi göreceksiniz. (Ana iş parçacığı bayrak yok anlamına gelir.)  
  
6.  İki iş parçacığı ikinci ve üçüncü listenin en üstündeki bayrağı Anahat simgeleri tıklatın. 

    Bayrak simgeleri boş anahatları yerine düz kırmızı olur.  
  
7.  Bayrak sütunu üst kısmındaki düğmeye tıklayın.  
  
    Düğme tıklandığında değiştirilen iş parçacığı listesi sırası. Dizi listesini üstte bayraklı iş parçacıklarını artık sıralanır.  
  
8.  Yeniden, bayrak sütunu üst kısmındaki düğmeye tıklayın.  
  
    Sıralama düzenini yeniden değiştirildi.  
  
## <a name="more-about-the-threads-window"></a>İş parçacıkları penceresi hakkında daha fazla bilgi  
  
#### <a name="to-learn-more-about-the-threads-window"></a>İş parçacıkları penceresi hakkında daha fazla bilgi edinmek için  
  
1.  İçinde **iş parçacıkları** penceresinde üçüncü sütunda soldan inceleyin. Bu sütunun üstünde düğme diyor **kimliği**.  
  
2.  Tıklayın **kimliği**.  
  
     Dizi listesini artık iş parçacığı kimliği numarasına göre sıralanır.  
  
3.  Listedeki herhangi bir iş parçacığı sağ tıklayın. Kısayol menüsünde **onaltılık gösterim**.  
  
     İş parçacığı kimliği sayılarının biçimini değiştirilir.  
  
4.  Fareyi üzerine **konumu** listedeki herhangi bir iş parçacığı sütunu.  
  
     İçeriklerinin anlık bir gecikmeden sonra bir DataTip görünür. Bu iş parçacığı için bir kısmi çağrı yığınını gösterir.

     > [!TIP]
     > İş parçacığı için çağrı yığınlarını için bir grafik görünümü açmak [Paralel Yığınlar](../debugger/using-the-parallel-stacks-window.md) penceresini (hata ayıklama sırasında seçin **hata ayıklama / Windows / Paralel Yığınlar**).  
  
5.  Etiketli üstten dördüncü sütununda Ara **kategori**. İş parçacıkları kategoride sınıflandırılır.  
  
     Bir işlemde oluşturulan ilk iş parçacığında ana iş parçacığı adlandırılır. İş parçacığı listesinde bulun.  
  
6.  Ana iş parçacığı sağ tıklayın ve ardından **iş parçacığına geçiş**.  
  
     A **kesme modu** penceresi görüntülenir. Hata ayıklayıcı şu anda (ana iş parçacığı olduğundan), bunu görüntüleyebilen herhangi bir kod yürütülmüyor söyler.   
  
7.  Bakmak **çağrı yığını** penceresi ve **hata ayıklama konumu** araç çubuğu.  
  
     İçeriğini **çağrı yığını** penceresi değişti. 

## <a name="bkmk_freeze"></a> Dondurma ve iş parçacığı yürütmeyi çözme 

Dondurma ve çözme (askıya alma ve sürdürme) iş parçacıkları iş gerçekleştirmek sırasını denetlemek için iş parçacığı. Bu, kilitlenmeler gibi eşzamanlılık sorunları çözün ve yarış durumlarına yardımcı olabilir.

> [!TIP]
> (Ayrıca genel bir hata ayıklama senaryosuna) diğer iş parçacıklarını dondurma olmadan tek bir iş parçacığı izleyin istiyorsanız bkz [birden çok iş parçacıklı uygulamalarda hata ayıklamaya başlama](../debugger/get-started-debugging-multithreaded-apps.md#bkmk_follow_a_thread).
  
#### <a name="to-freeze-and-unfreeze-threads"></a>Freeze ve iş parçacığı Çöz  
  
1.  İçinde **iş parçacıkları** penceresinde herhangi bir iş parçacığı sağ tıklayın ve ardından **dondurma**.  
  
2.  İkinci sütununa (geçerli iş parçacığı sütunu) bakın. Duraklatma simgesi artık var gibi görünüyor. Bu duraklatma simgesi, iş parçacığı'nın dondurulmuş olup olmadığını gösterir.  
  
3.  Göster **askıya sayısı** içinde seçerek sütun **sütunları** listesi.

    İş parçacığı için askıya alma sayımı artık 1'dir.  
  
4.  Dondurulmuş bir iş parçacığı sağ tıklayın ve ardından **çözme**.  
  
     Geçerli iş parçacığı sütunu ve **askıya sayısı** sütun değişikliği. 
  
## <a name="switching-the-to-another-thread"></a>Geçiş için başka bir iş parçacığı 
  
#### <a name="to-switch-threads"></a>Geçiş yapmak için iş parçacıkları  
  
1.  İçinde **iş parçacıkları** penceresinde (geçerli iş parçacığı sütunu) soldan ikinci sütunda inceleyin. Bu sütunun üstünde düğme, metin veya simge vardır.
  
2.  Geçerli iş parçacığı sütununa bakın ve bir iş parçacığı bir sarı ok olduğuna dikkat edin. Sarı ok, bu iş parçacığı (geçerli yürütme işaretçisi konumunu budur) geçerli iş parçacığının olduğunu gösterir.
  
    Geçerli iş parçacığı simgeyi gördüğünüz iş parçacığı kimlik numarasını not edin. Başka bir iş parçacığı için geçerli iş parçacığı simge taşınır, ancak geri bitirdiğinizde koymak istediğiniz gerekir. 
  
3.  Başka bir iş parçacığı sağ tıklayın ve ardından **iş parçacığına geçiş**.  
  
4.  Bakmak **çağrı yığını** kaynak kod düzenleyicisi penceresi. İçeriği değişmiş.  
  
5.  Bakmak **hata ayıklama konumu** araç çubuğu. Geçerli iş parçacığı simgesi, çok değişti.  
  
6.  Git **hata ayıklama konumu** araç çubuğu. Farklı bir iş parçacığından seçin **iş parçacığı** listesi.  
  
7.  Bakmak **iş parçacıkları** penceresi. Geçerli iş parçacığı simgesi değişmiştir.  
  
8. Kaynak Kod Düzenleyicisi'nde, bir iş parçacığı işaret sağ tıklayın. Kısayol menüsünde, işaret **iş parçacığına geçiş** ve bir iş parçacığı adı/kimlik numarasını'ı tıklatın.  
  
     Artık başka bir iş parçacığı için geçerli iş parçacığı simgesini değiştirme üç yoldan gördünüz: kullanarak **iş parçacıkları** penceresinde **iş parçacığı** listesinde **hata ayıklama konumu** araç ve Kaynak Kod düzenleyicisinde iş parçacığı işaretçisi.  
  
     İş parçacığı işaretleyiciyle, belirli bir konumda durdurulan iş parçacığı geçiş yapabilirsiniz. Kullanarak **iş parçacıkları** penceresi ve **hata ayıklama konumu** araç için herhangi bir iş parçacığı geçirebilirsiniz.   
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çok iş parçacıklı uygulamalarda hata ayıklama](../debugger/debug-multithreaded-applications-in-visual-studio.md)   
 [Nasıl Yapılır: Hata Ayıklarken Başka Bir İş Parçacığına Geçme](../debugger/how-to-switch-to-another-thread-while-debugging.md)
