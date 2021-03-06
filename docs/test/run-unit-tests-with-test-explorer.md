---
title: Test Gezgini ile birim testlerini çalıştırma ve hata ayıklama
description: Visual Studio 'da test Gezgini ile testlerin nasıl çalıştırılacağını öğrenin. Bu konu, derleme sonrasında otomatik test çalıştırmalarını etkinleştirme, test sonuçlarını görüntüleme, test listesini gruplandırma ve filtreleme, çalma listeleri oluşturma, testleri hata ayıklama ve test kısayollarını kullanma konularını ele alır.
ms.date: 07/29/2019
ms.topic: conceptual
f1_keywords:
- vs.unittesting.testexplorer.overview
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 27ca8a39d39fcc8b4e5ddca2cbedf72e44c6cc81
ms.sourcegitcommit: 689ba54ea14257d13031de881f5d4fe937a36f56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "71342456"
---
# <a name="run-unit-tests-with-test-explorer"></a>Test Gezgini ile birim testleri çalıştırma

Visual Studio 'dan veya üçüncü taraf birim testi projelerinden birim testlerini çalıştırmak için test Gezgini 'ni kullanın. Testleri kategoriler halinde gruplamak, test listesini filtrelemek ve testlerin çalma listelerini oluşturmak, kaydetmek ve çalıştırmak için test Gezgini ' ni de kullanabilirsiniz. Testlerde hata ayıklama yapabilir ve test performansını ve kod kapsamını çözümleyebilirsiniz.

Visual Studio hem yönetilen hem de yerel kod için Microsoft birim testi çerçeveleri içerir. Ancak, test Gezgini, test Gezgini bağdaştırıcısı uygulayan herhangi bir birim test çerçevesini de çalıştırabilir. Üçüncü taraf birim testi çerçevelerini yükleme hakkında daha fazla bilgi için bkz. [üçüncü taraf birim testi çerçeveleri yükleme](../test/install-third-party-unit-test-frameworks.md)

**Test Gezgini** , bir çözümde ve üretim kodu projelerinin parçası olan test sınıflarından birden çok test projesinin testlerini çalıştırabilir. Test projeleri, farklı birim testi çerçeveleri kullanabilir. Test altındaki kod .NET için yazıldığında, hedef kodun dilinden bağımsız olarak, test projesi de .NET ' i hedefleyen herhangi bir dilde yazılabilir. Yerel C/C++ kod projeleri, bir C++ birim test çerçevesi kullanılarak test edilmelidir. Daha fazla bilgi için [C/C++ için birim testleri yazma](writing-unit-tests-for-c-cpp.md).

## <a name="run-tests-in-test-explorer"></a>Testleri Test Gezgini'nde çalıştırma


Test projesi oluşturduğunuzda, testler Test Gezgini'nde görünür. Test Gezgini görünür değilse seçin **Test** Visual Studio menüsünde **Windows**ve ardından **Test Gezgini**.


::: moniker range="vs-2017"
![Birim Test Gezgini](../test/media/ute_failedpassednotrunsummary.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Test Gezgini](../test/media/vs-2019/test-explorer-16-2.png)
::: moniker-end

::: moniker range="vs-2017"
Çalıştırma, yazma ve testlerinizi yeniden çalıştırın, Test Gezgini sonuçları varsayılan gruplarında görüntüler **başarısız testler**, **başarılı testler**, **Atlanan testler** ve  **Testleri Çalıştır**. Test Gezgini'nin testlerinizi gruplandırma şeklini değiştirebilirsiniz.
::: moniker-end
::: moniker range=">=vs-2019"
Testlerinizi çalıştırırken, yazarken ve yeniden çalıştırdığınızda, test Gezgini sonuçları varsayılan bir **Proje**, **ad alanı**ve **sınıf**gruplandırmasında görüntüler. Test Gezgini 'nin testlerinizi gruplandırma şeklini değiştirebilirsiniz.
::: moniker-end

**Test Gezgini** araç çubuğundan testleri bulma, düzenleme ve çalıştırma işinin çoğunu yapabilirsiniz.

::: moniker range="vs-2017"
![Test Gezgini araç çubuğundan Testleri Çalıştır](../test/media/ute_toolbar.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Test Gezgini araç çubuğundan Testleri Çalıştır](../test/media/vs-2019/test-explorer-toolbar-diagram-16-2.png)
::: moniker-end

### <a name="run-tests"></a>Testleri çalıştırma

::: moniker range="vs-2017"
Tüm testler, Çözümdeki tüm testleri bir grup veya seçtiğiniz test kümesini çalıştırabilirsiniz. Aşağıdakilerden birini yapın:

- Bir çözümdeki tüm testleri çalıştırmak için tercih **tümünü Çalıştır**.

- Varsayılan bir gruptaki tüm testleri çalıştırmak için **Çalıştır** ' ı seçin ve ardından menüdeki grubu seçin.

- Çalıştırmak istediğiniz bireysel testleri seçin, seçili bir test için sağ tıklama menüsünü açın ve ardından **Seçili Testleri Çalıştır**' ı seçin.

- Bireysel testler herhangi bir sırada çalıştırılan engelleyen bağımlılık varsa, paralel test yürütme ile Aç ![ALIŞTIR&#95;parallelicon&#45;küçük](../test/media/ute_parallelicon-small.png) araç çubuğundaki iki durumlu düğme. Bu durum, tüm testleri çalıştırmak için geçen süre önemli ölçüde azaltabilir.

**Test Gezgini** penceresinin en üstündeki **geçiş/başarısızlık çubuğu** , testler çalışırken hareketlendirilir. Test çalıştırmasının sonunda, herhangi bir test başarısız olursa tüm testler başarılı veya Red durumunda, **geçiş/başarısızlık çubuğu** yeşile dönüşür.
::: moniker-end
::: moniker range=">=vs-2019"
Tüm testler, Çözümdeki tüm testleri bir grup veya seçtiğiniz test kümesini çalıştırabilirsiniz. Aşağıdakilerden birini yapın:

- Bir Çözümdeki tüm testleri çalıştırmak için **Tümünü Çalıştır** simgesini seçin.

- Varsayılan bir gruptaki tüm testleri çalıştırmak için **Çalıştır** simgesini seçin ve sonra menüdeki grubu seçin.

- Çalıştırmak istediğiniz bireysel testleri seçin, seçili bir test için sağ tıklama menüsünü açın ve ardından **Seçili Testleri Çalıştır**' ı seçin.

- Bireysel testlerin herhangi bir sırada çalıştırılmasını engelleyen bir bağımlılığı yoksa, araç çubuğunun ayarlar menüsünde paralel test yürütme ' yi açın. Bu durum, tüm testleri çalıştırmak için geçen süre önemli ölçüde azaltabilir.
::: moniker-end

### <a name="run-tests-after-every-build"></a>Her derleme sonrasında Testleri Çalıştır
::: moniker range="vs-2017"
|Düğme|Açıklama|
|-|-|
|![Yapıdan sonra çalıştırmak](../test/media/ute_runafterbuild_btn.png)|Her yerel derlemeden sonra birim testlerinizi çalıştırmak için standart menüdeki **Test** ' i seçin ve ardından **Test Gezgini** araç çubuğunda **derlemeden sonra Testleri Çalıştır** ' ı seçin.|

> [!NOTE]
> Her derleme sonrasında birim testlerini çalıştırmak, Visual Studio 2017 Enterprise veya Visual Studio 2019 gerektirir. Visual Studio 2019 ' de Community ve Professional 'a ve Enterprise 'a dahildir.
::: moniker-end
::: moniker range=">=vs-2019"
Her yerel derlemeden sonra birim testlerinizi çalıştırmak için, test Gezgini araç çubuğunda Ayarlar simgesini açın ve **derlemeden sonra Testleri Çalıştır**' ı seçin.
::: moniker-end

## <a name="view-test-results"></a>Test sonuçlarını görüntüle

Test Gezgini çalıştırma, yazma ve testlerinizi yeniden çalıştırın gibi sonuçları gruplarında görüntüler. **başarısız testler**, **başarılı testler**, **Atlanan testler** ve **çalıştırma Testleri**. Test Gezgini 'nin alt veya tarafındaki Ayrıntılar bölmesi, Test çalıştırmasının bir özetini görüntüler.

### <a name="view-test-details"></a>Test ayrıntılarını görüntüle

Tek bir testin ayrıntılarını görüntülemek için testi seçin.

::: moniker range="vs-2017"
![Test yürütme ayrıntıları](../test/media/ute_testdetails.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Test yürütme ayrıntıları](../test/media/vs-2019/test-explorer-detail.png)
::: moniker-end

Test ayrıntıları bölmesinde aşağıdaki bilgileri görüntüler:

- Kaynak dosya adı ve test yönteminin satır sayısı.

- Testin durumu.

- Test yöntemini çalıştırmak için geçen geçen süre.

Test başarısız olursa, Ayrıntılar bölmesinde de görüntüler:

- Test için birim test çerçevesi tarafından döndürülen ileti.

- Yığın izleme zaman test başarısız oldu.

### <a name="view-the-source-code-of-a-test-method"></a>Test yönteminin kaynak kodunu görüntüleme

Visual Studio düzenleyicisinde bir test yönteminin kaynak kodunu göstermek için, testi seçin ve sağ tıklama menüsünde **testi aç** ' ı seçin (klavye: **F12**).

## <a name="group-and-filter-the-test-list"></a>Test listesini gruplandırma ve filtreleme

Test Gezgini, testlerinizi önceden tanımlanmış kategoriler halinde gruplandırmanızı sağlar. Test Gezgini 'nde çalışan çoğu birim testi çerçevesi, testlerinizi gruplandırmak için kendi kategorilerinizi ve kategori/değer çiftlerini tanımlamanızı sağlar. Test özelliklerine karşılık dizeleri eşleştirerek, testlerin listesini de filtreleyebilirsiniz.

### <a name="group-tests-in-the-test-list"></a>Test listesindeki testleri gruplandırma

::: moniker range="vs-2017"
Testlerin düzenlenme şeklini değiştirmek için, **grupla** düğmesine ![Test Gezgini Grup düğmesi @ no__t-2 ' nin yanındaki aşağı oku seçin ve yeni bir gruplandırma ölçütü seçin.

![Test Gezgini 'nde kategoriye göre grup testleri](../test/media/ute_groupbycategory.png)
::: moniker-end
::: moniker range=">=vs-2019"
Test Gezgini, testlerinizi bir hiyerarşiye gruplandırmanıza olanak tanır. Varsayılan hiyerarşi gruplandırması **Proje**, **ad alanı**ve daha sonra **sınıftır**. Testlerin düzenlenme şeklini değiştirmek için **Gruplandırma ölçütü** düğmesini ![Test Gezgini grubu düğmesini @ no__t-2 ' yi seçin ve yeni bir gruplandırma ölçütü seçin.

![Test Gezgini 'nde kategoriye göre grup testleri](../test/media/vs-2019/test-explorer-groupby-162.png)

Hiyerarşi ve gruplama düzeylerini **tanımlayabilir ve sonra** tercih ettiğiniz sırada grupla seçeneklerini belirleyerek **sınıfa** göre gruplandırabilirsiniz.

![Duruma göre Gruplandır ve sonra sınıfı](../test/media/vs-2019/test-explorer-groupby-state-16-2.png)
::: moniker-end

### <a name="test-explorer-groups"></a>Test Gezgini grupları

::: moniker range="vs-2017"
|Grup|Açıklama|
|-|-----------------|
|**Süresi**|Yürütme süresine göre test grupları: **Hızlı**, **Orta**ve **yavaş**.|
|**Sonucu**|Testleri yürütme sonuçlarına göre gruplandırır: **Başarısız testler**, **Atlanan testler**, **başarılı testler**.|
|**Lerdir**|Tanımladığınız kategori/değer çiftlerine göre test grupları. Nitelik kategorilerini ve değerlerini belirten sözdizimi, birim test çerçevesi tarafından tanımlanır.|
|**Project**|Projeler adına göre test grupları.|
::: moniker-end
::: moniker range=">=vs-2019"
|Grup|Açıklama|
|-|-----------------|
|**Süresi**|Testleri yürütme zamanına göre gruplandırır: **Hızlı**, **Orta**ve **yavaş**.|
|**State**|Testleri yürütme sonuçlarına göre gruplandırır: **Başarısız testler**, **Atlanan testler**, **başarılı testler**, **çalıştırılmadı**|
|**Hedef Çerçeve** | Testleri, projeleri hedeflerine göre gruplandırır |
|**Namespace**|Testleri içerilen ad alanına göre gruplandırır.|
|**Project**|Testleri içeren proje tarafından gruplandırır.|
|**Sınıfı**|Testleri içerilen sınıfa göre gruplandırır.|
::: moniker-end

### <a name="traits"></a>Lerdir

Bir nitelik genellikle kategori adı/değer çiftidir, ancak tek bir kategori de olabilir. Nitelikler, birim test çerçevesi tarafından test yöntemi olarak tanımlanan yöntemlere atanabilir. Bir birim test çerçevesi, nitelik kategorilerini tanımlayabilir. Kendi Kategori ad/değer çiftlerinizi tanımlamak için nitelik kategorilerine değerler ekleyebilirsiniz. Nitelik kategorilerini ve değerlerini belirten sözdizimi, birim test çerçevesi tarafından tanımlanır.

**Yönetilen kod için Microsoft birim testi çerçevesindeki nitelikler**

Yönetilen uygulamalar için Microsoft birim testi çerçevesinde, <xref:Microsoft.VisualStudio.TestTools.UnitTesting.TestPropertyAttribute> özniteliğinde bir nitelik ad/değer çifti tanımlarsınız. Test çerçevesi aşağıdaki önceden tanımlı nitelikleri de içerir:

|Nitelik|Açıklama|
|-|-----------------|
|<xref:Microsoft.VisualStudio.TestTools.UnitTesting.OwnerAttribute>|Sahip kategorisi, birim test çerçevesi tarafından tanımlanır ve sahibin dize değerini sağlamanızı gerektirir.|
|<xref:Microsoft.VisualStudio.TestTools.UnitTesting.PriorityAttribute>|Öncelik kategorisi, birim test çerçevesi tarafından tanımlanır ve öncelik için bir tamsayı değeri sağlamanızı gerektirir.|
|<xref:Microsoft.VisualStudio.TestTools.UnitTesting.TestCategoryAttribute>|TestCategory özniteliği değer olmadan bir kategori sağlamanıza olanak sağlar.|
|<xref:Microsoft.VisualStudio.TestTools.UnitTesting.TestPropertyAttribute>|TestProperty özniteliği nitelik kategori/değer çiftini tanımlamanızı sağlar.|


**İçin Microsoft birim testi çerçevesindeki niteliklerC++**

[Için C++Microsoft birim testi çerçevesini kullanma ](how-to-use-microsoft-test-framework-for-cpp.md)konusuna bakın.

## <a name="create-custom-playlists"></a>Özel çalma listeleri oluşturma

::: moniker range="vs-2017"
Çalıştırmak veya bir grup olarak görüntülemek istediğiniz testlerin listesini oluşturabilir ve kaydedebilirsiniz. Bir çalma listesi seçtiğinizde, listedeki testler test Gezgini 'nde görüntülenir. Birden fazla çalma listesine bir test ekleyebilirsiniz ve varsayılan **Tüm testler** çalma listesini seçtiğinizde projenizdeki tüm testler kullanılabilir.

![Bir çalma listesi seçin](../test/media/ute_playlist.png)

**Bir çalma listesi oluşturmak için**, test Gezgini 'nde bir veya daha fazla test seçin. Sağ tıklama menüsünde,  > **NewPlaylist** **listesine ekle**' yi seçin. Dosyayı **Yeni çalma listesi oluştur** iletişim kutusunda belirttiğiniz ad ve konuma kaydedin.

**Bir çalma listesine test eklemek için**, test Gezgini 'nde bir veya daha fazla test seçin. Sağ tıklama menüsünde, **çalma listesine ekle**' yi seçin ve ardından testleri eklemek istediğiniz çalma listesini seçin.

**Bir çalma listesi açmak için**, Visual Studio menüsünden **Test** > **çalma** listesini seçin ve son kullanılan çalma listeleri listesinden seçim yapın veya çalma listesini **Aç** ' ı seçerek şarkı listesinin adını ve konumunu belirtin.

Bireysel testler herhangi bir sırada çalıştırılan engelleyen bağımlılık varsa, paralel test yürütme ile Aç ![ALIŞTIR&#95;parallelicon&#45;küçük](../test/media/ute_parallelicon-small.png) araç çubuğundaki iki durumlu düğme. Bu durum, tüm testleri çalıştırmak için geçen süre önemli ölçüde azaltabilir.
::: moniker-end
::: moniker range=">=vs-2019"
Çalıştırmak veya bir grup olarak görüntülemek istediğiniz testlerin listesini oluşturabilir ve kaydedebilirsiniz. Bir çalma listesi seçtiğinizde, listedeki testler yeni bir test Gezgini sekmesinde görüntülenir. Birden fazla çalma listesine bir test ekleyebilirsiniz.

**Bir çalma listesi oluşturmak için**, test Gezgini 'nde bir veya daha fazla test seçin. Sağ tıklama menüsünde, @no__t Yapılacaklar **listesine ekle**' yi seçin,**Yeni çalma listesi**' ni seçin.

![Çalma listesi oluşturma](../test/media/vs-2019/test-explorer-playlist-16-2.png)

Yeni bir test Gezgini sekmesinde çalma listesi açılır. Bu çalma listesini bir kez kullanarak atabilir veya çalma listesi penceresinin araç çubuğunda **Kaydet** düğmesine tıklayabilir ve sonra da bir ad ve konum seçerek çalma listesini kaydedebilirsiniz.

![Çalma listesi ayrı test Gezgini sekmesinde açılıyor](../test/media/vs-2019/test-explorer-playlist-tab-16-2.png)

**Bir çalma listesi oluşturmak için**, test Gezgini 'nde bir veya daha fazla test seçin. Sağ tıklayın ve @no__t Yapılacaklar **listesine ekle**' yi seçin-1**Yeni çalma listesi**.

**Bir çalma listesi açmak için**, Visual Studio araç çubuğunda çalma listesi simgesini seçin ve menüden önceden kaydedilmiş bir çalma listesi dosyası seçin.
::: moniker-end

::: moniker range=">=vs-2019"
### <a name="test-explorer-columns"></a>Test Gezgini sütunları

[Gruplar](#test-explorer-groups) , test Gezgini 'nde nitelik, yığın Izleme, hata Iletisi ve tam ad gibi sütunlar olarak da kullanılabilir. Çoğu sütun varsayılan olarak görünmez ve gördüğünüz sütunları ve görünecekleri sırayı özelleştirebilirsiniz.

![Duruma göre Gruplandır ve sonra sınıfı](../test/media/vs-2019/test-explorer-columns-16-2.png)

### <a name="filter-sort-and-rearrange-test-columns"></a>Test sütunlarını filtreleme, sıralama ve yeniden düzenleme

Sütunlar filtrelenebilir, sıralanabilir ve yeniden düzenlenebilir.
* Belirli nitelikleri filtrelemek için nitelikler sütununun en üstündeki filtre simgesine tıklayın.

  ![Sütun filtresi](../test/media/vs-2019/test-explorer-filter-column-16-2.png)

* Sütunların sırasını değiştirmek için, bir sütun başlığına tıklayın ve sola veya sağa sürükleyin.

* Bir sütunu sıralamak için sütun başlığına tıklayın. Tüm sütunlar sıralanmayabilir. Ayrıca, **SHIFT** tuşunu basılı tutarak ve ek bir sütun başlığına tıklayarak ikincil bir sütuna göre sıralama yapabilirsiniz.

  ![Sütun sıralaması](../test/media/vs-2019/test-explorer-sort-column-16-2.png)
::: moniker-end

## <a name="search-and-filter-the-test-list"></a>Test listesini arama ve filtreleme

Ayrıca, görüntülediğiniz ve çalıştırdığınız projelerinizde test yöntemlerini sınırlandırmak için test Gezgini arama filtrelerini de kullanabilirsiniz.

**Test Gezgini** arama kutusuna bir dize yazdığınızda ve **ENTER**' u seçtiğinizde, test listesi yalnızca tam adları dizeyi içeren testleri görüntüleyecek şekilde filtrelenir.

Farklı ölçütlere göre filtrelemek için:

1. Arama kutusunun sağındaki açılan listeyi açın.

2. Yeni bir ölçüt seçin.

3. Tırnak işaretleri arasında filtre değeri girin. Dizeyi içeren bir eşleşme yerine tam eşleşme aramak istiyorsanız, iki nokta (:) yerine bir eşittir işareti (=) kullanın.

::: moniker range="vs-2017"
![Test Gezgini 'nde testleri filtrele](../test/media/ute_filtertestlist.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Test Gezgini 'nde testleri filtrele](../test/media/vs-2019/test-explorer-search-filter-16-2.png)
::: moniker-end

> [!NOTE]
> Aramalar büyük/küçük harfe duyarlıdır ve belirtilen dizeyle ölçüt değerinin herhangi bir bölümüyle eşleşir.

::: moniker range="vs-2017"
|Leyicisini|Açıklama|
|-|-----------------|
|**Nitelik**|Hem nitelik kategorisini hem de eşleşme değerlerini arar. Nitelik kategorilerini ve değerlerini belirten sözdizimi, birim test çerçevesi tarafından tanımlanır.|
|**Project**|Test projesi adlarını eşleşmeler için arar.|
|**Hata Iletisi**|Eşleşmeler için başarısız Onaylamalar tarafından döndürülen Kullanıcı tanımlı hata iletilerini arar.|
|**Dosya yolu**|Test kaynak dosyalarının tam dosya adını eşleşmeler için arar.|
|**Tam nitelikli ad**|Test ad alanları, sınıflar ve yöntemlerin tam adını eşleşmeler için arar.|
|**Çıktı**|Standart çıkış (STDOUT) veya standart hata (stderr) ile yazılan Kullanıcı tanımlı hata iletilerini arar. Çıkış mesajlarını belirten sözdizimi, birim test çerçevesi tarafından tanımlanır.|
|**Sonucu**|Test Gezgini kategori adlarını eşleşmeler için arar: **Başarısız testler**, **Atlanan testler**, **başarılı testler**.|
::: moniker-end
::: moniker range=">=vs-2019"
|Leyicisini|Açıklama|
|-|-----------------|
|**State**|Test Gezgini kategori adlarını eşleşmeler için arar: **Başarısız testler**, **Atlanan testler**, **başarılı testler**.|
|**Lerdir**|Hem nitelik kategorisini hem de eşleşme değerlerini arar. Nitelik kategorilerini ve değerlerini belirten sözdizimi, birim test çerçevesi tarafından tanımlanır.|
|**Tam nitelikli ad**|Test ad alanları, sınıflar ve yöntemlerin tam adını eşleşmeler için arar.|
|**Project**|Test projesi adlarını eşleşmeler için arar.|
|**Hedef Çerçeve**|Test Gezgini kategori adlarını eşleşmeler için arar: **Başarısız testler**, **Atlanan testler**, **başarılı testler**.|
|**Namespace**|Test ad alanlarını eşleşmeler için arar.|
|**Sınıfı**|Test sınıfları adlarını eşleşmeler için arar.|
::: moniker-end

Bir filtrenin sonuçlarının bir alt kümesini dışlamak için aşağıdaki sözdizimini kullanın:

```
FilterName:"Criteria" -FilterName:"SubsetCriteria"
```

Örneğin, `FullName:"MyClass" - FullName:"PerfTest"`, adında "PerfTest" da dahil olan testler hariç "MyClass" içeren tüm testleri döndürür.

## <a name="debug-and-analyze-unit-tests"></a>Hata ayıklama ve birim testlerini analiz etme

Test Gezgini, testleriniz için hata ayıklama oturumu başlatmak için kullanabilirsiniz. Kodunuzu Visual Studio hata ayıklayıcısı ile sorunsuz bir şekilde Adımlama, İleri ve geri birim testleri ve test altındaki projeye arasında sürer. Hata ayıklamayı başlatmak için:

1. Visual Studio düzenleyicisinde, hatalarını ayıklamak istediğiniz bir veya daha fazla test yöntemlerinde kesme noktası ayarlayın.

    > [!NOTE]
    > Test yöntemleri herhangi bir sırada çalışabileceğinden, hata ayıklamak istediğiniz tüm test yöntemlerinde kesme noktalarını ayarlayın.

2. Test Gezgini 'nde test yöntemlerini seçin ve sağ tıklama menüsünde **Seçili testlerin hatalarını ayıkla** ' yı seçin.

   Hata ayıklayıcı hakkında daha fazla bilgi için bkz. [Visual Studio 'Da hata ayıklama](../debugger/debugger-feature-tour.md).

### <a name="diagnose-test-method-performance-issues"></a>Test yöntemi performans sorunlarını tanılama

Bir test yönteminin neden çok fazla zaman aldığını tanılamak için test Gezgini 'nde yöntemi seçin ve sağ tıklama menüsünde **profil seçili test** ' i seçin. Bkz. [Performans Gezgini](../profiling/performance-explorer.md).

### <a name="analyze-unit-test-code-coverage"></a>Birim testi kod kapsamını analiz etme

Visual Studio Enterprise sürümünde kullanılabilir olan Visual Studio kod kapsamı aracını kullanarak birim testleriniz tarafından test edilen ürün kodu miktarını belirleyebilirsiniz. Kod kapsamı Seçili testler ya da bir çözümdeki tüm testleri çalıştırabilirsiniz.

Bir çözümde test yöntemleri için kod kapsamını çalıştırmak için:

::: moniker range="vs-2017"

1. Üstteki menü çubuğunda **Test** ' i seçin ve ardından **kod kapsamını analiz et**' i seçin.

2. Alt menüden aşağıdaki komutlardan birini seçin:

    - **Seçili testler** , test Gezgini 'nde seçtiğiniz test yöntemlerini çalıştırır.

    - **Tüm testler** Çözümdeki tüm test yöntemlerini çalıştırır.

::: moniker-end

::: moniker range=">=vs-2019"

* Test Gezgini ' ne sağ tıklayın ve **Seçili testler Için kod kapsamını çözümle** ' yi seçin.

::: moniker-end

**Kod kapsamı sonuçlarını** penceresi satır, işlevi, sınıf, ad alanı ve modül tarafından uygulanan ürünün kodu bloklarının yüzdesini görüntüler.

Daha fazla bilgi için [ne kadar kodun test edildiğini belirlemek için kod kapsamı kullanın](../test/using-code-coverage-to-determine-how-much-code-is-being-tested.md).

## <a name="test-shortcuts"></a>Test kısayolları

Testler test Gezgini 'nden, test üzerindeki kod düzenleyicisine sağ tıklayıp **Test Çalıştır** ' ı seçerek veya Visual Studio 'Daki varsayılan [Test Gezgini kısayolları](../ide/default-keyboard-shortcuts-in-visual-studio.md#bkmk_testexplorerGLOBAL) kullanılarak çalıştırılabilir. Bazı kısayollar bağlam tabanlıdır. Bu, imlecinizin kod düzenleyicisinde olduğu yere göre testleri çalıştırdıkları veya hata ayıkladıkları anlamına gelir. İmlecinizin bir test yöntemi içindeyse, bu test yöntemi çalışır. İmlecinizin sınıf düzeyi ise, o sınıftaki tüm testler çalıştırılır. Bu, ad alanı düzeyi için de aynıdır.

|Sık kullanılan komutlar| Klavye Kısayolları|
|-|------------------------|
|TestExplorer.DebugAllTestsInContext|**Ctrl**+**R**, **CTRL**+**t**|
|TestExplorer.RunAllTestsInContext|**Ctrl**+**R**, **t**|
|TestExplorer.RunAllTests|**Ctrl**+**R**, **A**|
|TestExplorer.RepeatLastRun|**Ctrl**+**R**, **L**|

> [!NOTE]
> Testler yalnızca soyut sınıflarda tanımlandığından ve örneklenmemiş olduğundan, bir testi soyut bir sınıfta çalıştıramazsınız. Testleri soyut sınıflarda çalıştırmak için soyut sınıftan türeten bir sınıf oluşturun.

## <a name="see-also"></a>Ayrıca bkz.

- [Birim testi kod](../test/unit-test-your-code.md)
- [64 bitlik bir işlem olarak birim testi çalıştırma](../test/run-a-unit-test-as-a-64-bit-process.md)
- [Test Gezgini Hakkında SSS](test-explorer-faq.md)
