---
title: FxCop Çözümleyicileri editorconfig kullanarak yapılandırma
ms.date: 03/11/2019
ms.topic: conceptual
helpviewer_keywords:
- FxCop analyzers, configuring
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: ac751b7ec130b6bfbb18752c02b491b6c342f172
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62816940"
---
# <a name="configure-fxcop-analyzers"></a>FxCop Çözümleyicileri yapılandırın

[FxCop Çözümleyicileri](install-fxcop-analyzers.md) statik kod analizi için Roslyn Çözümleyicileri dönüştürülür, en önemli "FxCop" kurallardan oluşur. FxCop kod Çözümleyicileri iki yolla yapılandırabilirsiniz:

- İle bir [kural kümesi](#fxcop-analyzer-rule-sets), olanak sağlayan etkinleştirmek veya kuralı devre dışı bırak ve bireysel kural ihlalleri açısından önem derecesini ayarlayın.

- Sürümünü 2.6.3 başlatma [Microsoft.CodeAnalysis.FxCopAnalyzers](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers) aracılığıyla NuGet paketini bir [.editorconfig dosyasındaki](#editorconfig-file). [Yapılandırılabilir seçeneklerin](fxcop-analyzer-options.md) let hangi parçalarının iyileştirmek, analiz etmek için kod tabanı.

> [!TIP]
> FxCop statik kod analizi ve FxCop Çözümleyicileri arasındaki farklar hakkında daha fazla bilgi için bkz: [FxCop Çözümleyicileri SSS](fxcop-analyzers-faq.md).

## <a name="fxcop-analyzer-rule-sets"></a>FxCop Çözümleyicisi kural kümeleri

FxCop Çözümleyicileri yapılandırmanın bir yolu olan bir XML kullanarak *kural kümesi*. Bir kural kümesi, hedeflenen sorunları ve belirli koşullar belirleyen kod analizi kuralları gruplandırmasıdır. Kural kümeleri, etkinleştirmek veya kuralı devre dışı bırak ve bireysel kural ihlalleri açısından önem derecesini ayarlayın olanak tanır.

FxCop Çözümleyicisi NuGet paketi, aşağıdaki kural kategorileri için önceden tanımlanmış kural kümesi içerir:

- tasarlama
- belgeler
- bakım
- adlandırma
- performans
- güvenilirlik
- güvenlik
- kullanım

Daha fazla bilgi için [kural kümeleri için Roslyn Çözümleyicileri](analyzer-rule-sets.md).

## <a name="editorconfig-file"></a>EditorConfig dosyası

Çözümleyici kuralları için anahtar-değer çiftleri ekleyerek yapılandırabileceğiniz bir [.editorconfig](https://editorconfig.org) dosya. Bir yapılandırma dosyası olabilir [belirli bir projeye](#per-project-configuration) veya olabilir [paylaşılan](#shared-configuration) iki veya daha fazla proje arasında.

### <a name="per-project-configuration"></a>Proje başına yapılandırma

Belirli bir proje için yapılandırma Çözümleyicisi .editorconfig tabanlı etkinleştirmek için eklemeniz bir *.editorconfig* dosya projenin kök dizini.

> [!TIP]
> Projeye sağ tıklayarak .editorconfig dosyayı projenize ekleyebilirsiniz **Çözüm Gezgini** seçerek **Ekle** > **yeni öğe**. İçinde **Yeni Öğe Ekle** penceresinde girin **editorconfig** arama kutusuna. Seçin **editorconfig dosyası (varsayılan)** şablonu seçip **Ekle**.
>
> ![Visual Studio'da proje editorconfig öğe ekleme](media/add-editorconfig-file.png)

Şu anda hiyerarşik desteği yoktur ".editorconfig birleştirme" dosyası için farklı bir dizine düzeyde, örneğin, çözüm ve proje düzeyinde mevcut.

### <a name="shared-configuration"></a>Paylaşılan yapılandırma

İki veya daha fazla proje arasında Çözümleyicisi yapılandırması için bir .editorconfig dosyasındaki paylaşabilirsiniz, ancak bazı ek adımlar gerektirir.

1. Kaydet *.editorconfig* ortak bir konuma dosya.

2. Oluşturma bir *.props* dosya aşağıdaki içeriğe sahip:

   ```xml
   <Project DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
     <PropertyGroup>
       <SkipDefaultEditorConfigAsAdditionalFile>true</SkipDefaultEditorConfigAsAdditionalFile>
     </PropertyGroup>
     <ItemGroup Condition="Exists('<your path>\.editorconfig')" >
       <AdditionalFiles Include="<your path>\.editorconfig" />
     </ItemGroup>
   </Project>
   ```

3. İçin bir satır ekleyin, *.csproj* veya *.vbproj* içeri aktarmak için dosya *.props* önceki adımda oluşturulan dosya. Bu satırı FxCop Çözümleyicisi alma satırları önce yerleştirilmelidir *.props* dosyaları. Örneğin, .props dosyası ise, *editorconfig.props*:

   ```xml
   ...
   <Import Project="..\..\editorconfig.props" Condition="Exists('..\..\editorconfig.props')" />
   <Import Project="..\packages\Microsoft.CodeAnalysis.FxCopAnalyzers.2.6.3\build\Microsoft.CodeAnalysis.FxCopAnalyzers.props" Condition="Exists('..\packages\Microsoft.CodeAnalysis.FxCopAnalyzers.2.6.3\build\Microsoft.CodeAnalysis.FxCopAnalyzers.props')" />
   ...
   ```

4. Projeyi yeniden yükleyin.

> [!NOTE]
> .Editorconfig dosyasındaki kullanarak eski FxCop kuralı (statik kod analizi FxCop) yapılandıramazsınız.

## <a name="option-scopes"></a>Seçenek kapsamları

Her seçeneği, tüm kurallar, (örneğin, adlandırma veya Tasarım) kurallarının bir kategori veya belirli bir kural için yapılandırılabilir.

### <a name="all-rules"></a>Tüm kurallar

Tüm kurallar için bir seçenek yapılandırmak için sözdizimi aşağıdaki gibidir:

|Sözdizimi|Örnek|
|-|-|
| dotnet_code_quality. SeçenekAdı OptionValue = | `dotnet_code_quality.api_surface = public` |

### <a name="category-of-rules"></a>Kural kategorisi

Yapılandırma seçeneği söz dizimi bir *kategori* (örneğin, adlandırma, tasarım veya performans) kurallar aşağıdaki gibidir:

|Sözdizimi|Örnek|
|-|-|
| dotnet_code_quality. RuleCategory.OptionName OptionValue = | `dotnet_code_quality.Naming.api_surface = public` |

### <a name="specific-rule"></a>Özel kural

Belirli bir kural için bir seçenek yapılandırmak için sözdizimi aşağıdaki gibidir:

|Sözdizimi|Örnek|
|-|-|
| dotnet_code_quality. RuleId.OptionName OptionValue = | `dotnet_code_quality.CA1040.api_surface = public` |

## <a name="see-also"></a>Ayrıca bkz.

- [Yapılandırma Çözümleyicisi](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md)
- [FxCop Çözümleyicileri](install-fxcop-analyzers.md)
