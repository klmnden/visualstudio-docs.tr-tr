---
title: "Nasıl yapılır: Dll 'ler için C++ birim testleri yazma"
ms.date: 06/13/2019
ms.topic: conceptual
ms.author: mblome
manager: markl
ms.workload:
- cplusplus
author: mikeblome
ms.openlocfilehash: 1e9e77cd3b6cd02810873127bf9173eac80d7e74
ms.sourcegitcommit: 044bb54cb4552c8f4651feb11d62e52726117e75
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68661905"
---
# <a name="how-to-write-unit-tests-for-c-dlls"></a>Nasıl yapılır: Dll 'ler için C++ birim testleri yazma

Bu izlenecek yol, test-First yöntemini C++ kullanarak yerel dll 'nin nasıl geliştirileceği açıklanmaktadır. Temel adımlar aşağıdaki gibidir:

1. [Yerel bir test projesi oluşturun](#create_test_project). Test projesi, DLL projesiyle aynı çözümde bulunur.

2. [BIR DLL projesi oluşturun](#create_dll_project). Bu izlenecek yol yeni bir DLL oluşturur, ancak var olan bir DLL 'yi test etme yordamı benzerdir.

3. [DLL işlevlerini testlere görünür hale getirin](#make_functions_visible).

4. [Testleri](#iterate)yinelemeli olarak güçlendirin. Kodun geliştirilmesi testlerin yaptığı bir "kırmızı yeşil-yeniden düzenleme" döngüsünün kullanılması önerilir.

5. [Başarısız testlerde hata ayıklayın](#debug). Testleri hata ayıklama modunda çalıştırabilirsiniz.

6. [Testleri değişmeden tutarken yeniden düzenleme](#refactor). Yeniden düzenleme, dış davranışını değiştirmeden kodun yapısını iyileştirmek anlamına gelir. Bu kodu, kodun performansını, genişletilebilirliğini veya okunabilirliğini geliştirmek için yapabilirsiniz. Amaç, davranışı değiştirmediğinden, kodda yeniden düzenleme değişikliği yaparken testleri değiştirmeyin. Testler, yeniden düzenleme sırasında hata tanıtmadığınızdan emin olmanıza yardımcı olur.

7. [Kapsama bakın](using-code-coverage-to-determine-how-much-code-is-being-tested.md). Birim testleri, kodunuzun daha fazlasını yaparken daha kullanışlı olur. Kodunuzun hangi bölümlerinin test tarafından kullanıldığını keşfedebilirsiniz.

8. [Birimleri dış kaynaklardan yalıtın](using-stubs-to-isolate-parts-of-your-application-from-each-other-for-unit-testing.md). Genellikle, bir DLL, diğer dll 'Ler, veritabanları veya uzak alt sistemler gibi geliştirmekte olduğunuz sistem bileşenlerine bağımlıdır. Her birimi bağımlılıklarından yalıtılmış olarak test etmek yararlı olur. Dış bileşenler, testlerin yavaş çalışmasını sağlayabilir. Geliştirme sırasında diğer bileşenler tamamlanmamış olabilir.

## <a name="create_test_project"></a>Yerel birim testi projesi oluştur

1. Üzerinde **dosya** menüsünde seçin **yeni** > **proje**.

     **Visual Studio 2017 ve öncesi**: **Yüklü** > **Şablonlar** **görsel C++**  **testini genişletin**. >   > 
     **Visual Studio 2019**: **Dil** ayarla C++ ve arama kutusuna "test" yazın.

     **Yerel birim testi proje** şablonunu veya tercih ettiğiniz yüklü çerçeveyi seçin. Google Test veya Boost. test gibi başka bir şablon seçerseniz, bazı ayrıntılar farklı olsa da temel ilkeler aynı olur.

     Bu izlenecek yolda, test projesi adlandırılır `NativeRooterTest`.

2. Yeni projede, **UnitTest1. cpp** ' yi inceleyin

     ![Test&#95;sınıfı ve test&#95;yöntemiyle test projesi](../test/media/utecpp2.png)

     Dikkat edin:

    - Her bir testi kullanılarak tanımlanmış `TEST_METHOD(YourTestName){...}`.

         Geleneksel işlev imzası yazmanız gerekmez. İmza TEST_METHOD makro tarafından oluşturulur. Makro, void döndüren bir örnek işlevi oluşturur. Ayrıca, test yöntemi hakkında bilgi döndüren statik bir işlev oluşturur. Test Gezgini, yöntem bulmak bu bilgileri sağlar.

    - Test yöntemleri, sınıflara kullanarak gruplanır `TEST_CLASS(YourClassName){...}`.

         Testler çalıştırıldığında, her test sınıfının bir örneği oluşturulur. Test yöntemlerini belirtilmemiş sırayla çağrılır. Önce ve sonra her bir modül, sınıf veya yöntemi çağıran özel yöntemi tanımlayabilirsiniz.

3. Testin test Gezgini 'nde çalıştığını doğrulayın:

    1. Bazı test kodu ekleyin:

        ```cpp
        TEST_METHOD(TestMethod1)
        {
            Assert::AreEqual(1,1);
        }
        ```

         Dikkat `Assert` sınıfı yöntemleri test sonuçlarında doğrulamak için kullanabileceğiniz birkaç statik yöntemler sağlar.

    2. **Test** menüsünde**tüm testleri** **Çalıştır** > ' ı seçin.

         Test derlemeleri ve çalıştırmaları.

         **Test Gezgini** görüntülenir.

         Test **geçilen testler**altında görünür.

         ![Başarılı bir test ile birim test Gezgini](../test/media/utecpp04.png)

## <a name="create_dll_project"></a>DLL projesi oluşturma

::: moniker range="vs-2019"

Aşağıdaki adımlarda, Visual Studio 2019 ' de bir DLL projesi oluşturma gösterilmektedir.

1. C++ **Windows Masaüstü Sihirbazı 'nı**kullanarak bir proje oluşturun: **Çözüm Gezgini** çözüm adına sağ tıklayın ve**Yeni proje** **Ekle** > ' yi seçin. **Dili** olarak C++ ayarlayın ve arama kutusuna "Windows" yazın. Sonuçlar listesinden **Windows Masaüstü Sihirbazı** ' nı seçin.

     Bu kılavuzda, proje adlandırılır `RootFinder`.

2. **Oluştur**'a basın. Sonraki iletişim kutusunda, **uygulama türü** altında **dinamik bağlantı kitaplığı (dll)** öğesini seçin ve ayrıca **sembolleri dışarı aktar**' ı işaretleyin.

     **Sembolleri dışarı aktar** seçeneği, dışarı aktarılmış yöntemleri bildirmek için kullanabileceğiniz, kullanışlı bir makro oluşturur.

     ![C++DLL ve dışa aktarma sembolleri için ayarlanan proje Sihirbazı](../test/media/vs-2019/windows-desktop-project-dll.png)

3. Principal *. h* dosyasında bir dışarıya aktarılmış işlev bildirin:

     ![API makroları ile yeni DLL kod projesi ve. h dosyası](../test/media/utecpp07.png)

     Bildirimci `__declspec(dllexport)` , sınıfın genel ve korumalı üyelerinin dll dışında görünür olmasına neden olur. Daha fazla bilgi için bkz. [ C++ sınıflarda dllimport ve dllexport kullanma](/cpp/cpp/using-dllimport-and-dllexport-in-cpp-classes).

4. Principal *. cpp* dosyasında, işlev için en az bir gövde ekleyin:

    ```cpp
        // Find the square root of a number.
        double CRootFinder::SquareRoot(double v)
        {
            return 0.0;
        }
    ```

::: moniker-end

::: moniker range="vs-2017"

Aşağıdaki adımlarda, Visual Studio 2017 ' de bir DLL projesi oluşturma gösterilmektedir.

1. C++ **Win32 Proje** şablonunu kullanarak bir proje oluşturun.

     Bu kılavuzda, proje adlandırılır `RootFinder`.

2. Win32 uygulama Sihirbazı 'nda **DLL** 'yi seçin ve **sembolleri dışarı aktarın** .

     **Sembolleri dışarı aktar** seçeneği, dışarı aktarılmış yöntemleri bildirmek için kullanabileceğiniz, kullanışlı bir makro oluşturur.

     ![C++DLL ve dışa aktarma sembolleri için ayarlanan proje Sihirbazı](../test/media/utecpp06.png)

3. Principal *. h* dosyasında bir dışarıya aktarılmış işlev bildirin:

     ![API makroları ile yeni DLL kod projesi ve. h dosyası](../test/media/utecpp07.png)

     Bildirimci `__declspec(dllexport)` , sınıfın genel ve korumalı üyelerinin dll dışında görünür olmasına neden olur. Daha fazla bilgi için bkz. [ C++ sınıflarda dllimport ve dllexport kullanma](/cpp/cpp/using-dllimport-and-dllexport-in-cpp-classes).

4. Principal *. cpp* dosyasında, işlev için en az bir gövde ekleyin:

    ```cpp
        // Find the square root of a number.
        double CRootFinder::SquareRoot(double v)
        {
            return 0.0;
        }
    ```

::: moniker-end

## <a name="make_functions_visible"></a>DLL projesine test projesi için birkaç

1. DLL projesini test projesinin proje başvurularına ekleyin:

   1. ' Nde test proje düğümüne sağ **Çözüm Gezgini** ve **Ekle** > **başvuru**.

   2. **Başvuru Ekle** iletişim kutusunda, DLL projesini seçin ve **Ekle**' yi seçin.

        ![C++Proje Özellikleri | Yeni Başvuru Ekle](../test/media/utecpp09.png)

2. Asıl birim testi *. cpp* dosyasında, dll kodunun *. h* dosyasını dahil edin:

   ```cpp
   #include "..\RootFinder\RootFinder.h"
   ```

3. İçe aktarılmış işlevi kullanan temel bir test ekleyin:

   ```cpp
   TEST_METHOD(BasicTest)
   {
      CRootFinder rooter;
      Assert::AreEqual(
         // Expected value:
         0.0,
         // Actual value:
         rooter.SquareRoot(0.0),
         // Tolerance:
         0.01,
        // Message:
        L"Basic test failed",
        // Line number - used if there is no PDB file:
        LINE_INFO());
   }
   ```

4. Çözümü oluşturun.

    Yeni test, **Test Gezgini**'nde görünür.

5. İçinde **Test Gezgini**, seçin **tümünü Çalıştır**.

    ![Birim test Gezgini &#45; temel testi geçildi](../test/media/utecpp10.png)

   Test ve kod projelerini ayarlama sahiptir ve doğrulandı, kod projesinde işlevleri çalıştırmak testlerini çalıştırabilirsiniz. Şimdi gerçek test ve kod yazmaya başlayabilirsiniz.

## <a name="iterate"></a> Yinelemeli olarak testleri genişletme ve onları geçirin

1. Yeni bir test ekleyin:

    ```cpp
    TEST_METHOD(RangeTest)
    {
      CRootFinder rooter;
      for (double v = 1e-6; v < 1e6; v = v * 3.2)
      {
        double actual = rooter.SquareRoot(v*v);
        Assert::AreEqual(v, actual, v/1000);
      }
    }
    ```

    > [!TIP]
    > Geçmiş olan testleri değiştirmemenizi öneririz. Bunun yerine, yeni test Ekle, kod testin başarılı olması için güncelleştirin ve ardından başka bir test ekleyin ve benzeri.
    >
    > Kullanıcılarınızın gereksinimlerine değiştirdiğinizde, artık doğru testleri devre dışı bırakın. Yeni testler yazmak ve bunları teker teker artımlı aynı şekilde çalışır duruma getirin.

2. Çözümü oluşturun ve ardından **Test Gezgini**' nde **Tümünü Çalıştır**' ı seçin.

     Yeni test başarısız olur.

     ![RangeTest başarısız](../test/media/ute_cpp_testexplorer_rangetest_fail.png)

    > [!TIP]
    > Hemen yazdıktan sonra her testin başarısız olduğunu doğrulayın. Bu, hiçbir zaman başarısız bir test yazma kolay onlardan yardımcı olur.

3. Yeni testin başarılı olması için DLL kodunuzu geliştirin:

    ```cpp
    #include <math.h>
    ...
    double CRootFinder::SquareRoot(double v)
    {
      double result = v;
      double diff = v;
      while (diff > result/1000)
      {
        double oldResult = result;
        result = result - (result*result - v)/(2*result);
        diff = abs (oldResult - result);
      }
      return result;
    }
    ```

4. Çözümü derleyin ve ardından **Test Gezgini**, seçin **tümünü Çalıştır**.

     Her iki testler başarılı.

     ![Birim test Gezgini &#45; Aralık testi geçti](../test/media/utecpp12.png)

    > [!TIP]
    > Aynı anda testleri bir ekleyerek kod geliştirin. Tüm testler her yinelemeden sonra başarılı olduğundan emin olun.

## <a name="debug"></a> Başarısız bir test hatalarını ayıklama

1. Başka bir test ekleyin:

    ```cpp
    #include <stdexcept>
    ...
    // Verify that negative inputs throw an exception.
    TEST_METHOD(NegativeRangeTest)
    {
      wchar_t message[200];
      CRootFinder rooter;
      for (double v = -0.1; v > -3.0; v = v - 0.5)
      {
        try
        {
          // Should raise an exception:
          double result = rooter.SquareRoot(v);

          _swprintf(message, L"No exception for input %g", v);
          Assert::Fail(message, LINE_INFO());
        }
        catch (std::out_of_range ex)
        {
          continue; // Correct exception.
        }
        catch (...)
        {
          _swprintf(message, L"Incorrect exception for %g", v);
          Assert::Fail(message, LINE_INFO());
        }
      }
    }
    ```

2. Çözümü derleyin ve **Tümünü Çalıştır**' ı seçin.

3. Başarısız testi açın (veya çift tıklatın).

     Onaylama başarısız vurgulanır. Hata iletisi ayrıntı bölmesinde görünür **Test Gezgini**.

     ![NegativeRangeTests başarısız oldu](../test/media/ute_cpp_testexplorer_negativerangetest_fail.png)

4. Testin neden başarısız görmek için işlev adım:

    1. SquareRoot işlevinin başlangıcında bir kesme noktası ayarlayın.

    2. Başarısız test kısayol menüsünde **seçilen Testlerde Hata Ayıkla**.

         Kesme noktasında çalıştırma sona erdiğinde, kodda adım adım.

5. Geliştirdiğiniz işleve kod ekleyin:

    ```cpp

    #include <stdexcept>
    ...
    double CRootFinder::SquareRoot(double v)
    {
        // Validate parameter:
        if (v < 0.0)
        {
          throw std::out_of_range("Can't do square roots of negatives");
        }

    ```

6. Artık tüm sınamaları geçmesi.

   ![Tüm testler başarılı](../test/media/ute_ult_alltestspass.png)

::: moniker range="vs-2017"

> [!TIP]
> Bireysel testlerin herhangi bir sırada çalıştırılmasını engelleyen bir bağımlılığı yoksa, araç ![çubuğundaki Ute&#95;paralellicon&#45;küçük](../test/media/ute_parallelicon-small.png) geçiş düğmesi ile paralel test yürütmeyi etkinleştirin. Bu durum, tüm testleri çalıştırmak için geçen süre önemli ölçüde azaltabilir.

::: moniker-end

::: moniker range=">=vs-2019"

> [!TIP]
> Bireysel testlerin herhangi bir sırada çalıştırılmasını engelleyen bir bağımlılığı yoksa, araç çubuğunun ayarlar menüsünde paralel test yürütme ' yi açın. Bu durum, tüm testleri çalıştırmak için geçen süre önemli ölçüde azaltabilir.

::: moniker-end

## <a name="refactor"></a> Testleri değiştirmeden kodu yeniden düzenleme

1. SquareRoot işlevinde merkezi hesaplamayı kolaylaştırın:

    ```cpp
    // old code:
    //   result = result - (result*result - v)/(2*result);
    // new code:
         result = (result + v/result)/2.0;

    ```

2. Bir hata sunduğunuzdan emin olmak için çözümü derleyin ve **Tümünü Çalıştır**' ı seçin.

    > [!TIP]
    > Uygun bir birim testi kümesi, kodu değiştirirken hata sunmaabileceğinizden emin olmanızı sağlar.
    >
    > Diğer değişikliklerden ayrı düzenlemesi tutun.

## <a name="next-steps"></a>Sonraki adımlar

- **Yalıtımı.** Çoğu dll veritabanları ve diğer dll 'Ler gibi diğer alt sistemlere bağımlıdır. Bu diğer bileşenler genellikle paralel olarak geliştirilmiştir. Diğer bileşenler henüz kullanılamadığı sürece birim testi gerçekleştirilmesine izin vermek için, sahte veya

- **Derleme doğrulama testleri.** Ekip oluşturma sunucusunda, belirlenen aralıklarda testlerin gerçekleştirilmesini sağlayabilirsiniz. Bu, birkaç takım üyesinin çalışması tümleştirildiğinde hataların tanıtılmamasını sağlar.

- **İade testleri.** Her bir takım üyesinin, kaynak denetimine kodu denetlemesi için bazı testlerin gerçekleştirilmesini zorunlu hale getirebilirsiniz. Genellikle bu, tüm yapı doğrulama testleri kümesinin bir alt kümesidir.

   Ayrıca, en düşük kod kapsamı düzeyini de kullanabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [Mevcut C++ uygulamalara birim testleri ekleme](../test/how-to-use-microsoft-test-framework-for-cpp.md)
- [Microsoft.VisualStudio.TestTools.CppUnitTestFramework Kullanma](how-to-use-microsoft-test-framework-for-cpp.md)
- [Yerel kodda hata ayıklama](../debugger/debugging-native-code.md)
- [İzlenecek yol: Dinamik bağlantı kitaplığı oluşturma ve kullanma (C++)](/cpp/build/walkthrough-creating-and-using-a-dynamic-link-library-cpp)
- [İçeri ve dışarı aktarma](/cpp/build/importing-and-exporting)
