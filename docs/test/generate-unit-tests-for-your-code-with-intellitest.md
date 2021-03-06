---
title: Intellitest ile kodunuz için birim testleri oluşturma
ms.date: 10/05/2015
ms.topic: conceptual
f1_keywords:
- vs.UnitTest.CreateIntelliTest
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: c9670182432b1c6bc1e763e014b04b193c399330
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65461215"
---
# <a name="how-to-generate-unit-tests-by-using-intellitest"></a>Nasıl yapılır: Intellitest kullanarak birim testleri oluşturma

Intellitest, test verileri ve birim testleri paketi oluşturmak için .NET kodunuzu keşfeden. Koddaki her ifade için bir test girişi oluşturulur o ifadeyi yürütecek. Koddaki her koşullu şube için bir vaka analizi yapılır. Örneğin, `if` deyimleri, onaylamalar ve özel durumlar oluşturabilecek tüm işlemler analiz edilir. Bu analiz, yüksek kod kapsamı ile birim testleri oluşturma, yöntemlerinizin her biri için parametreleştirilmiş birim testi için test verilerini oluşturmak için kullanılır.

Intellitest çalıştırdığınızda, hangi testlerin başarısız oluyor ve onları düzeltmek için tüm gerekli kodu eklemek kolayca görebilirsiniz. Hangi testlerin bir regresyon paketi sağlamak için bir test projesine kaydetmek için seçebilirsiniz. Kodunuzu değiştikçe, üretilen testler, kod değişikliğine eşitlenmiş şekilde tutmanızı sağlayacak Intellitest yeniden çalıştırın.

## <a name="availability-and-extensions"></a>Kullanılabilirlik ve uzantıları

**Intellitest oluşturma** ve **Intellitest Çalıştır** menü komutları:

* Yalnızca Enterprise Edition, Visual Studio'da kullanılabilir.

* .NET Framework'ü hedefleyen yalnızca C# kodunu destekler.

* Olan [Genişletilebilir](#extend-framework) ve biçiminde, MSTest, MSTest V2, NUnit ve xUnit testleri yayma desteği.

* X64 desteklemeyen yapılandırma.

## <a name="explore-use-intellitest-to-explore-your-code-and-generate-unit-tests"></a>Keşfedin: Kodunuzu keşfedin ve birim testleri oluşturmak için Intellitest kullanın

Birim testler üretmek için türler genel olmalıdır.

1. Visual Studio'da çözümünüzü açın ve ardından test etmek istediğiniz yöntemi içeren sınıf dosyasını açın.

2. Bir yöntem sağ tıklatın ve seçin **Intellitest Çalıştır** , yönteminde kod için birim testleri oluşturmak için.

   ![Sağ&#45;Birim testler üretmek için yönteminizi tıklayın](../test/media/runpex.png)

   Intellitest kodunuz, farklı giriş ile birden çok kez çalışır. Her bir çalıştırmanın giriş test verileri ve elde edilen çıkış gösteren tablo ya da özel durum gösterilir.

   ![Testlerle araştırma sonuçları penceresi görüntülenir.](../test/media/pexexplorationresults.png)

Bir sınıfta tüm genel metotlar için birim testleri üretmek için yalnızca belirli bir yöntem yerine sınıfı sağ tıklayın ve ardından **Intellitest Çalıştır**. Aşağı açılan listeden kullanmak **araştırma sonuçları** penceresi sınıfında birim testleri ve her yöntem için giriş verilerini görüntülemek için.

![Listeden görüntülemek için test sonuçlarını seçin](../test/media/selectpextest.png)

Geçmek için kontrol testler için bildirilen sonuçları Sonuç sütunundaki kodunuz için beklentilerinizi. Başarısız testler için kodunuzu uygun şekilde düzeltin. Ardından düzeltmeler doğrulamak için Intellitest yeniden çalıştırın.

## <a name="persist-save-the-unit-tests-as-a-regression-suite"></a>Sürdür: Birim testleri bir regresyon paketi kaydedin.

1. Parametreli birim test projesine kaydetmek istediğiniz veri satırları seçin.

     ![Testleri seçin. doğru&#45;tıklayın ve Kaydet'i seçin](../test/media/savepextests.png)

     Test projesini görüntüleyebilir ve oluşturuldu - parametreli birim testi tek tek birim testleri, her satır için karşılık gelen kaydedilir *. g.cs* test projesini ve parametreli birim testi dosyası içine kaydedildi kendi ilişkili *.cs* dosya. Birim testlerini çalıştırmak ve el ile oluşturduğunuz herhangi bir birim test için yaptığınız gibi Test Explorer sonuçları görüntüleyin.

     ![Sınıf dosyasında birim testi görüntülemek için test yöntemi](../test/media/testmethodpex.png)

     Gerekli tüm başvuruları da test projesine eklenir.

     Yöntem kodunu değişirse birim testlerini değişiklikleri ile eşitlenmiş tutmak için Intellitest yeniden çalıştırın.

## <a name="assist-use-intellitest-to-focus-code-exploration"></a>Yardımcı: Odağı kod araştırması için Intellitest kullanın

1. Daha karmaşık bir kod varsa, Intellitest araştırma, kodunuzun odaklanarak ile yardımcı olur. Örneğin, bir parametre olarak arabirime sahip bir yöntemi varsa ve bu arabirimi uygulayan birden fazla sınıf, Intellitest söz konusu sınıfın bulur ve bir uyarı bildirir.

     Yapmak istediğinize karar verirken uyarıları görüntüleyin.

     ![Uyarıları görüntüle](../test/media/pexviewwarning.png)

2. Kodu inceleme ve test etmek istediğiniz anlamak sonra arabirimi sınamak üzere kullanmak için hangi sınıfların seçmek için uyarı düzeltebilirsiniz.

     ![Sağ&#45;uyarıya tıklayarak ve düzeltme seçin](../test/media/pexfixwarning.png)

     Bu seçenek eklenir *PexAssemblyInfo.cs* dosya.

     `[assembly: PexUseType(typeof(Camera))]`

3. Artık bir parametreli birim testi oluşturma ve verileri yalnızca, sabit sınıfı kullanarak test etmek için Intellitest yeniden çalıştırabilirsiniz.

     ![Intellitest test verileri oluşturmak için yeniden çalıştırın](../test/media/pexwarningsfixed.png)

## <a name="specify-use-intellitest-to-validate-correctness-properties-that-you-specify-in-code"></a>Belirtin: Kod içinde belirttiğiniz doğruluk özelliklerini doğrulamak için Intellitest kullanın

Giriş ve çıkışları doğrulamak için üretilmiş birim testlerini istediğiniz genel ilişkisi belirtin. Bu belirtim, bir test yöntemi gibi görünüyor, ancak Evrensel amaçlarıyla bir yöntem içinde kapsüllenir. Parametreli birim test yöntem budur ve yaptığınız herhangi bir onayları Intellitest oluşturabilen olası tüm giriş değerlerini tutmanız gerekir.

## <a name="q--a"></a>Soru - Yanıt

### <a name="q-can-you-use-intellitest-for-unmanaged-code"></a>S: Intellitest yönetilmeyen kod için kullanabilir miyim?

**Y:** Hayır, Intellitest yalnızca yönetilen kod ile çalışır.

### <a name="q-when-does-a-generated-test-pass-or-fail"></a>S: Ne zaman oluşturulan bir test geçti başarısız veya?

**Y:** Diğer bir birim test gibi hiçbir özel durum oluşursa bu geçirir. Herhangi bir onaylama işlemi başarısız olursa veya test edilen kod işlenmemiş bir özel durum oluşturursa başarısız olur.

Özel bazı durumlar oluşursa, geçirilebilecek bir test varsa, test yöntemi, test sınıfına veya derleme gereksinimlerinize göre aşağıdaki özniteliklerden birini düzeyi ayarlayabilirsiniz:

- **PexAllowedExceptionAttribute**

- **PexAllowedExceptionFromTypeAttribute**

- **PexAllowedExceptionFromTypeUnderTestAttribute**

- **PexAllowedExceptionFromAssemblyAttribute**

### <a name="q-can-i-add-assumptions-to-the-parameterized-unit-test"></a>S: Parametreli birim testine varsayımlar ekleyebilir miyim?

**Y:** Evet, varsayımlar hangi test verileri, belirli bir yöntem için birim testi için gerekli değildir. belirtmek için kullanın. Kullanım <xref:Microsoft.Pex.Framework.PexAssume> varsayımlar eklemek için sınıfı. Örneğin, bir varsayım ekleyebilirsiniz, `lengths` değişkeni şu şekilde null değil:

`PexAssume.IsNotNull(lengths);`

Bir varsayım ekleyip Intellitest yeniden yitirmesi test verileri kaldırılır.

### <a name="q-can-i-add-assertions-to-the-parameterized-unit-test"></a>S: Parametreli birim testine onaylar ekleyebilir miyim?

**Y:** Evet, Intellitest birim testleri çalıştırdığında ne raporunuza sunduğundan aslında doğru olduğunu denetler. Kullanım <xref:Microsoft.Pex.Framework.PexAssert> sınıfı veya onaylama Onaylamalar eklemek için test framework ile birlikte gelen API. Örneğin, iki değişken eşit olduğunu onaylama ekleyebilirsiniz.

`PexAssert.AreEqual(a, b);`

Onaylama Ekle ve Intellitest yeniden çalıştırın, değerinizi geçerli olduğunu ve yüklü değilse test başarısız olduğunu denetler.

### <a name="NoRun"></a> S: Parametreli birim testleri çalıştırmadan önce Intellitest oluşturabilir miyim?

**Y:** Evet, sınıf veya yöntemi içinde sağ tıklayın ve ardından **Intellitest oluşturma**.

![Sağ&#45;Düzenleyicisi, Intellitest oluşturma seçin](../test/media/pexcreateintellitest.png)

Testleriniz oluşturulmaya veya projenizin ve testleri nasıl adlandırıldığı değiştirmek için varsayılan biçimi kabul edin. Yeni bir test projesi oluşturun veya var olan bir projeye testlerinizi kaydedin.

![Intellitest MSTest varsayılan oluşturun](../test/media/pexcreateintellitestmstest.png)

<a name="extend-framework"></a>
### <a name="q-can-i-use-other-unit-test-frameworks-with-intellitest"></a>S: Intellitest ile diğer birim testi çerçeveleri kullanabilir miyim?

**Y:** Evet, için aşağıdaki adımları [bulun ve diğer çatıları Yükle](../test/install-third-party-unit-test-frameworks.md).
Test framework uzantıları Visual Studio Market'te de mevcuttur:

* [NUnit test oluşturucuları uzantısı](https://marketplace.visualstudio.com/items?itemName=NUnitDevelopers.TestGeneratorNUnitextension-18371)
* [test oluşturucuları için ise xUnit.net uzantısı](https://marketplace.visualstudio.com/items?itemName=BradWilson.xUnitnetTestExtensions)

Visual Studio'yu yeniden başlatın ve çözümünüzü yeniden sonra sınıf veya yöntemi içinde sağ tıklayın ve ardından seçin **Intellitest oluşturma**. Burada yüklü Çerçevenizi seçin:

![Diğer birim testi çerçevesi için Intellitest seçin](../test/media/pexcreateintellitestextensions.png)

Ardından, ilgili tek tek birim testleri oluşturmak için Intellitest Çalıştır *. g.cs* dosyaları.

### <a name="q-can-i-learn-more-about-how-the-tests-are-generated"></a>S: Testleri nasıl oluşturulacağını hakkında daha fazla bilgi edinebilirim?

**Y:** Evet, üst düzey bir genel bakış için bu okuyun [blog gönderisi](https://devblogs.microsoft.com/devops/intellitest-one-test-to-rule-them-all/).
