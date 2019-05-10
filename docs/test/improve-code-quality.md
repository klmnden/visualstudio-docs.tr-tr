---
title: Test araçları
ms.date: 03/16/2018
ms.topic: conceptual
helpviewer_keywords:
- testing tools [Visual Studio]
- unit tests [Visual Studio]
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 435eb2571f709f3ed5df4effbfdf3b5f4970457b
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65461403"
---
# <a name="testing-tools-in-visual-studio"></a>Visual Studio Test Araçları

Visual Studio Test Araçları size yardımcı olabilir ve takımınızın geliştirmek ve bunu sürdürmek yüksek standartlarda kod memnuniyeti.

> [!NOTE]
> Birim testi Visual Studio'nun tüm sürümlerinde kullanılabilir. Live Unit Testing, Intellitest ve kodlanmış UI testi gibi diğer test araçları yalnızca Visual Studio Enterprise Edition'da kullanılabilir. Sürümleri hakkında daha fazla bilgi için bkz. [karşılaştırma Visual Studio Ide'leri](https://visualstudio.microsoft.com/vs/compare/).

## <a name="test-explorer"></a>Test Gezgini

**Test Gezgini** penceresi oluşturma, yönetme ve birim testlerini çalıştırmak geliştiriciler yardımcı olur. Microsoft birim test çerçevesini veya çeşitli üçüncü taraf ve açık kaynak çerçevelerinden birini kullanabilirsiniz.

![Visual Studio Test Gezgini](media/devtest-testexplorer.png)

* [Birim testi ile çalışmaya başlama](unit-test-your-code.md)
* [Test Gezgini ile birim testleri çalıştırma](run-unit-tests-with-test-explorer.md)
* [Test Gezgini Hakkında SSS](test-explorer-faq.md)
* [Üçüncü taraf birim testi çerçevelerini yükleme](install-third-party-unit-test-frameworks.md)

Visual Studio ayrıca genişletilebilir ve üçüncü taraf birim test bağdaştırıcısı NUnit ve xUnit.net gibi kapısı açılır. Ayrıca, kod kopyalama yeteneğini yakından el gider yaygın hata düzeltmeleri için aday olabilecek anlamsal olarak benzer bir kod bloklarını belirlemenize yardımcı olur veya yeniden düzenleme yüksek kaliteli yazılım sunmaya ile.

![Üçüncü taraf test tümleştirmesi](media/devtest-thirdparty.png)

## <a name="live-unit-testing"></a>Live Unit Testing

[Live Unit Testing](../test/live-unit-testing.md) otomatik olarak birim testleri arka planda çalışır ve grafik olarak Visual Studio Kod Düzenleyicisi'nde kod kapsamı ve test sonuçlarını görüntüler.

## <a name="intellitest"></a>IntelliTest

Intellitest, birim testleri ve test verilerini, yönetilen kod için otomatik olarak oluşturur. Intellitest kapsamı artırır ve yeni veya mevcut koda yönelik birim testleri oluşturmak ve sürdürmek için gereken çabayı önemli ölçüde azaltır.

![Intellitest sürüyor](media/devtest-intellitest.png)

* [Intellitest ile kodunuz için birim testleri oluşturma](generate-unit-tests-for-your-code-with-intellitest.md)
* [Intellitest – hepsini yönetmek için bir test](https://devblogs.microsoft.com/devops/intellitest-one-test-to-rule-them-all/)
* [Intellitest başvuru kılavuzu](intellitest-manual/index.md)

## <a name="code-coverage"></a>Kod kapsamı

[Kod kapsamı](../test/using-code-coverage-to-determine-how-much-code-is-being-tested.md) proje kodunuzun ne oranda aslında birim testleri gibi kodlanmış testler tarafından edildiğini belirler. Etkin hatalara karşı koruma sağlamak için testleriniz çalışma veya "kodunuzun büyük bir kısmı kapsayan".

Kod kapsamı analizi, yönetilen ve yönetilmeyen (yerel) kod için uygulanabilir.

Test yöntemlerini Test Gezgini'ni kullanarak çalıştırdığınızda kod kapsamı bir seçenektir. Sonuçlar tablosu, her derleme sınıfı ve yöntemi içinde çalışan kod yüzdesini gösterir. Ayrıca, kaynak düzenleyici hangi kodun test edildiğini gösterir.

* [Ne kadar kodun test edildiğini belirlemek için kod kapsamını kullanma](using-code-coverage-to-determine-how-much-code-is-being-tested.md)
* [Birim testi, kod kapsamını ve kod kopya Analizi ile Visual Studio (Laboratuvar)](http://download.microsoft.com/download/6/2/B/62B60ECE-B9DC-4E8A-A97C-EA261BFB935E/Docs/Unit%20Testing,%20Code%20Coverage%20and%20Code%20Clone%20Analysis%20with%20Visual%20Studio%202015.docx)
* [Kod kapsamı analizini özelleştirme](customizing-code-coverage-analysis.md)

## <a name="microsoft-fakes"></a>Microsoft Fakes

[Microsoft Fakes](../test/isolating-code-under-test-with-microsoft-fakes.md) test ettiğiniz uygulamanın diğer bölümlerini saptamalar veya dolgular ile değiştirerek kodu yalıtmanıza yardımcı olur.

## <a name="user-interface-testing-with-coded-ui-and-selenium"></a>Kullanıcı arabirimi kodlanmış UI ve Selenium ile test

Kodlanmış UI testleri, uygulamanızın kullanıcı arabiriminin davranışı ve işlevsellik doğrulamak için tam olarak otomatikleştirilmiş testler oluşturmak için bir yol sağlar. Bunlar, teknoloji, XAML tabanlı UWP uygulamaları, tarayıcı uygulamaları ve SharePoint uygulamaları gibi birçok platformda UI testi otomatik hale getirebilirsiniz.

En iyi türünün en iyisi kodlanmış UI testleri veya Selenium ile test genel tarayıcı tabanlı UI olsun, Visual Studio, ihtiyacınız olan araçları sağlar.

![Kullanıcı Arabirimi ile kodlanmış UI testi](media/devtest-codeduitest.png)

* [UI otomasyonunu kullanarak kodunuzu test etme](use-ui-automation-to-test-your-code.md)
* [Oluşturma, düzenleme ve kodlanmış UI testi Bakımı kullanmaya başlayın](walkthrough-creating-editing-and-maintaining-a-coded-ui-test.md)
* [Kodlanmış UI testleriyle UWP uygulamalarını test etme](test-uwp-app-with-coded-ui-test.md)
* [Kodlanmış UI testlerini Visual Studio Enterprise (Laboratuvar) ile giriş](http://download.microsoft.com/download/6/2/B/62B60ECE-B9DC-4E8A-A97C-EA261BFB935E/Docs/Introduction%20to%20Coded%20UI%20Tests%20with%20Visual%20Studio%20Enterprise%202015.docx)

## <a name="load-testing"></a>Yük testi

[Yük testi](../test/quickstart-create-a-load-test-project.md) birim testleri ve web performans testleri çalıştırarak sunucu uygulaması üzerindeki yük benzetimini yapar.

## <a name="related-scenarios"></a>İlgili senaryolar

* [Keşif & el ile test (Azure Test planları)](/azure/devops/test/index?view=vsts)
* [Yük testi (Azure Test planları)](/azure/devops/test/load-test/index?view=vsts)
* [Sürekli test (Azure Test planları)](/azure/devops/pipelines/test/getting-started-with-continuous-testing?view=vsts)
* [Kod çözümleme araçları](../code-quality/code-analysis-for-managed-code-overview.md)
