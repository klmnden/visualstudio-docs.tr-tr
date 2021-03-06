---
title: C++ DLL'leri için birim testleri yazma
ms.date: 05/01/2019
ms.topic: conceptual
ms.author: mblome
manager: markl
ms.workload:
- cplusplus
author: mikeblome
ms.openlocfilehash: f9f17b129b0d5d85abacb0723b57703db74bcbea
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926663"
---
# <a name="write-unit-tests-for-c-dlls-in-visual-studio"></a>Visual Studio'da C++ DLL'leri için birim testleri yazma

DLL kodu, test etmek istediğiniz işlevleri dışa aktarır, bağlı olarak test etmek için birkaç yolu vardır. Aşağıdaki yöntemlerden birini seçin:

**Birim testleri yalnızca DLL 'den aktarılmış işlevleri çağırır:** [C/C++için yazma birim testlerinde](writing-unit-tests-for-c-cpp.md)açıklandığı şekilde ayrı bir test projesi ekleyin. Test projesinde DLL projesinden bir başvuru ekleyin.

Yordamına gidin [dışarı aktarılan işlevleri DLL projesinden başvurma](#projectRef).

**DLL, bir. exe dosyası olarak oluşturulmuştur:** Ayrı bir test projesi ekleyin. Bu çıkış nesnesi dosyasına bağlayın.

Yordamına gidin [testleri nesneye veya kitaplık dosyalarına bağlama](#objectRef).

**Birim testleri DLL 'den verilmeyen üye olmayan işlevleri çağırır ve DLL statik kitaplık olarak oluşturulabilir:** DLL projesini bir *. lib* dosyasına derlenmek üzere değiştirin. Test altındaki projeye başvuran ayrı bir test projesi ekleyin.

Bu yaklaşım, izin verilen olmayan üyeleri kullanabilirsiniz, ancak testleri ayrı bir projede hala devam testlerinizi avantajına sahiptir.

Yordamına gidin [DLL statik bir kitaplığa çevirme](#staticLink).

**Birim testleri, verilmeyen üye olmayan işlevleri çağırmalıdır ve kodun bir dinamik bağlantı kitaplığı (DLL) olarak oluşturulması gerekir:** Birim testlerini ürün koduyla aynı projeye ekleyin.

Yordamına gidin [aynı projede birim testleri eklemek için](#sameProject).

## <a name="create-the-tests"></a>Testleri oluşturma

### <a name="staticLink"></a> DLL statik bir kitaplığa çevirme

- Testlerinizi DLL proje tarafından dışa aktarılmaz üyeleri kullanmalıdır ve test altındaki projeye bir dinamik kitaplık olarak oluşturulduysa, bir statik kitaplığa dönüştürmeyi düşünün.

  1. İçinde **Çözüm Gezgini**, test edilen projenin kısayol menüsünde **özellikleri**. Proje **özellikleri** penceresi açılır.

  2. Seçin **yapılandırma özellikleri** > **genel**.

  3. Ayarlama **yapılandırma türü** için **statik kitaplık (.lib)** .

  Yordamı ile devam [testleri nesneye veya kitaplık dosyalarına bağlama](#objectRef).

### <a name="projectRef"></a> Dışa aktarılan DLL işlevlerinin test projesinden başvurmak için

- Ardından DLL proje test etmek istediğiniz işlevleri dışa aktarır, kod projesine test projesinden bir başvuru ekleyebilirsiniz.

  1. Yerel birim testi projesi oluşturun.

      ::: moniker range="vs-2019"

      1. Üzerinde **dosya** menüsünde seçin **yeni** > **proje**. **Yeni Proje Ekle** Iletişim kutusunda **dil** ' i ayarlayın C++ ve arama kutusuna "test" yazın. Ardından **yerel birim test projesini**seçin.

      ::: moniker-end

      ::: moniker range="vs-2017"

      1. **Dosya** menüsünde **Yeni** > **Proje** görsel>Test **birim testi C++ projesi**' ni seçin. **C++** > >

      ::: moniker-end

  1. **Çözüm Gezgini**' de, test projesine sağ tıklayın ve ardından**başvuru** **Ekle** > ' yi seçin.

  1. Seçin **projeleri**ve ardından test edilecek projeyi.

       Seçin **Ekle** düğmesi.

  1. Test projesi için Özellikler'de test edilen projenin konumunu ek içerik dizinlerine ekleyin.

       Seçin **yapılandırma özellikleri** > **VC ++ dizinleri** > **ekleme kodu dizinleri**.

       Seçin **Düzenle**ve ardından test edilen projenin üstbilgi dizinini ekleyin.

  Git [birim testleri yazma](#addTests).

### <a name="objectRef"></a> Testleri nesneye veya kitaplık dosyalarına bağlama

- DLL test etmek istediğiniz işlevleri dışa aktarmıyorsa çıktısını ekleyebilirsiniz *.obj* veya *.lib* dosyasını test projesinin bağımlılıklarına.

  1. Yerel birim testi projesi oluşturun.

      ::: moniker range="vs-2019"

      1. Üzerinde **dosya** menüsünde seçin **yeni** > **proje**. **Yeni Proje Ekle** Iletişim kutusunda **dil** ' i ayarlayın C++ ve arama kutusuna "test" yazın. Ardından **yerel birim test projesini**seçin.

      ::: moniker-end

      ::: moniker range="vs-2017"

      1. **Dosya** menüsünde **Yeni** > **Proje** görsel>Test **birim testi C++ projesi**' ni seçin. **C++** > >

      ::: moniker-end

  2. İçinde **Çözüm Gezgini**, test projesinin kısayol menüsünde **özellikleri**.

  3. Seçin **yapılandırma özellikleri** > **bağlayıcı** > **giriş** > **ek bağımlılıklar**.

       Seçin **Düzenle**ve adını ekleyin **.obj** veya **.lib** dosyaları. Tam yol adlarını kullanmayın.

  4. Seçin **yapılandırma özellikleri** > **bağlayıcı** > **genel** > **ek kitaplık dizinleri** .

       Seçin **Düzenle**ve dizin yolunu ekleyin **.obj** veya **.lib** dosyaları. Genellikle test edilen projenin derleme klasörü içindeki yoldur.

  5. Seçin **yapılandırma özellikleri** > **VC ++ dizinleri** > **ekleme kodu dizinleri**.

       Seçin **Düzenle**ve ardından test edilen projenin üstbilgi dizinini ekleyin.

  Git [birim testleri yazma](#addTests).

### <a name="sameProject"></a> Aynı projede birim testleri eklemek için

1. Üst bilgiler ve birim testi için gerekli olan kitaplık dosyalarını içerecek şekilde ürün kodu proje özelliklerini değiştirin.

   1. İçinde **Çözüm Gezgini**, test edilen projenin kısayol menüsünde **özellikleri**. Proje **özellikleri** penceresi açılır.

   2. Seçin **yapılandırma özellikleri** > **VC ++ dizinleri**.

   3. Dahil et ve kitaplık dizinlerini düzenleyin:

       |Dizin|Özellik|
       |-|-|
       |**Ekleme kodu dizinleri** | **$(VCInstallDir)UnitTest\include;$(IncludePath)**|
       |**Kitaplık dizinleri** | **$(VCInstallDir)UnitTest\lib;$(LibraryPath)**|

2. Bir C++ birim testi dosyası ekleyin:

   - İçinde **Çözüm Gezgini**, projenin kısayol menüsünde **Ekle** > **yeni öğe** > **C++ birim testi**.

   Git [birim testleri yazma](#addTests).

## <a name="addTests"></a> Birim testleri yazma

1. Her birim testi kodu dosyasında, ekleme bir `#include` test edilen projenin üstbilgileri için bildirimi.

2. Birim testi kod dosyalarına test sınıfları ve yöntemleri ekleyin. Örneğin:

    ```cpp
    #include "stdafx.h"
    #include "CppUnitTest.h"
    #include "MyProjectUnderTest.h"
    using namespace Microsoft::VisualStudio::CppUnitTestFramework;
    namespace MyTest
    {
      TEST_CLASS(MyTests)
      {
      public:
          TEST_METHOD(MyTestMethod)
          {
              Assert::AreEqual(MyProject::Multiply(2,3), 6);
          }
      };
    }
    ```

## <a name="run-the-tests"></a>Testleri çalıştırın

1. Üzerinde **Test** menüsünde seçin **Windows** > **Test Gezgini**.

1. Testlerinizin tümünü penceresinde görünür değilse, onun düğümüne sağ tıklayarak test projesi oluşturmak **Çözüm Gezgini** seçip **derleme** veya **yeniden**.

1. İçinde **Test Gezgini**, seçin **tümünü Çalıştır**, ya da belirli testleri çalıştırmak istediğiniz seçin. Bir test etkin kesme noktaları ile hata ayıklama modunda çalıştırmak dahil, diğer seçenekler için sağ tıklayın.

## <a name="see-also"></a>Ayrıca bkz.

- [C/C++ için birim testleri yazma](writing-unit-tests-for-c-cpp.md)
- [Microsoft.VisualStudio.TestTools.CppUnitTestFramework API Reference](../test/microsoft-visualstudio-testtools-cppunittestframework-api-reference.md)
- [Yerel kodda hata ayıklama](../debugger/debugging-native-code.md)
- [İzlenecek yol: Dinamik bağlantı kitaplığı oluşturma ve kullanma (C++)](/cpp/build/walkthrough-creating-and-using-a-dynamic-link-library-cpp)
- [İçeri ve dışarı aktarma](/cpp/build/importing-and-exporting)
- [Hızlı Başlangıç: Test Gezgini ile test temelli geliştirme](../test/quick-start-test-driven-development-with-test-explorer.md)
