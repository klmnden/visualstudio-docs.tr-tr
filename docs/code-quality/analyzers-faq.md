---
title: EditorConfig ve çözümleyiciler
ms.date: 03/11/2019
ms.topic: conceptual
helpviewer_keywords:
- analyzers, faq
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ae41d9ac30567a32780af422c3af1e2b0d6a63ae
ms.sourcegitcommit: b761a4a457646d04adfda510c8837734ee4d8f17
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/12/2019
ms.locfileid: "70929773"
---
# <a name="code-analysis-faq"></a>Kod Analizi hakkında SSS

Bu sayfa, Visual Studio 'da .NET Compiler Platform tabanlı kod analizi hakkında sık sorulan bazı soruların yanıtlarını içerir.

## <a name="code-analysis-versus-editorconfig"></a>Kod Analizi ve EditorConfig karşılaştırması

**S**: Kod stilini denetlemek için kod analizini veya EditorConfig 'i kullanmalıdır mi?

Y: Kod Analizi ve. editorconfig dosyaları el ile çalışır. [Bir. editorconfig dosyasında](../ide/editorconfig-code-style-settings-reference.md) veya [metin düzenleyici seçenekleri](../ide/code-styles-and-code-cleanup.md) sayfasında kod stilleri tanımladığınızda aslında Visual Studio 'da yerleşik olarak bulunan kod Çözümleyicileri yapılandırılırsınız. EditorConfig dosyaları, [FxCop çözümleyicileri](configure-fxcop-analyzers.md)gibi bazı NuGet çözümleyici paketlerini yapılandırmak için de kullanılabilir.

## <a name="editorconfig-versus-rule-sets"></a>EditorConfig ve kural kümeleri

**S**: Bir kural kümesi veya. editorconfig dosyası kullanarak çözümleyiciler yapılandırmam gerekir mi?

Y: Kural kümeleri ve. editorconfig dosyaları, Çözümleyicileri yapılandırmanın birbirini dışlamalı yollarıdır. Bunlar arada bulunabilir. [Kural kümeleri](analyzer-rule-sets.md) kuralları etkinleştirip devre dışı bırakmanızı ve bunların önem derecesini ayarlamanıza olanak sağlar. EditorConfig dosyaları, kuralları yapılandırmak için başka yollar sunar. FxCop çözümleyicileri için. editorconfig dosyaları [hangi kod türlerini analiz edeceğinizi tanımlamanızı](fxcop-analyzer-options.md)sağlar. Visual Studio 'da yerleşik olan çözümleyiciler için. editorconfig dosyaları bir kod temeli için [tercih edilen kod stillerini tanımlamanıza](../ide/editorconfig-code-style-settings-reference.md) olanak sağlar.

Kural kümelerine ve. editorconfig dosyalarına ek olarak, bazı çözümleyiciler, C# ve vb derleyicileri için [ek dosyalar](../ide/build-actions.md#build-action-values) olarak işaretlenen metin dosyaları kullanılarak yapılandırılır.

> [!NOTE]
> EditorConfig dosyaları eski Analizi yapılandırmak için kullanılamaz, ancak kural kümeleri olabilir.

## <a name="code-analysis-in-ci-builds"></a>CI Derlemeleriyle kod analizi

**S**: .NET Compiler Platform tabanlı kod analizi sürekli tümleştirme (CI) Derlemeleriyle çalışıyor mu?

Y: Evet. Bir NuGet paketinden yüklenen çözümleyiciler için, bu kurallar bir CI derlemesi de dahil olmak üzere [derleme zamanında zorlanır](roslyn-analyzers-overview.md#build-errors). CI 'de kullanılan çözümleyiciler, kural [kümelerinden](analyzer-rule-sets.md) ve [. editorconfig dosyalarından](configure-fxcop-analyzers.md)gelen kural yapılandırmasına göre oluşturulur. Şu anda, Visual Studio 'da yerleşik olarak bulunan kod Çözümleyicileri bir NuGet paketi olarak kullanılamaz ve bu nedenle bu kurallar bir CI derlemesinde öngörülenebilir değildir.

## <a name="ide-analyzers-versus-stylecop"></a>IDE Çözümleyicileri ve StyleCop karşılaştırması

**S**: Visual Studio IDE kod Çözümleyicileri ve StyleCop Çözümleyicileri arasındaki fark nedir?

Y: Visual Studio IDE, hem kod stili hem de kalite sorunlarına yönelik yerleşik çözümleyiciler içerir. Bu kurallar, sunulan yeni dil özelliklerini kullanmanıza ve kodunuzun bakımlılığını iyileştirmenize yardımcı olur. IDE Çözümleyicileri her bir Visual Studio sürümüyle sürekli olarak güncelleştirilir.

[StyleCop Çözümleyicileri](https://github.com/DotNetAnalyzers/StyleCopAnalyzers) , kodunuzda stil tutarlılığını denetleyen bir NuGet paketi olarak yüklenen üçüncü taraf Çözümleyicileri. Genel olarak, StyleCop kuralları bir kod tabanı için kişisel tercihlerinizi, başka bir stil önermeksizin ayarlamanıza olanak sağlar.

## <a name="code-analyzers-versus-legacy-analysis"></a>Kod Çözümleyicileri ve eski analizler

**S**: Eski analiz ve .NET Compiler Platform tabanlı kod analizi arasındaki fark nedir?

Y **: .net Compiler platform**tabanlı kod analizi, kaynak kodu gerçek zamanlı ve derleme sırasında analiz ederken, eski analiz derleme tamamlandıktan sonra ikili dosyaları analiz eder. Daha fazla bilgi için, bkz. [.net Compiler platform tabanlı analizler, eski analizler](roslyn-analyzers-overview.md#net-compiler-platform-based-analysis-versus-legacy-analysis) ve [FxCop çözümleyicileri hakkında SSS](fxcop-analyzers-faq.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Çözümleyiciler genel bakış](roslyn-analyzers-overview.md)
- [Kodlama kuralı ayarlarına EditorConfig için .NET](../ide/editorconfig-code-style-settings-reference.md)