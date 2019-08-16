---
title: Editorconfig kullanarak FxCop çözümleyicileri yapılandırma
ms.date: 03/11/2019
ms.topic: conceptual
helpviewer_keywords:
- FxCop analyzers, configuring
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 09d5fb41648a2cd2dbd844bfb0fa426fa704042f
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69551152"
---
# <a name="configure-fxcop-analyzers"></a>FxCop çözümleyicileri yapılandırma

[FxCop çözümleyicileri](install-fxcop-analyzers.md) , eski analizler tarafından .net Compiler platform tabanlı kod Çözümleyicileri ' ne dönüştürülmüş en önemli "FxCop" kurallarından oluşur. FxCop kod Çözümleyicileri 'ni iki şekilde yapılandırabilirsiniz:

- Kural [kümesiyle](#fxcop-analyzer-rule-sets), kuralı etkinleştirmenizi veya devre dışı bırakmanızı ve tek tek kural ihlalleri için önem derecesini ayarlamanıza imkan tanır.

- Bir [. editorconfig dosyası](#editorconfig-file)aracılığıyla [Microsoft. CodeAnalysis. fxcopçözümleyiciler](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers) NuGet paketinin 2.6.3 sürümünden başlayarak. [Yapılandırılabilir seçenekler](fxcop-analyzer-options.md) , kod tabanınızın hangi bölümlerinin çözümlenmesini daraltmanızı sağlar.

> [!TIP]
> Eski analiz ve FxCop çözümleyicileri arasındaki farklar hakkında daha fazla bilgi için bkz. [FxCop ÇÖZÜMLEYICILERI SSS](fxcop-analyzers-faq.md).

## <a name="fxcop-analyzer-rule-sets"></a>FxCop Çözümleyicisi kural kümeleri

FxCop çözümleyicileri yapılandırmanın bir yolu, bir XML *kural kümesi*kullanmaktır. Bir kural kümesi, hedeflenen sorunları ve belirli koşulları belirleyen kod analizi kurallarının bir gruplandırmasıdır. Kural kümeleri kuralı etkinleştirmenizi veya devre dışı bırakmanızı ve tek tek kural ihlalleri için önem derecesini ayarlamanıza olanak sağlar.

FxCop Çözümleyicisi NuGet paketi aşağıdaki kural kategorileri için önceden tanımlanmış kural kümelerini içerir:

- tasarlama
- belgeler
- bakım
- adlandırma
- performans
- güvenilirlik
- güvenlik
- kullanım

Daha fazla bilgi için bkz. [kod Çözümleyicileri Için kural kümeleri](analyzer-rule-sets.md).

## <a name="editorconfig-file"></a>EditorConfig dosyası

Bir [. editorconfig](https://editorconfig.org) dosyasına anahtar-değer çiftleri ekleyerek çözümleyici kurallarını yapılandırabilirsiniz. Bir yapılandırma dosyası [bir projeye özgü](#per-project-configuration) olabilir veya iki ya da daha fazla proje arasında [paylaşılabilir](#shared-configuration) .

### <a name="per-project-configuration"></a>Proje başına yapılandırma

Belirli bir proje için. editorconfig tabanlı çözümleyici yapılandırmasını etkinleştirmek üzere, projenin kök dizinine bir *. editorconfig* dosyası ekleyin.

> [!TIP]
> **Çözüm Gezgini** ' de projeye sağ tıklayıp**Yeni öğe** **Ekle** > ' yi seçerek projenize bir. editorconfig dosyası ekleyebilirsiniz. **Yeni öğe Ekle** penceresinde, arama kutusuna **editorconfig** yazın. **Editorconfig dosyası (varsayılan)** şablonunu seçin ve **Ekle**' yi seçin.
>
> ![Visual Studio 'daki projeye editorconfig öğesi ekleme](media/add-editorconfig-file.png)

Şu anda, farklı dizin düzeylerinde bulunan (örneğin, çözüm ve proje düzeyi) "birleştirme". editorconfig dosyaları için hiyerarşik bir destek yoktur.

### <a name="shared-configuration"></a>Paylaşılan yapılandırma

İki veya daha fazla proje arasında çözümleyici yapılandırması için bir. editorconfig dosyası paylaşabilirsiniz, ancak bazı ek adımlar gerektirir.

1. *. Editorconfig* dosyasını ortak bir konuma kaydedin.

2. Aşağıdaki içeriğe sahip bir *. props* dosyası oluşturun:

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

3. Önceki adımda oluşturduğunuz *. props* dosyasını içeri aktarmak için *. csproj* veya *. vbproj* dosyanıza bir satır ekleyin. Bu satır, FxCop Çözümleyicisi *. props* dosyalarını içeri aktararak herhangi bir satırdan önce yerleştirilmelidir. Örneğin,. props dosyanız *editorconfig. props*olarak adlandırılmışsa:

   ```xml
   ...
   <Import Project="..\..\editorconfig.props" Condition="Exists('..\..\editorconfig.props')" />
   <Import Project="..\packages\Microsoft.CodeAnalysis.FxCopAnalyzers.2.6.3\build\Microsoft.CodeAnalysis.FxCopAnalyzers.props" Condition="Exists('..\packages\Microsoft.CodeAnalysis.FxCopAnalyzers.2.6.3\build\Microsoft.CodeAnalysis.FxCopAnalyzers.props')" />
   ...
   ```

4. Projeyi yeniden yükleyin.

> [!NOTE]
> Eski FxCop kurallarını bir. editorconfig dosyası kullanarak yapılandıramazsınız.

## <a name="option-scopes"></a>Seçenek kapsamları

Her seçenek, kural kategorisi (örneğin, adlandırma veya tasarım) veya belirli bir kural için tüm kurallar için yapılandırılabilir.

### <a name="all-rules"></a>Tüm kurallar

Tüm kurallar için bir seçeneği yapılandırmak için sözdizimi aşağıdaki gibidir:

|Sözdizimi|Örnek|
|-|-|
| dotnet_code_quality. OptionName = OptionValue | `dotnet_code_quality.api_surface = public` |

### <a name="category-of-rules"></a>Kuralların kategorisi

Bir kural *kategorisi* (adlandırma, tasarım veya performans gibi) için bir seçenek yapılandırmanın sözdizimi aşağıdaki gibidir:

|Sözdizimi|Örnek|
|-|-|
| dotnet_code_quality. RuleCategory. OptionName = OptionValue | `dotnet_code_quality.Naming.api_surface = public` |

### <a name="specific-rule"></a>Belirli kural

Belirli bir kural için bir seçeneği yapılandırmanın sözdizimi aşağıdaki gibidir:

|Sözdizimi|Örnek|
|-|-|
| dotnet_code_quality. RuleId. OptionName = OptionValue | `dotnet_code_quality.CA1040.api_surface = public` |

## <a name="see-also"></a>Ayrıca bkz.

- [Çözümleyici yapılandırması](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md)
- [FxCop çözümleyicileri](install-fxcop-analyzers.md)
- [EditorConfig için .NET kodlama kuralları](../ide/editorconfig-code-style-settings-reference.md)
