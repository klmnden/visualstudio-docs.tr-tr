---
title: FxCop Çözümleyicisi kural kümeleri
ms.date: 09/23/2019
ms.topic: conceptual
helpviewer_keywords:
- analyzer packages, rule sets
- rule sets for analyzers
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: da1567dd088ecc060f031e59827ff33024e9e955
ms.sourcegitcommit: 88f576ac32af31613c1a10c1548275e1ce029f4f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "71185957"
---
# <a name="rule-sets-for-analyzer-packages"></a>Çözümleyici paketleri için kural kümeleri

Önceden tanımlanmış kural kümeleri, bazı NuGet çözümleyici paketlerine dahildir. Örneğin, [Microsoft. CodeAnalysis. Fxcopçözümleyiciler](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers/) NuGet çözümleyici paketine (sürüm 2.6.2 Critical ' den başlayarak) dahil edilen kural kümeleri, güvenlik, adlandırma veya performans gibi kategorilerine göre kuralları etkinleştirir veya devre dışı bırakır. Kural kümelerinin kullanılması, yalnızca belirli bir kural kategorisiyle ilgili olan kural ihlallerini hızlıca görmeyi kolaylaştırır.

Bir kural kümesi, hedeflenen sorunları ve belirli koşulları belirleyen kod analizi kurallarının bir gruplandırmasıdır. Kural kümeleri kuralları etkinleştirmenizi veya devre dışı bırakmanızı ve tek tek kural ihlalleri için önem derecesini ayarlamanıza olanak sağlar. FxCop Çözümleyicisi NuGet paketi aşağıdaki kural kategorileri için önceden tanımlanmış kural kümelerini içerir:

- tasarlama
- belgeler
- bakım
- adlandırma
- performans
- güvenilirlik
- güvenlik
- kullanım

Eski "FxCop" analizinden .NET Compiler Platform tabanlı kod çözümlemesine geçiş yapıyorsanız, bu kural kümeleri, [daha önce kullandığınız](rule-set-reference.md)şekilde benzer kural yapılandırmalarının kullanılmasına devam etmeyi sağlar.

## <a name="use-analyzer-package-rule-sets"></a>Çözümleyici paketi kural kümelerini kullanma

[NuGet Çözümleyicisi paketini](install-roslyn-analyzers.md)yükledikten sonra, *RuleSets* dizininde önceden tanımlanmış kural kümesini bulun. Örneğin, `Microsoft.CodeAnalysis.FxCopAnalyzers` çözümleyici paketine başvuruluyorsa, *RuleSets* dizinini *% USERPROFILE\\%. nuget\packages\microsoft.CodeAnalysis.fxcopanalyzers\\\<sürümünde bulabilirsiniz \>\rulesets*. Buradan, bir veya daha fazla RuleSets 'i kopyalayın ve bunları Visual Studio projenizi içeren dizine yapıştırın veya doğrudan **Çözüm Gezgini**.

Ayrıca, [önceden tanımlanmış bir kural kümesini](how-to-create-a-custom-rule-set.md) tercih etmeniz için özelleştirebilirsiniz. Örneğin, bir veya daha fazla kuralın önem derecesini değiştirerek ihlallerin **hata listesi**hata veya uyarı olarak görünmesini sağlayabilirsiniz.

## <a name="set-the-active-rule-set"></a>Etkin kural kümesini ayarla

Etkin kural kümesini ayarlama işlemi, .NET Core/. NET Standard projeniz veya .NET Framework projeniz olmasına bağlı olarak biraz farklıdır.

### <a name="net-core"></a>.NET Core

Bir kuralı, .NET Core veya .NET Standard projelerinde analiz için etkin kural kümesini ayarlamak için, **CodeAnalysisRuleSet** özelliğini proje dosyanıza el ile ekleyin. Örneğin, aşağıdaki kod parçacığı etkin kural kümesi `HelloWorld.ruleset` olarak ayarlanır.

```xml
<PropertyGroup Condition=" '$(Configuration)|$(Platform)' == 'Debug|AnyCPU' ">
  ...
  <CodeAnalysisRuleSet>HelloWorld.ruleset</CodeAnalysisRuleSet>
</PropertyGroup>
```

### <a name="net-framework"></a>.NET Framework

Bir kuralı .NET Framework projelerinde analiz için etkin kural kümesini ayarlamak için, **Çözüm Gezgini** içindeki projeye sağ tıklayın ve **Özellikler**' i seçin. Proje özelliği sayfalarında **Kod Analizi** sekmesini seçin. **Bu kural kümesini Çalıştır**' ın altında, **Araştır**' ı seçin ve ardından proje dizinine kopyaladığınız istenen kural kümesini seçin. Şimdi yalnızca seçili kural kümesinde etkinleştirilen kuralların kural ihlallerini görürsünüz.

## <a name="available-rule-sets"></a>Kullanılabilir kural kümeleri

Önceden tanımlı çözümleyici kural kümeleri, paketteki&mdash;tüm kuralları etkileyen, bunların tümünü devre dışı bırakan ve her kuralın varsayılan önem derecesini ve etkinleştirme ayarlarını yapan bir tane olan üç RuleSet içerir:

- AllRulesEnabled. RuleSet
- Allkuraldevre dışı. RuleSet
- Allkurallarını varsayılan. RuleSet

Ayrıca, paketteki her bir kural kategorisi için performans veya güvenlik gibi iki kural kümesi vardır. Bir kural kümesi kategori için tüm kurallara izin verir ve bir kural kümesi, kategorideki her bir kural için varsayılan önem derecesini ve etkinleştirme ayarlarını kabul eder.

[Microsoft. CodeAnalysis. Fxcopçözümleyiciler](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers/) NuGet Çözümleyicisi paketi aşağıdaki kategorilerin kural kümelerini içerir:

- tasarlama
- belgeler
- bakım
- adlandırma
- performans
- güvenilirlik
- güvenlik
- kullanım

## <a name="see-also"></a>Ayrıca bkz.

- [Çözümleyiciler SSS](analyzers-faq.md)
- [.NET Compiler Platform çözümleyicilerine genel bakış](roslyn-analyzers-overview.md)
- [Çözümleyicileri yükleiciler](install-roslyn-analyzers.md)
- [Çözümleyicileri yapılandırma](use-roslyn-analyzers.md)
- [Kod analizi kurallarını gruplandırmak için kural kümeleri kullanma](using-rule-sets-to-group-code-analysis-rules.md)
