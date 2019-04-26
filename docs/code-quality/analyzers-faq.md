---
title: EditorConfig Çözümleyicileri karşılaştırması
ms.date: 03/11/2019
ms.topic: conceptual
helpviewer_keywords:
- analyzers, faq
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bec9296f15c48cf3b327c78cd0ce7d57adafa002
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62571478"
---
# <a name="analyzers-faq"></a>Çözümleyiciler hakkında SSS

Bu sayfa, Visual Studio'da Roslyn Çözümleyicileri hakkında bazı sık sorulan soruların yanıtlarını içerir.

## <a name="roslyn-analyzers-versus-editorconfig"></a>Roslyn çözümleyicilerini .editorconfig karşılaştırması

**Q**: Kod stili için Roslyn Çözümleyicileri veya .editorconfig kullanmalıyım?

**A**: Roslyn Çözümleyicileri ve .editorconfig dosyalarını elle yakından çalışır. Kod stilleri tanımladığınızda [.editorconfig dosyasındaki](../ide/editorconfig-code-style-settings-reference.md) veya [metin düzenleyici seçenekleri](../ide/code-styles-and-quick-actions.md) sayfasında, Visual Studio'da yerleşik olarak bulunan Roslyn Çözümleyicileri gerçekten yapılandırmakta olduğunuz. EditorConfig dosyaları da bazı üçüncü taraf Çözümleyicisi paketleri gibi yapılandırmak için kullanılabilir [FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="editorconfig-versus-rule-sets"></a>EditorConfig kural kümelerinin karşılaştırması

**Q**: Ben bir kural kümesi veya .editorconfig dosyasındaki kullanarak my Çözümleyicileri yapılandırmamız gerekir mi?

**A**: Kural kümeleri ve .editorconfig dosyalarını Çözümleyicileri yapılandırmak için birbirini dışlayan yolları açıklanmıştır. Bunlar bir arada bulunabilir. [Kural kümeleri](analyzer-rule-sets.md) etkinleştirmek ve kuralları devre dışı bırakılır ve bunların önem derecesinin sağlar. EditorConfig dosyaları kurallarını yapılandırmak için başka yollar sunar. .Editorconfig dosyalarını FxCop Çözümleyicileri için izin [analiz etmek için kod türlerini tanımlamak](fxcop-analyzer-options.md). .Editorconfig dosyalarını Visual Studio'da yerleşik olarak bulunan Çözümleyicileri için izin [tercih edilen kod stillerini tanımlamak](../ide/editorconfig-code-style-settings-reference.md) bir kod temeli için.

Kural kümeleri ve .editorconfig dosyalarını ek olarak, bazı üçüncü taraf Çözümleyicileri metin dosyaları olarak işaretlenmiş kullanılarak yapılandırılan [ek dosyalar](../ide/build-actions.md#build-action-values) için C# ve VB derleyicileri.

> [!NOTE]
> Kural kümeleri olabilir ancak EditorConfig dosyaları statik kod analizi kurallarını yapılandırmak için kullanılamaz.

## <a name="analyzers-in-ci-builds"></a>CI yapılarında çözümleyiciler

**Q**: Çözümleyiciler içinde sürekli tümleştirme (CI) derlemeleri çalışır?

**A**: Evet. Bir NuGet paketinden yüklenen Çözümleyicileri bu kurallardır [derleme zorunlu](roslyn-analyzers-overview.md#build-errors)CI derleme sırasında dahil. Hem CI derlemeleri saygı kural yapılandırmasında kullanılan Çözümleyicileri [kural kümeleri](analyzer-rule-sets.md) ve [.editorconfig dosyalarını](configure-fxcop-analyzers.md). Şu anda, Visual Studio'da yerleşik olarak bulunan kod Çözümleyicileri bir NuGet paketi olarak kullanılabilir değil ve bu nedenle bu kuralları bir CI yapı içinde uygulanabilir değildir.

## <a name="ide-analyzers-versus-stylecop"></a>IDE Çözümleyicileri StyleCop karşılaştırması

**Q**: Visual Studio IDE, kod Çözümleyicileri ve StyleCop Çözümleyicileri arasındaki fark nedir?

**A**: Visual Studio IDE, her iki kod stili ve kalite sorunları için yerleşik Çözümleyicileri içerir. Bu kurallar yardımcı sunulan ve sürdürülebilirliği kodunuzu geliştirmek gibi yeni dil özellikleri kullanın. IDE Çözümleyicileri sürekli güncelleştirilen her Visual Studio sürümü ile.

[StyleCop Çözümleyicileri](https://github.com/DotNetAnalyzers/StyleCopAnalyzers) olan kod stili tutarlılık denetimi bir NuGet paketi olarak yüklenen üçüncü taraf Çözümleyicileri. Genel olarak, StyleCop kurallar, kişisel bir kod için temel bir stil başka bir öneren olmadan Tercihler olanak sağlar.

## <a name="analyzers-versus-static-code-analysis"></a>Statik kod analizi ve çözümleyiciler

**Q**: Çözümleyicileri ve statik kod analizi arasındaki fark nedir?

**A**: Statik kod analizi, derleme tamamlandıktan sonra ikili dosyaları analiz eder, oysa Çözümleyicileri gerçek zamanlı ve derleme sırasında kaynak kodu analiz edin. Daha fazla bilgi için [Roslyn Çözümleyicileri statik kod analizi karşılaştırması](roslyn-analyzers-overview.md#roslyn-analyzers-vs-static-code-analysis) ve [FxCop Çözümleyicileri SSS](fxcop-analyzers-faq.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Çözümleyiciler genel bakış](roslyn-analyzers-overview.md)
- [Kodlama kuralı ayarlarına EditorConfig için .NET](../ide/editorconfig-code-style-settings-reference.md)