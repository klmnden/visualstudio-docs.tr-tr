---
title: Çözümleyicisi için kural kümeleri
ms.date: 04/22/2019
ms.topic: conceptual
helpviewer_keywords:
- analyzers, rule sets
- rule sets for analyzers
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 696e6bd46c17054494be2ea0e0f2a1af4fd703d7
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65675481"
---
# <a name="rule-sets-for-roslyn-analyzers"></a>Roslyn çözümleyicilerini için kural kümeleri

Önceden tanımlanmış kural kümeleri bazı NuGet Çözümleyicisi paketleri dahil edilir. Örneğin, eklenen kural kümesi [Microsoft.CodeAnalysis.FxCopAnalyzers](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers/) NuGet Çözümleyicisi paketi (sürüm 2.6.2 başlayarak) etkinleştirmek veya adlandırma, güvenlik gibi kategorilerine göre kuralları devre dışı bırakın veya performans. Kural kümeleri kullanma, kuralın belirli bir kategoriye ait kural ihlalleri hızlıca görmek kolaylaştırır.

Eski "FxCop" statik kod analizi için Roslyn Çözümleyicileri geçiriyorsanız, bu kural kümeleri, daha önce kullandığınız aynı kuralı yapılandırmaları kullanmaya devam etmek etkinleştirin.

## <a name="use-analyzer-rule-sets"></a>Çözümleyicisi için kural kümeleri kullanma

Çalıştırdıktan sonra [NuGet Çözümleyicisi paket yükleme](install-roslyn-analyzers.md), önceden tanımlanmış kural kümesi bulun, *rulesets* dizin. Örneğin, başvurulan, `Microsoft.CodeAnalysis.FxCopAnalyzers` Çözümleyicisi paketini ve ardından bulabilir, *rulesets* dizin konumunda *% USERPROFILE %\\.nuget\packages\microsoft.codeanalysis.fxcopanalyzers\\ \<sürüm\>\rulesets*. Buradan, bir veya daha fazla rulesets kopyalayıp bunları doğrudan ya da Visual Studio projenizi içeren dizine **Çözüm Gezgini**.

Ayrıca [önceden tanımlanmış kural kümesi özelleştirme](how-to-create-a-custom-rule-set.md) tercihinize. Örneğin, böylece hatalar veya uyarılar olarak ihlalleri görünür bir veya daha fazla kural önem derecesi değiştirebilirsiniz **hata listesi**.

## <a name="set-the-active-rule-set"></a>Etkin kural kümesi ayarlama

Etkin kural kümesini ayarlama işlemi, bir .NET Core/.NET Standard veya .NET Framework projesi olmasına bağlı olarak biraz farklıdır.

### <a name="net-core"></a>.NET Core

.NET Core veya .NET Standard projelerine analizi için etkin kural kümesi bir kural oluşturmak için el ile eklemeniz **CodeAnalysisRuleSet** proje dosyanıza özelliği. Örneğin, aşağıdaki kod parçacığı kümeleri kod `HelloWorld.ruleset` etkin kural olarak ayarlayın.

```xml
<PropertyGroup Condition=" '$(Configuration)|$(Platform)' == 'Debug|AnyCPU' ">
  ...
  <CodeAnalysisRuleSet>HelloWorld.ruleset</CodeAnalysisRuleSet>
</PropertyGroup>
```

### <a name="net-framework"></a>.NET Framework

.NET Framework projelerindeki analizi için etkin kural kümesi bir kural oluşturmak için projeye sağ **Çözüm Gezgini** ve **özellikleri**. Proje özellik sayfaları'nda seçin **Kod Analizi** sekmesi. Altında **bu kural kümesini Çalıştır**seçin **Gözat**ve ardından proje dizinine kopyalanır istenen kural kümesi seçin. Artık yalnızca seçili kural kümesinde etkin bu kuralları için kural ihlalleri görürsünüz.

## <a name="available-rule-sets"></a>Kullanılabilir kural kümeleri

Paketteki tüm kuralları etkiler üç rulesets önceden tanımlanmış Çözümleyicisi kural kümelerini Ekle&mdash;tümünü sağlayan, Tümünü devre dışı bırakan bir, diğeri, önem derecesi ve etkinleştirme her kuralın varsayılan ayarlarını kabul eder:

- AllRulesEnabled.ruleset
- AllRulesDisabled.ruleset
- AllRulesDefault.ruleset

Ayrıca, performans veya güvenlik gibi paket kurallarında her kategorisi için iki kural kümesi vardır. Bir kural kümesi kategorisi için tüm kuralları etkinleştirir ve varsayılan önem derecesi ve etkinleştirme ayarları kategorideki her kural için bir kural kümesi geliştirir.

[Microsoft.CodeAnalysis.FxCopAnalyzers](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers/) NuGet Çözümleyicisi paketi hangi eşleşme kuralını eski "FxCop" statik kod analizi için kullanılabilen ayarlar aşağıdaki kategoriler için kural kümeleri içerir:

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
- [.NET derleyici platformu Çözümleyicileri genel bakış](roslyn-analyzers-overview.md)
- [Çözümleyicilerini yükleme](install-roslyn-analyzers.md)
- [Çözümleyiciler kullanın](use-roslyn-analyzers.md)
- [Kural Kod Analizi kurallarını gruplandırmak için kümeleri kullanma](using-rule-sets-to-group-code-analysis-rules.md)
