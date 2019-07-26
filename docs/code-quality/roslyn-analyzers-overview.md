---
title: Roslyn Çözümleyicileri kullanarak kod analizi
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
ms.openlocfilehash: cae7a02c774773d08c287dde7df59ff62fdbec58
ms.sourcegitcommit: 9cfd3ef6c65f671a26322320818212a1ed5955fe
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/26/2019
ms.locfileid: "68533346"
---
# <a name="overview-of-net-compiler-platform-analyzers"></a>.NET Compiler Platform çözümleyicilerine genel bakış

.NET Compiler Platform ("Roslyn") Çözümleyicileri, kodunuzu stil, kalite ve bakım, tasarım ve diğer sorunlar için analiz eder. Visual Studio, siz yazarken C# veya Visual Basic kodunuzu çözümleyen yerleşik çözümleyiciler kümesini içerir. Bu yerleşik çözümleyiciler için tercihleri [metin düzenleyici seçenekleri](../ide/code-styles-and-code-cleanup.md) sayfasında veya bir [. editorconfig dosyasında](../ide/editorconfig-code-style-settings-reference.md)yapılandırırsınız. Ek Çözümleyicileri, Visual Studio uzantısı veya NuGet paketi olarak yükleyebilirsiniz.

Kural ihlalleri bir çözümleyici tarafından bulunursa, bunlar kod düzenleyicisinde (sorunlu kod altında bir *dalgalı çizgi* olarak) ve **hata listesi** penceresinde raporlanır.

Birçok çözümleyici kuralı veya *tanılaması*, sorunu gidermek için uygulayabileceğiniz bir veya daha fazla ilişkili *kod düzeltmesiyle* birlikte bulunabilir. Visual Studio 'da yerleşik olarak bulunan çözümleyici tanılamaları, ilişkili bir kod düzeltmesine sahiptir. Kod düzeltmeleri, ampul simgesi menüsünde diğer [hızlı eylem](../ide/quick-actions.md)türleriyle birlikte gösterilir. Bu kod düzeltmeleri hakkında daha fazla bilgi için bkz. [Genel Hızlı Eylemler](../ide/common-quick-actions.md).

![Çözümleyici ihlali ve hızlı eylem kodu onarımı](../code-quality/media/built-in-analyzer-code-fix.png)

## <a name="roslyn-analyzers-vs-static-code-analysis"></a>Roslyn Çözümleyicileri-statik kod analizi

.NET Compiler Platform ("Roslyn") çözümleyiciler, yönetilen kod için, sonunda [Statik kod analizini](../code-quality/code-analysis-for-managed-code-overview.md) değiştirecektir. Statik kod analizi kurallarının birçoğu zaten Roslyn Çözümleyicisi tanılama olarak yeniden yazıldı.

Statik kod çözümleme kuralı ihlalleri gibi, Roslyn çözümleyici ihlalleri **hata listesi**görüntülenir. Ayrıca, Roslyn Çözümleyicisi ihlalleri, kod Düzenleyicisi 'nde, sorunlu kodun altında *dalgalı çizgiler* olarak da görünür. Dalgalı çizginin rengi kuralın [önem derecesi ayarına](../code-quality/use-roslyn-analyzers.md#rule-severity) bağlıdır. Aşağıdaki ekran görüntüsünde, bir kırmızı&mdash;, bir yeşil ve bir gri olmak üzere üç ihlal gösterilmektedir:

![Kod düzenleyicisinde dalgalı çizgiler](media/diagnostics-severity-colors.png)

Roslyn çözümleyiciler, etkinleştirilirse statik kod analizi gibi derleme zamanında kodu analiz eder, ancak yazarken da canlı hale gelir. [Tam çözüm analizini](../code-quality/how-to-enable-and-disable-full-solution-analysis-for-managed-code.md#to-toggle-full-solution-analysis)etkinleştirirseniz, Roslyn Çözümleyicileri, düzenleyicide açık olmayan kod dosyalarının tasarım zamanı analizini de sağlar.

> [!TIP]
> Roslyn çözümleyicilerinin derleme zamanı hataları ve uyarıları yalnızca çözümleyiciler bir NuGet paketi olarak yüklenirse gösterilir.

Yalnızca Roslyn çözümleyicilerinin, statik kod analizi tarafından aynı tür sorunları rapor ettiğine değil, ancak dosya veya projenizde ihlalin bir kısmını veya tümünü düzeltmenize olanak sağlar. Bu eylemlere *kod düzeltmeleri*denir. Kod düzeltmeleri IDE 'ye özgüdür; Visual Studio 'da, bunlar [hızlı eylemler](../ide/quick-actions.md)olarak uygulanır. Tüm çözümleyici tanılamaları ilişkili bir kod düzeltmesine sahip değildir.

> [!NOTE]
> Aşağıdaki UI seçenekleri yalnızca statik kod analizi için geçerlidir:
>
> - **Çalıştırma kodu analizini** **Çözümle** > menü seçeneği.
> - Projenin özellik sayfalarındaki **Kod Analizi** sekmesinde **oluşturulan kod** onay kutularından sonuçları derleme ve gizleme **üzerinde Kod analizini etkinleştir** (Bu seçeneklerin Roslyn Çözümleyicileri üzerinde hiçbir etkisi yoktur).

**Hata listesi**Roslyn çözümleyicilerinin ve statik kod analizinden ihlalleri birbirinden ayırt etmek için **araç** sütununa bakın. Araç değeri **Çözüm Gezgini**içindeki çözümleyici derlemelerinden biriyle eşleşiyorsa (örneğin, **Microsoft. Codequality. çözümleyiciler**), Ihlalin bir Roslyn çözümleyicisinden gelir. Aksi takdirde, ihlalin statik kod analizinden kaynaklanır.

![Hata Listesi araç sütunu](media/code-analysis-tool-in-error-list.png)

> [!TIP]
> Bir proje dosyasındaki **RunCodeAnalysis** MSBuild özelliği yalnızca statik kod analizi için geçerlidir. Çözümleyiciler yüklerseniz, derleme sonrasında statik kod analizinin çalıştırılmasını engellemek için **RunCodeAnalysis** öğesini proje dosyanızda **false** olarak ayarlayın.
>
> ```xml
> <RunCodeAnalysis>false</RunCodeAnalysis>
> ```

## <a name="nuget-package-versus-vsix-extension"></a>NuGet paketi ve VSıX uzantısı

.NET Compiler Platform Çözümleyicileri, bir NuGet paketi veya Visual Studio uzantısı olarak Visual Studio uzantısı aracılığıyla her proje için yüklenebilir. Bu iki çözümleyici [yükleme](../code-quality/install-roslyn-analyzers.md)yöntemi arasında bazı önemli davranış farklılıkları vardır.

### <a name="scope"></a>Kapsam

Çözümleyiciler Visual Studio uzantısı olarak yüklerseniz, çözüm düzeyinde Visual Studio 'nun tüm örneklerine uygulanır. Çözümleyicileri, tercih edilen yöntemi olan bir NuGet paketi olarak yüklerseniz, yalnızca NuGet paketinin yüklendiği proje için geçerlidir. Ekip ortamlarında, NuGet paketleri olarak yüklenen çözümleyiciler, o projede çalışan *tüm geliştiriciler* için kapsamdadır.

### <a name="build-errors"></a>Derleme hataları

Komut satırı veya bir sürekli tümleştirme (CI) yapısının parçası olarak, derleme zamanında uygulanan kuralların uygulanmasını sağlamak için, Çözümleyicileri bir NuGet paketi olarak yükler. Çözümleyici uyarıları ve hataları, çözümleyiciler bir uzantı olarak yüklerseniz derleme raporunda gösterilmez.

Aşağıdaki ekran görüntüsünde, bir çözümleyici kuralı ihlali içeren bir proje oluşturmanın komut satırı derleme çıkışı gösterilmektedir:

![Kural ihlali ile MSBuild çıkışı](media/command-line-build-analyzers.png)

### <a name="rule-severity"></a>Kural önem derecesi

Visual Studio uzantısı olarak yüklenen çözümleyicilerin kurallarının önem derecesini ayarlayamazsınız. [Kural önem derecesini](../code-quality/use-roslyn-analyzers.md#rule-severity)yapılandırmak için Çözümleyicileri bir NuGet paketi olarak yükler.

## <a name="categories"></a>Kategoriler

Aşağıda, kodunuzun çözümlenmesine yardımcı olan farklı çözümleyiciler türleri verilmiştir:

- Microsoft 'un önerilen çözümleyiciler: [FxCop çözümleyicileri](../code-quality/fxcop-analyzers.yml)
- Visual Studio IDE Çözümleyicileri: [EditorConfig](../ide/code-styles-and-code-cleanup.md)
- Üçüncü taraf Çözümleyicileri: [StyleCop](https://www.nuget.org/packages/StyleCop.Analyzers/), [roslynator](https://www.nuget.org/packages/Roslynator/), [xUnit Çözümleyicileri](https://www.nuget.org/packages/xunit.analyzers/), [sonar Çözümleyicisi](https://www.nuget.org/packages/SonarAnalyzer.CSharp/)

## <a name="next-steps"></a>Sonraki adımlar

> [!div class="nextstepaction"]
> [Visual Studio 'da Roslyn çözümleyiciler yüklemesi](../code-quality/install-roslyn-analyzers.md)

> [!div class="nextstepaction"]
> [Visual Studio 'da Roslyn Çözümleyicileri kullanma](../code-quality/use-roslyn-analyzers.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Çözümleyiciler SSS](analyzers-faq.md)
- [Kendi Roslyn çözümleyicinizi yazma](../extensibility/getting-started-with-roslyn-analyzers.md)
- [.NET Compiler Platform SDK](/dotnet/csharp/roslyn-sdk/)
