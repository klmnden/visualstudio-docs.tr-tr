---
title: Roslyn çözümleyicilerini kullanarak kod analizi
ms.date: 03/26/2018
ms.topic: overview
helpviewer_keywords:
- code analysis, managed code
- analyzers
- Roslyn analyzers
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: ba1529840a38a23929b9926cc4bed5cc22a058cb
ms.sourcegitcommit: 36f5ffd6ae3215fe31837f4366158bf0d871f7a9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59232573"
---
# <a name="overview-of-net-compiler-platform-analyzers"></a>.NET derleyici platformu Çözümleyicileri genel bakış

.NET derleyici Platformu ("Roslyn") Çözümleyicileri stili, kalite ve Bakım, tasarım ve diğer sorunlar için kodunuzu analiz edin. Visual Studio analiz Çözümleyicileri yerleşik bir kümesini içerir, C# veya yazarken Visual Basic kodunu yazın. Bu yerleşik Çözümleyicileri tercihlerini yapılandırabileceğiniz [metin düzenleyici seçenekleri](../ide/code-styles-and-quick-actions.md) sayfası veya bir [.editorconfig dosyasındaki](../ide/editorconfig-code-style-settings-reference.md). Visual Studio uzantısı veya bir NuGet paketi olarak ek Çözümleyicileri yükleyebilirsiniz.

Kural ihlallerinin bir çözümleyici tarafından bulunamazsa, Kod Düzenleyicisi'nde raporlanır (olarak bir *dalgalı* sorunlu kod altında) ve **hata listesi** penceresi.

Birçok çözümleyicisi kuralları veya *tanılama*, olması bir veya daha fazla ilişkili *kod düzeltme* sorunu düzeltmek için uygulayabilirsiniz. Visual Studio'ya her yerleşik Çözümleyicisi tanılama ilişkili kod düzeltme vardır. Kod düzeltmeleri, ampul simgesini menüsünde diğer türleri ile birlikte gösterilir [hızlı Eylemler](../ide/quick-actions.md). Bu kod düzeltmeleri hakkında daha fazla bilgi için bkz. [yaygın hızlı Eylemler](../ide/common-quick-actions.md).

![İhlali Çözümleyicisi ve kod düzeltmenizi hızlı eylem](../code-quality/media/built-in-analyzer-code-fix.png)

## <a name="roslyn-analyzers-vs-static-code-analysis"></a>Roslyn çözümleyicilerini statik kod analizi karşılaştırması

.NET derleyici Platformu ("Roslyn") Çözümleyicileri sonunda yerini alacak [statik kod analizi](../code-quality/code-analysis-for-managed-code-overview.md) yönetilen kod için. Statik kod analizi kuralları çoğunu zaten olarak Roslyn Çözümleyicisi tanılama yazıldı.

Roslyn Çözümleyicisi ihlalleri statik kod analizi kural ihlalleri gibi görünen **hata listesi**. Ayrıca, Roslyn Çözümleyicisi ihlalleri ayrıca Kod düzenleyicisinde görünmesini *squigglies* sorunlu kod altında. Dalgalı rengi bağımlı [önem derecesi ayarına](../code-quality/use-roslyn-analyzers.md#rule-severity) kural. Üç ihlalleri aşağıdaki ekran görüntüsünde gösterilmektedir&mdash;bir kırmızı, yeşil bir ve bir gri:

![Kod düzenleyicisinde Squigglies](media/diagnostics-severity-colors.png)

Roslyn çözümleyicilerini etkinleştirildi ancak siz yazarken canlı, ayrıca, statik kod analizi gibi derleme zamanında kod analiz edin. Etkinleştirirseniz [tam çözüm analizini](../code-quality/how-to-enable-and-disable-full-solution-analysis-for-managed-code.md#to-toggle-full-solution-analysis), Roslyn Çözümleyicileri de düzenleyicide açık olmayan kod dosyaları tasarım zamanı analizini sağlar.

> [!TIP]
> Derleme hataları ve Uyarıları Roslyn Çözümleyicileri gelen yalnızca bir NuGet paketi olarak Çözümleyicileri yüklü olup olmadığını gösterilir.

Yalnızca aynı türdeki statik kod analizini yapar sorunları rapor Roslyn Çözümleyicileri, ancak bunların birini veya tümünü dosyası veya proje dosyasında ihlali oluşumlarını gidermenizi kolaylaştırır. Bu eylemler adlı *kod düzeltme*. Kod düzeltmeleri IDE özgüdür; Visual Studio'da, bunlar olarak uygulanan [hızlı Eylemler](../ide/quick-actions.md). Tüm Çözümleyicisi tanılama ilişkili kod düzeltme vardır.

> [!NOTE]
> Aşağıdaki kullanıcı Arabirimi seçenekleri, yalnızca statik kod analizi için geçerlidir:
>
> - **Çözümle** > **kod çözümlemeyi Çalıştır** menü seçeneği.
> - **Derlemede kod analizini etkinleştir** ve **üretilen koddan gelen sonuçları Gizle** onay **Kod Analizi** sekmesinde bir projenin özellik sayfalarındaki (Bu seçenekler sahip yok etkisi Roslyn Çözümleyicileri).

Roslyn çözümleyicilerini gelen ihlalleri ve statik kod analizi birbirinden ayırmak için **hata listesi**, bakmak **aracı** sütun. Aracı değer Çözümleyicisi derlemelerde birini eşleşip eşleşmediğini **Çözüm Gezgini**, örneğin **Microsoft.CodeQuality.Analyzers**, ihlalin Roslyn Çözümleyicisi'nden gelir. Aksi takdirde, statik kod çözümleme dışı ihlali kaynaklanır.

![Hata listesi sütunu aracı](media/code-analysis-tool-in-error-list.png)

> [!TIP]
> **RunCodeAnalysis** proje dosyasında msbuild özelliği, yalnızca statik kod analizi uygulanır. Çözümleyicilerini yükleme verilirse **RunCodeAnalysis** için **false** proje dosyanızda statik kod analizi derleme sonrasında çalışmasını engelleyin.
>
> ```xml
> <RunCodeAnalysis>false</RunCodeAnalysis>
> ```

## <a name="nuget-package-versus-vsix-extension"></a>NuGet paketi VSIX uzantısı karşılaştırması

.NET derleyici platformu Çözümleyicileri olabilir, her proje bir NuGet paketi veya Visual Studio genelinde üzerinden Visual Studio uzantısı olarak yüklü. Bu iki yöntemden arasındaki bazı temel davranış farkları vardır [çözümleyicilerini yükleme](../code-quality/install-roslyn-analyzers.md).

### <a name="scope"></a>Kapsam

Visual Studio uzantısı olarak Çözümleyicileri yüklerseniz, Visual Studio'nun tüm örneklerini çözüm düzeyinde uygulanır. Tercih edilen yöntemi olan bir NuGet paketi olarak Çözümleyicileri yüklerseniz bunlar yalnızca NuGet paketini yüklendiği projesi için geçerlidir. Ekip ortamlarında kapsamın Çözümleyicileri NuGet paketleri olarak yüklü bulunan *tüm geliştiricilerin* bu proje üzerinde çalışır.

### <a name="build-errors"></a>Derleme hataları

Komut satırı aracılığıyla parçası olarak veya sürekli tümleştirme (CI) derleme dahil olmak üzere yapı zamanında uygulanan kuralları için bir NuGet paketi olarak Çözümleyicileri yükleyin. Uzantı olarak Çözümleyicileri yüklerseniz Çözümleyicisi uyarılarını ve hataları derleme raporda görünmüyor.

Aşağıdaki ekran görüntüsünde, komut satırı derleme çıktı Çözümleyicisi Kuralı ihlali içeren bir proje oluşturma gösterir:

![MSBuild çıkışıyla kuralı ihlali](media/command-line-build-analyzers.png)

### <a name="rule-severity"></a>Kural önem derecesi

Visual Studio uzantısı olarak yüklenen Çözümleyicileri gelen kural önem derecesi olarak ayarlanamıyor. Yapılandırmak için [kural önem derecesi](../code-quality/use-roslyn-analyzers.md#rule-severity), bir NuGet paketi olarak çözümleyicilerini yükleme.

## <a name="next-steps"></a>Sonraki adımlar

> [!div class="nextstepaction"]
> [Visual Studio'da Roslyn çözümleyicilerini yükleme](../code-quality/install-roslyn-analyzers.md)

> [!div class="nextstepaction"]
> [Roslyn çözümleyicilerini Visual Studio'da kullanın](../code-quality/use-roslyn-analyzers.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Çözümleyiciler hakkında SSS](analyzers-faq.md)
- [Kendi Roslyn çözümleyicinizi yazma](../extensibility/getting-started-with-roslyn-analyzers.md)
- [.NET Compiler Platform SDK’sı](/dotnet/csharp/roslyn-sdk/)