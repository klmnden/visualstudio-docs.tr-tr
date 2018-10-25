---
title: Çok iş parçacıklı uygulamalarda hata ayıklamayı öğrenin
description: Paralel Yığınlar ve paralel izleme Visual Studio kullanarak hata ayıklama
ms.custom: H1HackMay2017
ms.date: 08/01/2018
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
ms.assetid: 62df746b-b0f6-4df4-83cf-b1d9d2e72833
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 66239362e454d5ab333214c444aeee3fa54b1b8a
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49936868"
---
# <a name="get-started-debugging-multithreaded-applications-in-visual-studio"></a>Visual Studio'da çok iş parçacıklı uygulamalarda hata ayıklamaya başlama
Visual Studio, çeşitli araçları ve çok iş parçacıklı uygulamalarda hata ayıklamanıza yardımcı olmak için kullanıcı arabirimi öğeleri sağlar. Bu öğreticide, iş parçacığı işaretçileri kullanmak gösterilir **Paralel Yığınlar** penceresinde **paralel izleme** pencere, koşullu kesme noktaları ve filtre kesme noktaları. Bu öğreticide yalnızca birkaç dakika sürer, ancak bunu tamamlamaya, çok iş parçacıklı uygulamalarda hata ayıklama özellikleriyle alışmanızı.

| | |
|---------|---------|
| ![video kamera simgesini film](../install/media/video-icon.png "bir video izleyin") | [Bir video izleyin](https://mva.microsoft.com/en-US/training-courses-embed/getting-started-with-visual-studio-2017-17798/Debugging-Multi-threaded-Apps-in-Visual-Studio-2017-MoZPKMD6D_111787171) benzer adımları gösteren çok iş parçacıklı hata ayıklama. |

Diğer konular, diğer birden çok iş parçacıklı hata ayıklama araçları kullanarak ek bilgileri sağlayın:

- İçin nasıl kullanılacağını gösteren benzer bir konu **hata ayıklama konumu** araç ve **iş parçacıkları** penceresinde görmek [izlenecek yol: birden çok iş parçacıklı bir uygulamada hata ayıklama](../debugger/how-to-use-the-threads-window.md).

- Kullanan bir örnek ile benzer bir konu <xref:System.Threading.Tasks.Task> (yönetilen kod) ve Eşzamanlılık Çalışma zamanı (C++) [izlenecek yol: paralel uygulamada hata ayıklama](../debugger/walkthrough-debugging-a-parallel-application.md). En çok iş parçacıklı uygulama türleri için geçerli olan genel hata ayıklama ipuçları için hem bu konuda hem de bağlı konuyu okuyun.
  
Bu öğreticiye başlamadan bir çok iş parçacıklı uygulaması projesi gerekir. Bu projeyi oluşturmak için burada listelenen adımları izleyin.  
  
#### <a name="to-create-the-multithreaded-app-project"></a>Çok iş parçacıklı bir uygulama projesi oluşturmak için  
  
1.  Üzerinde **dosya** menüsünde seçin **yeni** ve ardından **proje**.  
  
     **Yeni proje** iletişim kutusu görüntülenir.  
  
2.  Tercih ettiğiniz dili seçin: **Visual C#**, **Visual C++**, veya **Visual Basic**.  
  
3.  Altında **Windows Masaüstü**, seçin **konsol uygulaması**.  
  
4.  İçinde **adı** kutusuna MyThreadWalkthroughApp adı yazın.  
  
5.  **Tamam**'ı tıklatın.  
  
     Yeni bir konsol projesi görünür. Bir kaynak dosyası projeyi oluşturduğunuzda görünür. Seçtiğiniz dile bağlı olarak, kaynak dosya Program.cs, MyThreadWalkthroughApp.cpp veya Module1.vb olarak adlandırılabilir.  
  
6.  Kaynak dosyada kod silin ve burada gösterilen örnek kod ile değiştirin.

    ```csharp
    using System;
    using System.Threading;

    public class ServerClass
    {

        static int count = 0;
        // The method that will be called when the thread is started.
        public void InstanceMethod()
        {
            Console.WriteLine(
                "ServerClass.InstanceMethod is running on another thread.");

            int data = count++;
            // Pause for a moment to provide a delay to make
            // threads more apparent.
            Thread.Sleep(3000);
            Console.WriteLine(
                "The instance method called by the worker thread has ended.");
        }
    }

    public class Simple
    {
        public static void Main()
        {
            for (int i = 0; i < 10; i++)
            {
                CreateThreads();
            }
        }
        public static void CreateThreads()
        {
            ServerClass serverObject = new ServerClass();

            Thread InstanceCaller = new Thread(new ThreadStart(serverObject.InstanceMethod));
            // Start the thread.
            InstanceCaller.Start();

            Console.WriteLine("The Main() thread calls this after "
                + "starting the new InstanceCaller thread.");

        }
    }
    ```

    ```C++
    #include "stdafx.h"
    #include <thread>
    #include <iostream>
    #include <vector>

    using namespace;

    int count = 0;

    void doSomeWork() {

        cout << "The doSomeWork function is running on another thread." << endl;
        int data = count++;
        // Pause for a moment to provide a delay to make
        // threads more apparent.
        this_thread::sleep_for(chrono::seconds(3));
        cout << "The function called by the worker thread has ended." << endl;
    }

    int main() {
        vector<thread> threads;

        for (int i = 0; i < 10; ++i) {

            threads.push_back(thread(doSomeWork));
            cout << "The Main() thread calls this after starting the new thread" << endl;
        }

        for (auto& thread : threads) {
            thread.join();
        }

        return 0;
    }
    ```

    ```VB
    Imports System.Threading

    Public Class ServerClass
        ' The method that will be called when the thread is started.
        Public count = 0
        Public Sub InstanceMethod()
            Console.WriteLine(
                    "ServerClass.InstanceMethod is running on another thread.")

            Dim data = count + 1
            ' Pause for a moment to provide a delay to make
            ' threads more apparent.
            Thread.Sleep(3000)
            Console.WriteLine(
                    "The instance method called by the worker thread has ended.")
        End Sub

    End Class

    Public Class Simple

        Public Shared Sub Main()

            Dim ts As New ThreadStarter
            For index = 1 To 10
                ts.CreateThreads()
            Next

        End Sub

    End Class
    Public Class ThreadStarter
        Public Sub CreateThreads()
            Dim serverObject As New ServerClass()

            ' Create the thread object, passing in the
            ' serverObject.InstanceMethod method using a
            ' ThreadStart delegate.
            Dim InstanceCaller As New Thread(AddressOf serverObject.InstanceMethod)

            ' Start the thread.
            InstanceCaller.Start()

            Console.WriteLine("The Main() thread calls this after " _
                        + "starting the new InstanceCaller thread.")

        End Sub
    End Class
    ```
  
7.  Üzerinde **dosya** menüsünü tıklatın **Tümünü Kaydet**.  
  
#### <a name="to-begin-the-tutorial"></a>Öğreticiyi başlamak için  
  
-   Kaynak Kod Düzenleyicisi'nde aşağıdaki kodu bulun: 
  
    ```csharp  
    Thread.Sleep(3000);  
    Console.WriteLine();  
    ```  
  
    ```C++  
    this_thread::sleep_for(chrono::seconds(3));
    cout << "The function called by the worker thread has ended." << endl; 
    ```  

    ```VB
    Thread.Sleep(3000)
    Console.WriteLine()
    ```
  
#### <a name="to-start-debugging"></a>Hata ayıklamayı başlatmak için  
  
1. ' A tıklayın sol kanalda `Thread.Sleep` veya `this_thread::sleep_for` ifadesi yeni kesme noktası eklemek için.  
  
    Kaynak kod düzenleyicinin sol tarafındaki kanalda, kırmızı bir daire görünür. Bu, bir kesme noktası bu konumda şimdi ayarlandığını gösterir. 
  
2. Üzerinde **hata ayıklama** menüsünü tıklatın **hata ayıklamayı Başlat** (**F5**).  
  
    Visual Studio çözümü oluşturur, uygulamayı hata ayıklayıcısı ekli çalıştırmaya başladığında ve uygulama kesme noktasında durur.  
  
   > [!NOTE]
   > Konsol penceresine odak geçiş yapıyorsanız, tıklayın [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Pencere odağı döndürülecek [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
3. Kaynak Kod Düzenleyicisi'nde kesme noktasını içeren satırı bulun:  
  
   ```csharp  
   Thread.Sleep(3000);  
   ```  
  
   ```C++  
   this_thread::sleep_for(chrono::seconds(3)); 
   ```

   ```VB
   Thread.Sleep(3000)
   ```    
  
#### <a name="ShowThreadsInSource"></a>İş parçacığı işaret bulmak için  

1.  Hata ayıklama araç çubuğunda **kaynak iş parçacıklarını Göster** düğmesi ![kaynak iş parçacıklarını Göster](../debugger/media/dbg-multithreaded-show-threads.png "ThreadMarker").

2. Tuşuna **F11** hata ayıklayıcı tek satırlık bir kod ilerlemek için bir kez.
  
3.  Pencerenin sol tarafındaki cilt payını bakın. Bu satırda göreceğiniz bir *iş parçacığı işaret* simgesi ![iş parçacığı işaret](../debugger/media/dbg-thread-marker.png "ThreadMarker") , iki bez iş parçacığı benzer. İş parçacığı işaretçisi, bir iş parçacığı bu konuma durdurulduğunu gösterir.

    Bir iş parçacığı işaret kısmen bir kesme noktası tarafından altına gizlenmiş, dikkat edin. 
  
4.  İşaretçi iş parçacığı işaret gelin. Bir DataTip görünür. DataTip durdurulmuş her iş parçacığı için adı ve iş parçacığı kimlik numarasını belirtir. Bu durumda, muhtemelen adıdır `<noname>`. 
  
5.  Kısayol menüsünde kullanılabilir seçenekleri görmek için iş parçacığı işaret sağ tıklayın.
    
## <a name="ParallelStacks"></a>İş parçacıkları konumunu görüntülemek

İçinde **Paralel Yığınlar** penceresinde geçirebilirsiniz (için görev-tabanlı programlama) ve iş parçacıkları görünümü arasında Görevler görünümü ve her bir iş parçacığı için çağrı yığını bilgilerini görüntüleyebilirsiniz. Bu uygulamada iş parçacıkları görünümü kullanabiliriz.

1. Açık **Paralel Yığınlar** penceresini seçerek **hata ayıklama > Windows > Paralel Yığınlar**. Şuna benzer bir şey görmeniz gerekir (gördüğü bilgiler her iş parçacığı, donanım ve programlama dilini geçerli konumuna bağlı olarak farklı olacaktır).

    ![Paralel Yığınlar penceresini](../debugger/media/dbg-multithreaded-parallel-stacks.png "ParallelStacksWindow")

    Bu örnekte, soldan sağa doğru yönetilen kod için bu bilgileri aldığımız:
    
    - Ana iş parçacığı (sol taraf) üzerinde durduruldu `Thread.Start` (durma noktası iş parçacığı işaret simgesiyle gösterilir ![iş parçacığı işaret](../debugger/media/dbg-thread-marker.png "ThreadMarker")).
    - İki iş parçacığı girmiş `ServerClass.InstanceMethod`, biri olan geçerli iş parçacığı (sarı ok), içinde başka bir iş parçacığı tarafından durdurulduğu sırada `Thread.Sleep`.
    - Yeni bir iş parçacığı (sağdaki) de başlangıç (üzerinde durduruldu `ThreadHelper.ThreadStart`).

2.  Girişlere sağ **Paralel Yığınlar** penceresi kısayol menüsünde kullanılabilir seçenekleri görmek için.

    Bu sağ tıklama menülerinde çeşitli eylemleri gerçekleştirebilirsiniz, ancak bu öğretici için size bu ayrıntıları birkaçını göstereceğiz **paralel izleme** penceresi (sonraki bölümlerde).

    > [!NOTE]
    > Liste görünümünde her iş parçacığı üzerinde bilgilerle, görmeniz fazla ilgileniyorsanız **iş parçacıkları** penceresi yerine. Bkz: [izlenecek yol: birden çok iş parçacıklı bir uygulamada hata ayıklama](../debugger/how-to-use-the-threads-window.md).

## <a name="set-a-watch-on-a-variable"></a>Bir değişken üzerinde bir izleme ayarlayın

1. Açık **paralel izleme** penceresini seçerek **hata ayıklama > Windows > paralel İzleme > paralel Watch 1**.

2. Gördüğünüz hücreyi tıklatın `<Add Watch>` metin (veya 4 sütundaki boş üst bilgi hücresini) türü `data`, ve Enter tuşuna basın.

    Her iş parçacığı için veri değişkeni için değerleri penceresinde görünür.

3. Tıklayın yeniden gördüğünüz hücresinde `<Add Watch>` metin (veya 5 sütun üstbilgisi boş hücreye) türü `count`, ve Enter tuşuna basın.

    Her iş parçacığı sayısı değişkeni için değerleri penceresinde görünür. (Henüz bu kadar bilgi görmüyorsanız, hata ayıklayıcı iş parçacıklarının yürütülmesini ilerlemek için birkaç kez daha F11 tuşuna basarak deneyin.)

    ![Paralel İzleme penceresi](../debugger/media/dbg-multithreaded-parallel-watch.png "ParallelWatchWindow")

4. Mevcut seçenekleri görmek için penceresinde satırları birine sağ tıklayın.

## <a name="flagging-and-unflagging-threads"></a>Bayrak ekleme ve Unflagging iş parçacıkları  
Özel dikkat vermek istediğiniz iş parçacıklarının bayrağını. İş parçacıklarını işaretleme önemli iş parçacığı izlemek ve önem verdiğiniz olmayan iş parçacıkları yok saymak için iyi bir yolu var.  
  
#### <a name="to-flag-threads"></a>İş parçacıklarını için  

1. İçinde **paralel izleme** penceresinde SHIFT tuşunu basılı tutun ve birden çok satır seçin.

2. Sağ tıklatın ve seçin **bayrağı**.

    Şimdi, tüm seçili iş parçacıklarını bayrakla işaretlenir. Artık, yalnızca bayraklı iş parçacıklarını gösterecek şekilde filtreleyebilirsiniz.
  
3.  İçinde **paralel izleme** penceresinde Bul **yalnızca bayraklı iş parçacıklarını Göster** düğmesi ![bayraklı iş parçacıklarını Göster](../debugger/media/dbg-threads-show-flagged.png "ThreadMarker").  
  
4.  Tıklayın **yalnızca bayraklı iş parçacıklarını Göster** düğmesi.  
  
    Yalnızca bayraklı iş parçacığı listesinde görünür.

    > [!TIP]
    > Bazı iş parçacıklarını bayrakla olduğunda, bir kod düzenleyicisinde kod satırını sağ tıklatın ve seçin **çalıştırma bayraklı iş parçacıklarını imlece kadar** (bayraklı iş parçacıklarını tüm kod ulaşmak seçtiğinizden emin olun). Bu kod yürütme sırasını denetlemek kolaylaştıran, seçilen satırdaki iş parçacıkları duraklatılır [dondurma ve iş parçacıklarını çözme](#bkmk_freeze).

5.  Tıklayın **yalnızca bayraklı iş parçacıklarını Göster** geri açıp kapatmak için düğme **tüm iş parçacıklarını Göster** modu.
    
#### <a name="to-unflag-threads"></a>İş parçacıklarını bayrakla için

İş parçacıklarını işaretleme için bir veya daha fazla bayraklı iş parçacıklarını de sağ tıklayabilirsiniz **paralel izleme** penceresi ve **Unflag**.

## <a name="bkmk_freeze"></a> Dondurma ve iş parçacığı yürütmeyi çözme 

> [!TIP]
> Dondurma ve çözme (askıya alma ve sürdürme) iş parçacıkları iş gerçekleştirmek sırasını denetlemek için iş parçacığı. Bu, kilitlenmeler gibi eşzamanlılık sorunları çözün ve yarış durumlarına yardımcı olabilir.
  
#### <a name="to-freeze-and-unfreeze-threads"></a>Freeze ve iş parçacığı Çöz  
  
1.  İçinde **paralel izleme** penceresinde, seçili tüm sütunları içeren sütuna sağ tıklayıp **dondurma**.

    İkinci sütunda duraklatma simgesi artık her satırı için görüntülenir. Duraklatma simgesi, iş parçacığı'nın dondurulmuş olup olmadığını gösterir.

2.  Yalnızca bir satıra tıklayarak satırları kaldırın.

3.  Bir satırın sağ tıklayıp **çözme**.

    Duraklatma simgesi iş parçacığı artık dondurulmuş olup olmadığını gösteren bu satırda kaybolduktan.

4.  Kod düzenleyicisine geçin ve tıklatın **F11**. Çözülmüş iş parçacığı çalıştırır.

    Uygulama, bazı yeni iş parçacıkları de örneği. Herhangi bir yeni iş parçacığı bayrak yok ve değil dondurulmuş dikkat edin.

## <a name="bkmk_follow_a_thread"></a> Tek bir iş parçacığı, koşullu kesme noktaları kullanarak izleyin

Bazen, hata ayıklayıcı tek bir iş parçacığının yürütülmesini izlemek yararlı olabilir. İlginizi olmayan iş parçacıklarını dondurma tarafından bunu bir yoludur ancak bazı senaryolarda (Yineleme örneğin belirli bir hata) için diğer iş parçacıklarını dondurma olmadan tek bir iş parçacığı izleyin isteyebilirsiniz. Diğer iş parçacıklarını dondurma olmadan bir diziyi takip etmeye, ilgilendiğiniz iş parçacığı üzerinde kod parçalamak kaçınmalısınız. Bunu ayarlayarak yapabilirsiniz bir [koşullu kesme noktası](../debugger/using-breakpoints.md#BKMK_Specify_a_breakpoint_condition_using_a_code_expression).

İş parçacığı adı veya iş parçacığı kimliği gibi farklı koşullar üzerinde kesme noktaları ayarlayın Yardımcı olabilecek başka bir yöntem, her bir iş parçacığı için benzersiz olacağını bildiğiniz verileri koşul ayarlamaktır. Bazı belirli veri değeri belirli herhangi bir iş parçacığı daha ilgi olduğu bir yaygın hata ayıklama senaryosuna budur.

#### <a name="to-follow-a-single-thread"></a>Tek bir iş parçacığı izlemek için

1. Daha önce oluşturduğunuz kesme noktasına sağ tıklayıp seçin **koşullar**.

2. İçinde **kesme noktası ayarları** penceresinde, tür `data == 5` koşullu ifade.

    ![Koşullu kesme noktası](../debugger/media/dbg-multithreaded-conditional-breakpoint.png "ConditionalBreakpoint")

    > [!TIP]
    > Ardından belirli bir iş parçacığında fazla ilgileniyorsanız, bir iş parçacığı adı veya iş parçacığı kimliği koşul için kullanın. Bunu yapmak için **kesme noktası ayarları** penceresinde **filtre** yerine **koşullu ifade**ve filtre ipuçlarını izleyin. Uygulama kodunuz, iş parçacığı ad (iş parçacığı kimlikleri hata ayıklayıcıyı başlattığınızda değişikliği) isteyebilirsiniz.

3. Kapat **kesme noktası ayarları** penceresi.

4. Yeniden başlatma tıklayın ![yeniden uygulama](../debugger/media/dbg-tour-restart.png "RestartApp") hata ayıklama oturumunuzu yeniden başlatmak için.

    Veri değişkeni 5 olduğu iş parçacığında koda çalışmamasına neden olur. Sarı ok (geçerli hata ayıklayıcı bağlamı) için konum **paralel izleme** penceresini doğrulayın.

5. Artık, kod (F10) adım ve (F11) kodda ilerleyebilmeniz ve tek iş parçacığının yürütülmesini izleyin.

    Kesme noktası koşulu iş parçacığına benzersizdir ve hata ayıklayıcı (bunları devre dışı bırakmanız gerekebilir) diğer iş parçacıkları üzerinde diğer herhangi bir kesme noktası isabet etmez sürece, kod üzerinde adım ve diğer iş parçacıkları için geçmeden kodda ilerleyebilmeniz.

    > [!NOTE]
    > Hata ayıklayıcı geçildiğinde, tüm iş parçacıklarının çalışacağı. Ancak, diğer iş parçacıklarından biri bir kesme noktasına denk gelir sürece diğer iş parçacıkları üzerinde koda hata ayıklayıcı kesme olmaz. 
  
## <a name="more-about-the-multithreaded-debugging-windows"></a>Çok iş parçacıklı hata ayıklama pencereleri hakkında daha fazla bilgi 

#### <a name="to-switch-to-another-thread"></a>Başka bir iş parçacığına geçiş yapmak için 

- Başka bir iş parçacığına geçiş yapmak için bkz: [nasıl yapılır: başka bir iş parçacığı sırasında hata ayıklama için geçiş](../debugger/how-to-switch-to-another-thread-while-debugging.md) 

#### <a name="to-learn-more-about-the-parallel-stack-and-parallel-watch-windows"></a>Paralel yığını ve paralel izleme pencereleri hakkında daha fazla bilgi için  
  
- Bkz: [nasıl yapılır: paralel yığını penceresini kullanma](../debugger/using-the-parallel-stacks-window.md) 

- Bkz: [nasıl yapılır: paralel İzleme penceresini kullanma](../debugger/how-to-use-the-parallel-watch-window.md) 
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çok iş parçacıklı uygulamalarda hata ayıklama](../debugger/debug-multithreaded-applications-in-visual-studio.md)   
 [Nasıl Yapılır: Hata Ayıklarken Başka Bir İş Parçacığına Geçme](../debugger/how-to-switch-to-another-thread-while-debugging.md)
