---
title: Birim testi ile çalışmaya başlama
ms.date: 04/01/2019
ms.topic: conceptual
helpviewer_keywords:
- unit testing, create unit test plans
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f3f3537a56b746c9104898d68e40038fcd545910
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58856466"
---
# <a name="get-started-with-unit-testing"></a>Birim testi ile çalışmaya başlama

Visual Studio, tanımlamak ve kod durumunu korumak, kod kapsamından emin olmak için birim testleri çalıştırın ve müşterilerinizin yapmadan önce hataları ve hataları bulmak için kullanın. Sık kodunuzun düzgün çalıştığından emin olmak için birim testlerinizi çalıştırın.

## <a name="create-unit-tests"></a>Birim testleri oluşturma

Bu bölümde, yüksek düzeyde birim testi projesi oluşturma işlemini açıklar.

> [!TIP]
> "HelloWorldCore", test altındaki projeye bir örnek projesidir ve hiçbir kodunu gösterilecek içindir. Test için bkz: bir "Merhaba Dünya" projesi oluşturmak istiyorsanız [ilk kez oluşturma C# konsol uygulaması](../ide/quickstart-csharp-console.md). İzlenecek tam yol makale için bkz: [oluşturma ve çalıştırma birim testleri için yönetilen kod](walkthrough-creating-and-running-unit-tests-for-managed-code.md).

1. Visual Studio'da test etmek istediğiniz projeyi açın.

1. İçinde **Çözüm Gezgini**, çözüm düğümü seçin. Ardından, üstteki menü çubuğundan **dosya** > **Ekle** > **yeni proje**.

1. Yeni Proje iletişim kutusunda, bir birim testi proje şablonunu seçin ve istediğiniz test çerçevesi için bulun.

   ::: moniker range=">=vs-2019"

   ![Visual Studio 2019'de birim test projesi şablonunu](media/vs-2019/add-new-test-project.png)

   Tıklayın **sonraki**test projesi için bir ad seçin ve ardından **Oluştur**.

   ::: moniker-end

   ::: moniker range="vs-2017"

   ![Visual Studio 2019'de birim test projesi şablonunu](media/mstest-test-project-template.png)

   Test projesi için bir ad seçin ve ardından **Tamam**.

   ::: moniker-end

   Projeyi çözümünüze eklenir.

   ![Çözüm Gezgini'nde birim testi projesi](media/vs-2019/solution-explorer.png)

1. Birim test projesinde, sağ tıklayarak test etmek istediğiniz projeye bir başvuru eklemek **başvuruları** veya **bağımlılıkları** seçip **Başvuru Ekle**.

1. Test edip tıklayın, kodu içeren projeyi seçin **Tamam**.

   ![Visual Studio'da proje başvurusu Ekle](media/vs-2019/reference-manager.png)

1. Kod için birim test yöntemini ekleyin.

   ![Visual Studio'da birim test yöntemine kod ekleyin](media/vs-2019/unit-test-method.png)

## <a name="run-unit-tests"></a>Birim testleri çalıştırma

1. Açık [Test Gezgini](../test/run-unit-tests-with-test-explorer.md) seçerek **Test** > **Windows** > **Test Gezgini** üst menü çubuğundan.

1. Tıklayarak birim testlerinizi çalıştırın **tümünü Çalıştır**.

   ![Test Gezgini'nde birim testleri çalıştırma](media/vs-2019/test-explorer-run-all.png)

   Testleri tamamladıktan sonra yeşil bir onay işareti, bir testi geçtiğini gösterir. Kırmızı "x" simgesini bir testin başarısız olduğunu gösterir.

   ![Test Gezgini'nde birim testi sonuçlarını gözden geçirin](media/vs-2019/unit-test-passed.png)

> [!TIP]
> Kullanabileceğiniz [Test Gezgini](../test/run-unit-tests-with-test-explorer.md) yerleşik test çerçevesi (MSTest) birim testleri çalıştırma veya üçüncü taraftan test çerçeveleri. Testleri kategoriler halinde gruplandırmak, test listesini filtrelemek ve oluşturmak, kaydedin ve test çalma listeleri çalıştırın. Ayrıca, Testlerde Hata Ayıkla ve test, performans ve kod kapsamını analiz edin.

## <a name="view-live-unit-test-results"></a>Canlı birim testi sonuçlarını görüntüleme

MSTest, xUnit ve NUnit test çerçevesi Visual Studio 2017 veya sonraki bir sürümde kullanıyorsanız, Canlı Birim testlerinizin sonuçları görebilirsiniz.

> [!NOTE]
> Live unit Testing, yalnızca Enterprise Edition'da kullanılabilir.

1. Live unit testing alanından kapatma **Test** menüsünü seçerek **Test** > **Live Unit Testing** > **Başlat**.

   ::: moniker range="vs-2017"

   ![Live unit Testing üzerinde Aç](media/live-test-results-start.png)

   ::: moniker-end

   ::: moniker range=">=vs-2019"

   ![Live unit testing Visual Studio 2019 Başlat](media/vs-2019/start-live-unit-testing.png)

   ::: moniker-end

1. Yazma ve kod düzenleme gibi kod düzenleyicisi penceresi içinde test sonuçlarını görüntüleyin.

   ![Test sonuçlarını görüntüleme](media/vs-2019/live-unit-testing-results.png)

1. Bu yöntem kapsayan testlerin adlarını gibi daha fazla bilgi için test sonucu göstergesi tıklayın.

   ![Test sonucu göstergelerini seçin](media/vs-2019/live-unit-testing-details.png)

Live unit testing hakkında daha fazla bilgi için bkz: [Live unit testing](../test/live-unit-testing-intro.md).

## <a name="generate-unit-tests-with-intellitest"></a>Intellitest ile birim testleri oluşturma

Intellitest çalıştırdığınızda, hangi testlerin başarısız oluyor ve onları düzeltmek için tüm gerekli kodu eklemek görebilirsiniz. Hangi testlerin bir regresyon paketi sağlamak için bir test projesine kaydetmek için seçebilirsiniz. Kodunuzu değiştikçe, üretilen testler, kod değişikliğine eşitlenmiş şekilde tutmanızı sağlayacak Intellitest yeniden çalıştırın. Bilgi edinmek için bkz. nasıl [Intellitest ile kodunuz için birim testleri oluşturmak](../test/generate-unit-tests-for-your-code-with-intellitest.md).

> [!TIP]
> Intellitest, yalnızca .NET Framework'ü hedefleyen yönetilen kod için kullanılabilir.

![Intellitest oluşturma birim testleriyle](media/intellitest.png)

## <a name="analyze-code-coverage"></a>Kod kapsamını analiz etme

Proje kodunuzun ne oranda aslında birim testleri gibi kodlanmış testler tarafından test edilen belirlemek için Visual Studio kod kapsamı özelliğini kullanabilirsiniz. Etkin hatalara karşı koruma sağlamak için testleriniz kodunuzun büyük bir kısmı entegrasyonlar için çalışılmalı. Bilgi edinmek için bkz. nasıl [ne kadar kodun test edildiğini belirlemek için kod kapsamı kullanın](../test/using-code-coverage-to-determine-how-much-code-is-being-tested.md).

## <a name="use-a-third-party-test-framework"></a>Bir üçüncü taraf test çerçevesi kullanın

Visual Studio'da, Boost, Google ve NUnit gibi üçüncü taraf test çerçevelerini kullanarak birim testleri çalıştırabilirsiniz. Kullanım **NuGet Paket Yöneticisi** tercih ettiğiniz çerçevesi için NuGet paketini yüklemek için. Veya, xUnit ve NUnit için test çerçeveleri, Visual Studio gerekli NuGet paketlerini içeren, önceden yapılandırılmış test proje şablonları içerir.

Kullanan birim testleri oluşturmak için [NUnit](https://nunit.org/):

1. Test etmek istediğiniz kodu içeren çözümü açın.

2. Çözüme sağ **Çözüm Gezgini** ve **Ekle** > **yeni proje**.

3. Seçin **NUnit Test projesini** proje şablonu.

   ::: moniker range=">=vs-2019"

   ![Visual Studio 2019 NUnit test proje şablonu](media/vs-2019/nunit-test-project-template.png)

   Tıklayın **sonraki**, projeyi adlandırın ve ardından **Oluştur**.

   ::: moniker-end

   ::: moniker range="vs-2017"

   Projeyi adlandırın ve ardından **Tamam** oluşturun.

   ::: moniker-end

   Proje şablonu NUnit NUnit3TestAdapter NuGet başvurular içerir.

   ![Çözüm Gezgini'nde NUnit NuGet bağımlılıklarını](media/vs-2019/nunit-nuget-dependencies.png)

4. Bir başvuru test projesinden test etmek istediğiniz kodu içeren projeye ekleyin.

5. Kod, test yöntemine ekleyin.

   ![Kod birim testi kod dosyanıza ekleyin](media/vs-2019/unit-test-method.png)

6. Test çalıştırmak **Test Gezgini** veya test kodu sağ tıklayıp seçme **çalıştırma test**.

## <a name="see-also"></a>Ayrıca bkz.

* [İzlenecek yol: Yönetilen kod için birim testleri oluşturma ve çalıştırma](walkthrough-creating-and-running-unit-tests-for-managed-code.md)
* [Birim Testleri Oluştur komutu](create-unit-tests-menu.md)
* [Intellitest ile testleri oluşturma](generate-unit-tests-for-your-code-with-intellitest.md)
* [Test Gezgini ile testleri çalıştırma](run-unit-tests-with-test-explorer.md)
* [Kod kapsamını analiz etme](using-code-coverage-to-determine-how-much-code-is-being-tested.md)