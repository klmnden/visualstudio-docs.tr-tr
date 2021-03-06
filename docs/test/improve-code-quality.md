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
ms.openlocfilehash: 153624ec6f0bdb13e4d89a92edf977d0badc7e62
ms.sourcegitcommit: 3e74ec49a54e5c3da7631f4466128cdf4384af6b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "68712212"
---
# <a name="testing-tools-in-visual-studio"></a>Visual Studio Test Araçları

Visual Studio Test Araçları size yardımcı olabilir ve takımınızın geliştirmek ve bunu sürdürmek yüksek standartlarda kod memnuniyeti.

> [!NOTE]
> Birim testi Visual Studio'nun tüm sürümlerinde kullanılabilir. Live Unit Testing, IntelliTest ve kodlanmış UI testi gibi diğer test araçları yalnızca Visual Studio Enterprise sürümünde kullanılabilir. Sürümler hakkında daha fazla bilgi için bkz. [Visual Studio Ides 'ı karşılaştırın](https://visualstudio.microsoft.com/vs/compare/).

## <a name="test-explorer"></a>Test Gezgini

**Test Gezgini** penceresi, geliştiricilerin birim testlerini oluşturmalarına, yönetmesine ve çalıştırmasına yardımcı olur. Microsoft birim test çerçevesini veya çeşitli üçüncü taraf ve açık kaynak çerçevelerinden birini kullanabilirsiniz.

::: moniker range="vs-2017"
![Visual Studio Test Gezgini](media/devtest-testexplorer.png)
::: moniker-end

::: moniker range="vs-2019"
![Visual Studio Test Gezgini 16,2](media/vs-2019/test-explorer-16-2.PNG)
::: moniker-end

* [Birim testini kullanmaya başlama](unit-test-your-code.md)
* [Test Gezgini ile birim testleri çalıştırma](run-unit-tests-with-test-explorer.md)
* [Test Gezgini Hakkında SSS](test-explorer-faq.md)
* [Üçüncü taraf birim testi çerçevelerini yükleme](install-third-party-unit-test-frameworks.md)

Visual Studio da genişletilebilir ve NUnit ve xUnit.net gibi üçüncü taraf birim testi bağdaştırıcılarının kapısını açar. Ayrıca, kod kopyalama özelliği, yaygın hata düzeltmeleri veya yeniden düzenleme için aday olabilecek anlamsal benzer kod bloklarını tanımlamanızı sağlayarak yüksek kaliteli yazılım sunmaya yardımcı olur.

![Üçüncü taraf test tümleştirmesi](media/devtest-thirdparty.png)

## <a name="live-unit-testing"></a>Live Unit Testing

[Live Unit Testing](../test/live-unit-testing.md) otomatik olarak birim testleri arka planda çalışır ve grafik olarak Visual Studio Kod Düzenleyicisi'nde kod kapsamı ve test sonuçlarını görüntüler.

## <a name="intellitest"></a>IntelliTest

IntelliTest, yönetilen kodunuz için birim testlerini ve test verilerini otomatik olarak oluşturur. IntelliTest kapsamı geliştirir ve yeni veya mevcut kod için birim testleri oluşturma ve sürdürme çabaları önemli ölçüde azaltır.

![IntelliTest eylemde](media/devtest-intellitest.png)

* [Intellitest ile kodunuz için birim testleri oluşturma](generate-unit-tests-for-your-code-with-intellitest.md)
* [IntelliTest – tümünü kurala göre bir test](https://devblogs.microsoft.com/devops/intellitest-one-test-to-rule-them-all/)
* [Intellitest başvuru kılavuzu](intellitest-manual/index.md)

## <a name="code-coverage"></a>Kod kapsamı

[Kod kapsamı](../test/using-code-coverage-to-determine-how-much-code-is-being-tested.md) proje kodunuzun ne oranda aslında birim testleri gibi kodlanmış testler tarafından edildiğini belirler. Hatalara karşı etkili bir şekilde koruma sağlamak için, testleriniz kodunuzun büyük bir oranını "ele almalıdır" veya "kapsamalıdır".

Kod kapsamı analizi, hem yönetilen hem de yönetilmeyen (yerel) koda uygulanabilir.

Test yöntemlerini Test Gezgini'ni kullanarak çalıştırdığınızda kod kapsamı bir seçenektir. Sonuçlar tablosu, her derleme sınıfı ve yöntemi içinde çalışan kod yüzdesini gösterir. Ayrıca, kaynak düzenleyici hangi kodun test edildiğini gösterir.

* [Ne kadar kodun test edildiğini belirlemek için kod kapsamını kullanma](using-code-coverage-to-determine-how-much-code-is-being-tested.md)
* [Visual Studio (Lab) ile birim testi, kod kapsamı ve kod kopyası Analizi](http://download.microsoft.com/download/6/2/B/62B60ECE-B9DC-4E8A-A97C-EA261BFB935E/Docs/Unit%20Testing,%20Code%20Coverage%20and%20Code%20Clone%20Analysis%20with%20Visual%20Studio%202015.docx)
* [Kod kapsamı analizini özelleştirme](customizing-code-coverage-analysis.md)

## <a name="microsoft-fakes"></a>Microsoft Fakes

[Microsoft Fakes](../test/isolating-code-under-test-with-microsoft-fakes.md) , uygulamanın diğer bölümlerini saplamalar veya parçalar ile değiştirerek test ettiğiniz kodu yalıtmanıza yardımcı olur.

## <a name="user-interface-testing-with-coded-ui-and-selenium"></a>Kodlanmış UI ve Selenium ile Kullanıcı Arabirimi testi

Kodlanmış UI testleri, uygulamanızın kullanıcı arabiriminin işlevselliğini ve davranışını doğrulamak için tam otomatikleştirilmiş testlerin oluşturulması için bir yol sağlar. XAML tabanlı UWP uygulamaları, tarayıcı uygulamaları ve SharePoint uygulamaları da dahil olmak üzere çeşitli teknolojiler genelinde UI testini otomatik hale getirebilir.

Selenium ile, en iyi kodlanmış UI testlerini veya genel tarayıcı tabanlı UI testini tercih etmeksizin, Visual Studio ihtiyacınız olan tüm araçları sağlar.

![Kodlanmış UI ile UI testi](media/devtest-codeduitest.png)

* [UI otomasyonunu kullanarak kodunuzu test etme](use-ui-automation-to-test-your-code.md)
* [Kodlanmış UI testi oluşturmaya, düzenlemesine ve sürdürme ile çalışmaya başlama](walkthrough-creating-editing-and-maintaining-a-coded-ui-test.md)
* [Kodlanmış UI Testleriyle UWP uygulamalarını test etme](test-uwp-app-with-coded-ui-test.md)
* [Visual Studio Enterprise (Lab) ile kodlanmış UI testlerine giriş](http://download.microsoft.com/download/6/2/B/62B60ECE-B9DC-4E8A-A97C-EA261BFB935E/Docs/Introduction%20to%20Coded%20UI%20Tests%20with%20Visual%20Studio%20Enterprise%202015.docx)

## <a name="load-testing"></a>Yük testi

[Yük testi](../test/quickstart-create-a-load-test-project.md) birim testleri ve web performans testleri çalıştırarak sunucu uygulaması üzerindeki yük benzetimini yapar.

## <a name="related-scenarios"></a>İlgili senaryolar

* [Keşif & el ile test (Azure Test planları)](/azure/devops/test/index?view=vsts)
* [Yük testi (Azure Test planları)](/azure/devops/test/load-test/index?view=vsts)
* [Sürekli test (Azure Test planları)](/azure/devops/pipelines/test/getting-started-with-continuous-testing?view=vsts)
* [Kod çözümleme araçları](../code-quality/code-analysis-for-managed-code-overview.md)
