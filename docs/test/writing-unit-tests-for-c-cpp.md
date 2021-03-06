---
title: C/C++ için birim testleri yazma
description: CTest, Boost. test ve Google Test dahil çeşitli test çerçeveleri kullanarak Visual Studio 'da birim testlerini yazın C++ .
ms.date: 09/27/2019
ms.topic: conceptual
ms.author: mblome
manager: markl
ms.workload:
- cplusplus
author: mikeblome
ms.openlocfilehash: 75244cc728b238a04569875ac01f1c2a3f27d336
ms.sourcegitcommit: 16175e0cea6af528e9ec76f0b94690faaf1bed30
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481913"
---
# <a name="write-unit-tests-for-cc-in-visual-studio"></a>Visual Studio'da C/C++ için birim testleri yazma

Yazma ve C++ birim testlerinizi çalıştırmak **Test Gezgini** penceresi, diğer dillerde olduğu gibi. Kullanma hakkında daha fazla bilgi için **Test Gezgini**, bkz: [Test Gezgini ile birim testleri çalıştırma](run-unit-tests-with-test-explorer.md).

> [!NOTE]
> C++ için Live Unit Testing, kodlanmış UI testleri ve Intellitest gibi bazı özellikler desteklenmez.

Visual Studio bu C++ test çerçeveleri, gereken ek hiçbir yüklemeleriyle içerir:

- Microsoft birim testi çerçevesi için C++
- Google Test
- Boost.Test
- CTest

Yüklü çerçeveleri yanı sıra, Visual Studio içinde kullanmak istediğiniz her çerçeve için kendi test bağdaştırıcısı yazabilirsiniz. Birim testleriyle bir test bağdaştırıcısı tümleştirebilirsiniz **Test Gezgini** penceresi. Çeşitli üçüncü taraf bağdaştırıcıları bulunur [Visual Studio Market](https://marketplace.visualstudio.com). Daha fazla bilgi için [üçüncü taraf birim testi çerçevelerini yükleme](install-third-party-unit-test-frameworks.md).

**Visual Studio 2017 ve üzeri (Professional ve Enterprise)**

C++ birim testi projeleri desteği [CodeLens](../ide/find-code-changes-and-other-history-with-codelens.md).

**Visual Studio 2017 ve üzeri (tüm sürümler)**

- **Google Test bağdaştırıcısı** varsayılan bileşeni olarak eklenir **C++ ile masaüstü geliştirme** iş yükü. Bir çözüme ekleyebileceğiniz, **Çözüm Gezgini**çözüm düğümündeki **Yeni Proje Ekle** sağ tıklama menüsü ve **Araçlar** > **seçenekleri**aracılığıyla yapılandırabileceğiniz seçenekler aracılığıyla bir proje şablonu vardır. Daha fazla bilgi için [nasıl yapılır: Visual Studio @ no__t-0 içinde Google Test kullanın.

- **Boost.Test** varsayılan bileşeni olarak eklenir **C++ ile masaüstü geliştirme** iş yükü. İle tümleşik **Test Gezgini** ancak şu anda proje şablonu yok, bu nedenle onu el ile yapılandırılması gerekir. Daha fazla bilgi için [nasıl yapılır: Visual Studio @ no__t-0 ' da Boost. test kullanın.

- **Ctest** desteği,  **C++ CMake araçları** bileşenine dahildir ve iş yükü **ile C++ masaüstü geliştirmenin** bir parçasıdır. Ancak, CTest henüz tam olarak tümleşiktir değil **Test Gezgini**. Daha fazla bilgi için [nasıl yapılır: Visual Studio @ no__t-0 ' da CTest kullanın.

**Visual Studio 2015 veya önceki**

Bağdaştırıcının Google Test ve Boost.Test bağdaştırıcısı uzantıları Visual Studio Market'ten indirebilirsiniz [Boost.Test için Test bağdaştırıcısı](https://marketplace.visualstudio.com/items?itemName=VisualCPPTeam.TestAdapterforBoostTest) ve [Google Test için Test bağdaştırıcısı](https://marketplace.visualstudio.com/items?itemName=VisualCPPTeam.TestAdapterforGoogleTest).

## <a name="basic-test-workflow"></a>Temel test iş akışı

Aşağıdaki bölümlerde, C++ birim testi başlamanıza yardımcı olmak için temel adımları gösterilmektedir. Temel yapılandırma, Microsoft ve Google Test çerçeveleri için çok benzer. Boost.Test el ile bir test projesi oluşturmanız gerekir.

::: moniker range="vs-2019"

### <a name="create-a-test-project-in-visual-studio-2019"></a>Visual Studio 2019 'de test projesi oluşturma

Tanımlanır ve test etmek istediğiniz kodu aynı çözümde bulunan bir veya daha fazla test projeleri içindeki testleri çalıştır. Varolan çözüme yeni bir test projesi eklemek için ndeki çözüm düğümüne sağ **Çözüm Gezgini** ve **Ekle** > **yeni proje**. **Dil** ayarla C++ ve arama kutusuna "test" yazın. Aşağıdaki çizim, **ile C++ masaüstü geliştirme** ve **UWP geliştirme** iş yükü yüklü olduğunda kullanılabilir olan test projelerini göstermektedir:

![C++VIsual Studio 2019 ' de test projeleri](media/vs-2019/cpp-new-test-project-vs2019.png)

::: moniker-end

::: moniker range="vs-2017"

### <a name="create-a-test-project-in-visual-studio-2017"></a>Visual Studio 2017 'de test projesi oluşturma

Tanımlanır ve test etmek istediğiniz kodu aynı çözümde bulunan bir veya daha fazla test projeleri içindeki testleri çalıştır. Varolan çözüme yeni bir test projesi eklemek için ndeki çözüm düğümüne sağ **Çözüm Gezgini** ve **Ekle** > **yeni proje**. Sol bölmede seçin **Visual C++ Test** ve merkez bölmesinden proje türlerinden birini seçin. Ne zaman kullanılabilir olan test projeleri aşağıdaki çizimde **C++ ile masaüstü geliştirme** iş yükü yüklenir:

![C++ Test projeleri](media/cpp-new-test-project.png)

::: moniker-end

### <a name="create-references-to-other-projects-in-the-solution"></a>Çözümdeki diğer projelere başvuruları oluşturma

Test edilecek projedeki işlevlerine erişmek test kodunuzu etkinleştirmek için test projenizde projeye bir başvuru ekleyin. ' Nde test proje düğümüne sağ **Çözüm Gezgini** ve **Ekle** > **başvuru**. Ardından iletişim kutusunda, test etmek istediğiniz projeleri seçin.

![Başvuru ekleme](media/cpp-add-ref-test-project.png)

### <a name="link-to-object-or-library-files"></a>Nesne veya kitaplık dosyalarına bağlantı

Test kodu test etmek istediğiniz işlevleri dışa aktarmazsa, output. obj veya. lib dosyalarını test projesinin bağımlılıklarına ekleyebilirsiniz. [Testleri nesne veya kitaplık dosyalarına bağlamak için](https://docs.microsoft.com/visualstudio/test/unit-testing-existing-cpp-applications-with-test-explorer?view=vs-2015#objectRef)bkz.

### <a name="add-include-directives-for-header-files"></a>Ekle #include için üst bilgi dosyaları

Sonra birim sınamanız *.cpp* ekleyin bir `#include` test etmek istediğiniz türleri ve işlevleri bildirme herhangi bir üst bilgi dosyaları yönergesi. Tür `#include "` ve seçmenize yardımcı olması için IntelliSense sonra etkinleşir. Ek üst bilgilere için yineleyin.

![Ekleme yönergelerinde](media/cpp-add-includes-test-project.png)

Kaynak dosyadaki her bir Include deyimindeki tam yolu yazmak zorunda kalmamak için, **Proje** > **özelliklerine**gerekli klasörleri ekleyebilirsiniz  > **C/C++**  > **genel** > **Ek ekleme Dizinler**.

### <a name="write-test-methods"></a>Test yöntemleri yazın

> [!NOTE]
> Bu bölüm, C/C++ için Microsoft birim testi çerçevesi için söz dizimini gösterir. Burada belgelenmiştir: [Microsoft. VisualStudio. TestTools. CppUnitTestFramework API başvurusu](microsoft-visualstudio-testtools-cppunittestframework-api-reference.md). Google Test belgeleri için bkz. [Google Test öncü](https://github.com/google/googletest/blob/master/googletest/docs/primer.md). Boost. test için bkz. [Boost test Kitaplığı: Birim test çerçevesi @ no__t-0.

*.Cpp* dosyası test projenize bir saptama sınıfı ve kodu test yazma ilişkin bir örnek olarak tanımlanan yöntemi vardır. İmzaları yöntemleri gelen bulunabilir hale TEST_CLASS ve TEST_METHOD makroları kullandığını unutmayın **Test Gezgini** penceresi.

![Ekleme yönergelerinde](media/cpp-write-test-methods.png)

TEST_CLASS ve TEST_METHOD parçası olan [Microsoft Yerel Test çerçevesi](microsoft-visualstudio-testtools-cppunittestframework-api-reference.md). **Test Gezgini** desteklenen diğer çerçeveler test yöntemlerinde benzer şekilde bulur.

Bir TEST_METHOD void döndürür. Bir test sonucu oluşturmak için statik yöntemleri kullanın. `Assert` gerçek sonuçlar, beklenen değer karşı test etmek için sınıf. Aşağıdaki örnekte, varsayalım `MyClass` alan bir oluşturucu sahip bir `std::string`. Oluşturucu beklendiği gibi sınıfı başlatır sınayabiliriz şu şekilde:

```cpp
TEST_METHOD(TestClassInit)
{
    std::string name = "Bill";
    MyClass mc(name);
    Assert::AreEqual(name, mc.GetName());
}
```

Önceki örnekte, sonucunu `Assert::AreEqual` çağrı, testin başarılı veya başarısız olup olmadığını belirler. Assert sınıfı, beklenen gerçek sonuçlar karşılaştırma için birçok yöntem içerir.

Ekleyebileceğiniz *nitelikler* yöntemleri test sahipleri, öncelik ve diğer bilgileri belirtmek için test etmek için. Ardından bu değerleri sıralama ve Gruplama testler için kullanabileceğiniz **Test Gezgini**. Daha fazla bilgi için [Test Gezgini ile birim testleri çalıştırma](run-unit-tests-with-test-explorer.md).

### <a name="run-the-tests"></a>Testleri çalıştırın

1. Üzerinde **Test** menüsünde seçin **Windows** > **Test Gezgini**. Aşağıdaki çizim bir test projesi olan testleri henüz çalıştırılmamış gösterir.

   ![Test Gezgini testleri çalıştırmadan önce](media/cpp-test-explorer.png)

   > [!NOTE]
   > CTest tümleştirme **Test Gezgini** henüz kullanıma sunulmamıştır. CMake ana menüden CTest testleri çalıştırın.

1. Testlerinizin tümünü penceresinde görünür değilse, onun düğümüne sağ tıklayarak test projesi oluşturmak **Çözüm Gezgini** seçip **derleme** veya **yeniden**.

1. İçinde **Test Gezgini**, seçin **tümünü Çalıştır**, ya da belirli testleri çalıştırmak istediğiniz seçin. Bir test etkin kesme noktaları ile hata ayıklama modunda çalıştırmak dahil, diğer seçenekler için sağ tıklayın. Tüm testleri çalıştırdıktan sonra hangi testleri geçti ve hangilerinin başarısız pencere gösterir:

![Testler çalıştıktan sonra test Gezgini](media/cpp-test-explorer-passed.png)

Başarısız testler için ileti nedenini tanılamaya yardımcı olan ayrıntılar sunar. Başarısız testi sağ tıklatın ve seçin **seçilen Testlerde Hata Ayıkla** hatanın oluştuğu fonksiyona adıma.

Kullanma hakkında daha fazla bilgi için **Test Gezgini**, bkz: [Test Gezgini ile birim testleri çalıştırma](run-unit-tests-with-test-explorer.md).

Birim testi için ilgili en iyi yöntemler için bkz. [birim testi temel bilgileri](unit-test-basics.md)

## <a name="use-codelens"></a>CodeLens kullanın

**Visual Studio 2017 ve üzeri (Professional ve Enterprise sürümleri)**

[CodeLens](../ide/find-code-changes-and-other-history-with-codelens.md) , kod düzenleyicisinden çıkmadan bir birim testinin durumunu hızlıca görmenizi sağlar. CodeLens, bir C++ birim testi projesi şu yollardan birinde için başlatabilirsiniz:

- Düzenle ve test projenizi veya çözümünüzü oluşturun.
- Proje veya çözümü yeniden oluşturun.
- Öğesinden test çalıştırma **Test Gezgini** penceresi.

Sonra **CodeLens** başlatıldı, gördüğünüz durumu simgeleri her bir birim testi üzerinde test edin.

![C++ CodeLens simgeler](media/cpp-test-codelens-icons.png)

Daha fazla bilgi edinmek veya çalıştırmak veya birim testi hata ayıklama için simgesine tıklayın:

![C++ CodeLens çalıştırma ve hata ayıklama](media/cpp-test-codelens-run-debug.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Birim testi kod](unit-test-your-code.md)
