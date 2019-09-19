---
title: CPU kullanım verilerini çözümleme (C++)
description: CPU kullanımı Tanılama aracını C++ kullanarak uygulama performansını ölçme
ms.date: 08/06/2018
ms.topic: quickstart
f1_keywords:
- ''
helpviewer_keywords:
- Profiling Tools, quick start
- Diagnostics Tools, CPU Usage
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 2f2587d621715e6e04edade779116e22d021072c
ms.sourcegitcommit: 53bc4c11b82882ab658e34c65ae374060f823531
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71128176"
---
# <a name="quickstart-analyze-cpu-usage-data-in-visual-studio-c"></a>Hızlı Başlangıç: Visual Studio 'da CPU kullanım verilerini çözümleme (C++)

Visual Studio, uygulamanızdaki performans sorunlarını çözümlemenize yardımcı olacak birçok güçlü özellik sunar. Bu konu, temel özelliklerden bazılarını öğrenmenin hızlı bir yolunu sağlar. Burada, yüksek CPU kullanımı nedeniyle performans sorunlarını belirlemek için araca bakacağız. Tanılama araçları, yerel/C++ geliştirme ve ASP.NET dahil olmak üzere Visual Studio .NET geliştirme için desteklenir.

Tanılama hub'ı, çok sayıda çalıştırın ve tanılama oturumunuzu yönetmek için diğer bir seçenek sunar. Burada açıklanan **CPU kullanım** aracı size ihtiyacınız olan verileri sağlamıyorsa, [diğer profil oluşturma araçları](../profiling/profiling-feature-tour.md) sizin için yararlı olabilecek farklı türde bilgiler sağlar. Çoğu durumda, uygulamanızın performans sorunu, CPU, bellek, işleme kullanıcı Arabirimi veya ağ isteği süresi gibi dışında bir şey tarafından kaynaklanabilir. Tanılama hub'ı, çok sayıda kaydedin ve bu tür verilerin analiz etmek için diğer bir seçenek sunar.

Windows 8 ve üzeri, hata ayıklayıcısı ile profil oluşturma araçları çalıştırmak için gereklidir (**tanılama araçları** pencere). Windows 7 ve üzeri sürümlerde, [performans profil oluşturucuyu](../profiling/profiling-feature-tour.md)son mordıtem Aracı ' nı kullanabilirsiniz.

## <a name="create-a-project"></a>Proje oluşturma

1. Visual Studio 'da **Dosya** > **Yeni proje**' yi seçin.

2. Altında **Visual C++** , seçin **Windows Masaüstü**seçip Ortadaki bölmeden **Windows konsol uygulaması**.

    Görmüyorsanız **Windows konsol uygulaması** proje şablonu, tıklayın **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu. Visual Studio Yükleyicisi'ni başlatır. Seçin **C++ ile masaüstü geliştirme** iş yükü, ardından **Değiştir**.

3. **Diagnostics_Get_Started_Native** gibi bir ad yazın ve **Tamam**' a tıklayın.

    Visual Studio projesi oluşturur.

4. *Mydbgapp. cpp*içinde aşağıdaki kodu değiştirin

    ```c++
    int main()
    {
        return 0;
    }
    ```

    Bu kodla (kaldırmayın `#include "stdafx.h"`):

    ```c++
    #include <iostream>
    #include <limits>
    #include <mutex>
    #include <random>
    #include <functional>

    //.cpp file code:

    static constexpr int MIN_ITERATIONS = std::numeric_limits<int>::max() / 1000;
    static constexpr int MAX_ITERATIONS = MIN_ITERATIONS + 10000;

    long long m_totalIterations = 0;
    std::mutex m_totalItersLock;

    int getNumber()
    {

        std::uniform_int_distribution<int> num_distribution(MIN_ITERATIONS, MAX_ITERATIONS);
        std::mt19937 random_number_engine; // pseudorandom number generator
        auto get_num = std::bind(num_distribution, random_number_engine);
        int random_num = get_num();

        auto result = 0;
        {
            std::lock_guard<std::mutex> lock(m_totalItersLock);
            m_totalIterations += random_num;
        }
        // we're just spinning here
        // to increase CPU usage
        for (int i = 0; i < random_num; i++)
        {
            result = get_num();
        }
        return result;
    }

    void doWork()
    {
        std::wcout << L"The doWork function is running on another thread." << std::endl;

        auto x = getNumber();
    }

    int main()
    {
        std::vector<std::thread> threads;

        for (int i = 0; i < 10; ++i) {

            threads.push_back(std::thread(doWork));
            std::cout << "The Main() thread calls this after starting the new thread" << std::endl;
        }

        for (auto& thread : threads) {
            thread.join();
        }

        return 0;
    }
    ```

## <a name="step-1-collect-profiling-data"></a>1\. Adım: Profil oluşturma verilerini topla

1. İlk olarak, `main` işlevdeki Bu kod satırında uygulamanızda bir kesme noktası ayarlayın:

    `for (int i = 0; i < 10; ++i) {`

    Kod satırının solundaki cilt paya tıklayarak bir kesme noktası ayarlayın.

2. Sonra, `main` işlevin sonundaki kapanış küme ayracı üzerinde ikinci bir kesme noktası ayarlayın:

     ![Profil oluşturma için kesme noktaları ayarla](../profiling/media/quickstart-cpu-usage-breakpoints-cplusplus.png "Profil oluşturma için kesme noktaları ayarla")

    > [!TIP]
    > İki kesme noktaları ayarlayarak veri toplamayı çözümlemek istediğiniz kod parçalarını sınırlayabilirsiniz.

3. **Tanılama araçları** pencere, siz kapatmadığınız müddetçe zaten görünür. Pencereyi ayarlayıp yeniden getirmek için tıklayın **hata ayıklama** > **Windows** > **tanılama araçlarını Göster**.

4. Tıklayın **hata ayıklama** > **hata ayıklamayı Başlat** (veya **Başlat** araç çubuğunda veya **F5**).

     Uygulamanın yüklenmesi bittiğinde, tanılama araçlarının **Özet** görünümü görüntülenir.

5. Hata ayıklayıcı duraklatıldığında, CPU kullanım verilerinin toplanmasını sağlamak için **CPU profilini kaydet**' i seçip **CPU kullanımı** sekmesini açın.

     ![Tanılama araçları CPU profilini oluşturmayı etkinleştirir](../profiling/media/quickstart-cpu-usage-summary.png "Tanılama araçları CPU profilini oluşturmayı etkinleştirir")

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

     ![Tanılama araçları CPU kullanımı sekmesinde](../profiling/media/quickstart-cpu-usage-cpu-cplusplus.png "DiagToolsCPUUsageTab")

    > [!TIP]
    > İşlevler, en fazla çalışmayı yapan olanlar başlayarak sırayla listelenir (çağrı sırayla olmadıklarını). Bu, uzun çalışan işlevleri hızlıca belirlemenize yardımcı olur.

2. İşlev listesinde, `getNumber` işlevine çift tıklayın.

    İşleve çift tıkladığınızda, **çağıran/çağrılan** görünümü sol bölmede açılır.

    ![Tanılama araçları arayan-Aranan görünümü](../profiling/media/quickstart-cpu-usage-caller-callee-cplusplus.png "DiagToolsCallerCallee")

    Bu görünümde, seçilen işlev başlıkta ve **geçerli işlev** kutusunda (`getNumber`Bu örnekte) görüntülenir. Geçerli işlevi çağıran işleve sol altında gösterilen **işlevi çağırma**, ve geçerli işlev tarafından çağrılan tüm işlevleri gösterilir **çağrılan işlevlerin** sağdaki kutuya. (Geçerli işlevin değiştirmek için ya da kutusunu seçebilirsiniz.)

    Bu görünüm, toplam süre (ms) ve genel uygulamayı işlevi tamamlamak için gerçekleştirdiği zaman yüzdesini gösterir.

    **İşlev gövdesi** ayrıca süresi (ve zamanı yüzdesi) işlev gövdesinde harcanan süre hariç toplam miktarı harcanan içinde arama ve işlevlerin çağrılma gösterilmektedir. (Bu çizimde, işlev gövdesinde 119 MS 'den 43602 tanesi harcanmış ve kalan süre bu işlev tarafından çağrılan diğer kodda harcanmıştı). Gerçek değerler ortamınıza bağlı olarak çok farklı olacaktır.

    > [!TIP]
    > Yüksek değerleri **işlev gövdesi** işlevin kendisi içinde bir performans engelini işaret edebilir.

## <a name="next-steps"></a>Sonraki adımlar

- [Bellek kullanımını analiz etme](../profiling/memory-usage.md)performans sorunlarını tanımlamak için.
- [CPU kullanımını analiz etme](../profiling/cpu-usage.md) CPU kullanım aracı hakkında daha ayrıntılı bilgiler.
- Bir hata ayıklayıcı ekli veya çalışan bir uygulamayı hedefleyerek CPU kullanımını analiz etme-daha fazla bilgi için bkz. hata [ayıklayıcı ile veya olmayan profil oluşturma araçlarında](../profiling/running-profiling-tools-with-or-without-the-debugger.md) [hata ayıklama olmadan profil oluşturma verileri toplama](../profiling/running-profiling-tools-with-or-without-the-debugger.md#collect-profiling-data-without-debugging) .

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio profil oluşturma](../profiling/index.yml)
- [Araçlar profil oluşturmaya ilk bakış](../profiling/profiling-feature-tour.md)
