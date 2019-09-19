---
title: CPU kullanım verilerini çözümleme (ASP.NET)
description: CPU kullanımı Tanılama aracını kullanarak ASP.NET uygulamalarında uygulama performansını ölçme
ms.custom: mvc
ms.date: 08/06/2018
ms.topic: quickstart
helpviewer_keywords:
- Profiling Tools, quick start
- Diagnostics Tools, CPU Usage
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: cbaaa53fe737761fdd938b7861c371e8e5619acc
ms.sourcegitcommit: 53bc4c11b82882ab658e34c65ae374060f823531
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71128174"
---
# <a name="quickstart-analyze-cpu-usage-data-in-visual-studio-aspnet"></a>Hızlı Başlangıç: Visual Studio 'da CPU kullanım verilerini çözümleme (ASP.NET)

Visual Studio, uygulamanızdaki performans sorunlarını çözümlemenize yardımcı olacak birçok güçlü özellik sunar. Bu konu, temel özelliklerden bazılarını öğrenmenin hızlı bir yolunu sağlar. Burada, yüksek CPU kullanımı nedeniyle performans sorunlarını belirlemek için bir araca bakacağız. Tanılama araçları, yerel/C++ geliştirme ve ASP.NET dahil olmak üzere Visual Studio .NET geliştirme için desteklenir.

Tanılama hub'ı, çok sayıda çalıştırın ve tanılama oturumunuzu yönetmek için diğer bir seçenek sunar. Burada açıklanan **CPU kullanım** aracı size ihtiyacınız olan verileri sağlamıyorsa, [diğer profil oluşturma araçları](../profiling/profiling-feature-tour.md) sizin için yararlı olabilecek farklı türde bilgiler sağlar. Çoğu durumda, uygulamanızın performans sorunu, CPU, bellek, işleme kullanıcı Arabirimi veya ağ isteği süresi gibi dışında bir şey tarafından kaynaklanabilir.

Windows 8 ve üzeri, hata ayıklayıcısı ile profil oluşturma araçları çalıştırmak için gereklidir (**tanılama araçları** pencere). Windows 7 ve üzeri sürümlerde, [performans profil oluşturucuyu](../profiling/profiling-feature-tour.md)son mordıtem Aracı ' nı kullanabilirsiniz.

## <a name="create-a-project"></a>Proje oluşturma

1. Visual Studio 'da **Dosya** > **Yeni proje**' yi seçin.

1. **C#Görsel**bölümünde **Web**' i seçin ve ardından orta bölmedeki **ASP.NET Web uygulaması (.NET Framework)** öğesini seçin.

    **ASP.NET Web uygulaması** proje şablonunu görmüyorsanız, **Yeni proje** iletişim kutusunun sol bölmesindeki **Visual Studio yükleyicisi aç** bağlantısına tıklayın. Visual Studio Yükleyicisi'ni başlatır. **ASP.net ve Web geliştirme** iş yükünü seçin ve ardından **Değiştir**' i seçin.

1. **MyProfilingApp_MVC** gibi bir ad yazın ve **Tamam**' a tıklayın.

1. Görüntülenen iletişim kutusunda Ortadaki bölmede **MVC** ' yi seçin ve ardından **Tamam**' a tıklayın.

    Visual Studio projesi oluşturur. Çözüm Gezgini (sağ bölme) proje dosyalarınızı gösterir.

1. Çözüm Gezgini, modeller klasörüne sağ tıklayın ve**sınıf** **Ekle** > ' yi seçin.

1. Yeni sınıfı `Data.cs` adlandırın ve **Ekle**' yi seçin.

1. Çözüm Gezgini ' de açın `Models/Data.cs` ve aşağıdaki `using` ifadeyi dosyanın en üstüne ekleyin:

    ```csharp
    using System.Threading;
    ```

1. Data.cs ' de, aşağıdaki kodu değiştirin:

    ```csharp
    public class Data
    {
    }
    ```

    Bu kod ile:

    ```csharp
    public class ServerClass
    {
        const int MIN_ITERATIONS = int.MaxValue / 1000;
        const int MAX_ITERATIONS = MIN_ITERATIONS + 10000;

        long m_totalIterations = 0;
        readonly object m_totalItersLock = new object();
        // The method that will be called when the thread is started.
        public void GenerateData()
        {
            Console.WriteLine(
                "ServerClass.InstanceMethod is running on another thread.");

            var x = GetNumber();
        }

        private int GetNumber()
        {
            var rand = new Random();
            var iters = rand.Next(MIN_ITERATIONS, MAX_ITERATIONS);
            var result = 0;
            lock (m_totalItersLock)
            {
                m_totalIterations += iters;
            }
            // we're just spinning here
            // and using Random to frustrate compiler optimizations
            for (var i = 0; i < iters; i++)
            {
                result = rand.Next();
            }
            return result;
        }
    }

    public class Simple
    {
        int numberOfThreads = 200;

        public Simple()
        {
            for (int i = 0; i < numberOfThreads; i++)
            {
                CreateThreads();
            }
        }
        public static void CreateThreads()
        {
            ServerClass serverObject = new ServerClass();

            Thread InstanceCaller = new Thread(new ThreadStart(serverObject.GenerateData));
            // Start the thread.
            InstanceCaller.Start();

            Console.WriteLine("The Main() thread calls this after "
                + "starting the new InstanceCaller thread.");

        }

        public int GetData()
        {
            // Not returning any meaningful data.
            return numberOfThreads;
        }
    }
    ```

1. Çözüm Gezgini, *Controller/HomeControllers. cs*' yi açın ve aşağıdaki kodu değiştirin:

    ```csharp
    public ActionResult About()
    {
        ViewBag.Message = "Your application description page.";

        return View();
    }
    ```

    Bu kod ile:

    ```csharp
    public ActionResult About()
    {
        Models.Simple s = new Models.Simple();

        ViewBag.Message = "Your application description page.";

        return View(s.GetData());
    }
    ```

## <a name="step-1-collect-profiling-data"></a>1\. Adım: Profil oluşturma verilerini topla

1. İlk olarak, `Simple` kurucudaki Bu kod satırında uygulamanızda bir kesme noktası ayarlayın:

    `for (int i = 0; i < 200; i++)`

    Kod satırının solundaki cilt paya tıklayarak bir kesme noktası ayarlayın.

1. Sonra, `Simple` oluşturucunun sonundaki kapanış küme ayracı üzerinde ikinci bir kesme noktası ayarlayın:

     ![Profil oluşturma için kesme noktaları ayarla](../profiling/media/quickstart-cpu-usage-breakpoints-aspnet.png)

    > [!TIP]
    > İki kesme noktaları ayarlayarak veri toplamayı çözümlemek istediğiniz kod parçalarını sınırlayabilirsiniz.

1. **Tanılama araçları** pencere, siz kapatmadığınız müddetçe zaten görünür. Pencereyi ayarlayıp yeniden getirmek için tıklayın **hata ayıklama** > **Windows** > **tanılama araçlarını Göster**.

1. Tıklayın **hata ayıklama** > **hata ayıklamayı Başlat** (veya **Başlat** araç çubuğunda veya **F5**).

1. Uygulamanın yüklenmesi tamamlandığında, yeni kodu çalıştırmaya başlamak için Web sayfasının en üstündeki **hakkında hakkında** bağlantısına tıklayın.

1. Tanılama araçlarının **Özet** görünümüne bakın.

1. Hata ayıklayıcı duraklatıldığında, CPU kullanım verilerinin toplanmasını sağlamak için **CPU profilini kaydet**' i seçip **CPU kullanımı** sekmesini açın.

     ![Tanılama araçları CPU profilini oluşturmayı etkinleştirir](../profiling/media/quickstart-cpu-usage-summary.png)

     Veri toplama etkinleştirildiğinde, kayıt düğmesi kırmızı bir daire görüntüler.

     **CPU profilini kaydet**' i seçtiğinizde, Visual Studio işlevlerinizi kaydetmeye başlar ve ne kadar sürer ve ayrıca örnekleme oturumunun belirli kesimlerine odaklanmak için kullanabileceğiniz bir zaman çizelgesi grafiği sağlar. Bu toplanan verileri yalnızca, uygulamanız bir kesme noktasında durdurulduğunda görüntüleyebilirsiniz.

6. Uygulamayı, ikinci bir kesme noktasına kadar çalıştırmak için F5'e basın.

     Şimdi, artık performans verileri bölge için özellikle uygulamanız iki kesme noktaları arasında çalışan kod için var.

     Profil Oluşturucu, iş parçacığı veri hazırlama başlar. Bitmesini bekleyin.

     CPU kullanımı aracı raporda görüntüler **CPU kullanımı** sekmesi.

     Bu noktada, verileri çözümlemek başlayabilirsiniz.

## <a name="step-2-analyze-cpu-usage-data"></a>2\. Adım: CPU kullanım verilerini çözümleme

CPU kullanımı altında işlevler listesini inceleyerek, en fazla çalışmayı yapan işlevleri tanımlama ve ardından her birine daha yakından bakalım alma verilerinizi analiz etmeye başlamanızı öneririz.

1. İşlev listesinde, en fazla çalışmayı yapan işlevler inceleyin.

     ![Tanılama araçları CPU kullanımı sekmesi](../profiling/media/quickstart-cpu-usage-cpu-aspnet.png)

    > [!TIP]
    > İşlevler, en fazla çalışmayı yapan olanlar başlayarak sırayla listelenir (çağrı sırayla olmadıklarını). Bu, uzun çalışan işlevleri hızlıca belirlemenize yardımcı olur.

2. İşlev listesinde, `MyProfilingApp_MVC.Models.ServerClass::GetNumber` işlevine çift tıklayın.

    İşleve çift tıkladığınızda, **çağıran/çağrılan** görünümü sol bölmede açılır.

    ![Tanılama araçları arayan/çağrılan görünümü](../profiling/media/quickstart-cpu-usage-caller-callee-aspnet.png)

    Bu görünümde, seçilen işlev başlıkta ve **geçerli işlev** kutusunda (`ServerClass::GetNumber`Bu örnekte) görüntülenir. Geçerli işlevi çağıran işleve sol altında gösterilen **işlevi çağırma**, ve geçerli işlev tarafından çağrılan tüm işlevleri gösterilir **çağrılan işlevlerin** sağdaki kutuya. (Geçerli işlevin değiştirmek için ya da kutusunu seçebilirsiniz.)

    Bu görünüm, toplam süre (ms) ve genel uygulamayı işlevi tamamlamak için gerçekleştirdiği zaman yüzdesini gösterir.

    **İşlev gövdesi** ayrıca süresi (ve zamanı yüzdesi) işlev gövdesinde harcanan süre hariç toplam miktarı harcanan içinde arama ve işlevlerin çağrılma gösterilmektedir. (Bu çizimde, işlev gövdesinde 2220 MS 'tan 2235 tanesi harcanmış ve kalan süre (< 20 ms) Bu işlev tarafından çağrılan harici kodda harcanmıştı). Gerçek değerler ortamınıza bağlı olarak farklı olacaktır.

    > [!TIP]
    > Yüksek değerleri **işlev gövdesi** işlevin kendisi içinde bir performans engelini işaret edebilir.

## <a name="next-steps"></a>Sonraki adımlar

- [Bellek kullanımını analiz etme](../profiling/memory-usage.md)performans sorunlarını tanımlamak için.
- [CPU kullanımını analiz etme](../profiling/cpu-usage.md) CPU kullanım aracı hakkında daha ayrıntılı bilgiler.
- Bir hata ayıklayıcı ekli veya çalışan bir uygulamayı hedefleyerek CPU kullanımını analiz etme-daha fazla bilgi için bkz. hata [ayıklayıcı ile veya olmayan profil oluşturma araçlarında](../profiling/running-profiling-tools-with-or-without-the-debugger.md) [hata ayıklama olmadan profil oluşturma verileri toplama](../profiling/running-profiling-tools-with-or-without-the-debugger.md#collect-profiling-data-without-debugging) .

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio profil oluşturma](../profiling/index.yml)
- [Araçlar profil oluşturmaya ilk bakış](../profiling/profiling-feature-tour.md)
