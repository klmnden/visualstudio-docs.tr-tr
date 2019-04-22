---
title: Kod ölçümleri IDE veya komut satırından oluşturun
ms.date: 11/02/2018
ms.topic: conceptual
helpviewer_keywords:
- code metrics data
- code metrics results
- code metrics [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4275e92b21289c5cf1e3243b2bc782a9e0821fde
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59232755"
---
# <a name="how-to-generate-code-metrics-data"></a>Nasıl yapılır: Kod ölçümleri verileri üretme

Kod ölçüm verileri üç şekilde oluşturabilirsiniz:

- Yükleyerek [FxCop Çözümleyicileri](#fxcop-analyzers-code-metrics-rules) ve içerdiği dört kod ölçümleri (Bakım) kurallarını etkinleştirme.

- Seçerek [ **Çözümle** > **kod ölçümlerini Hesapla** ](#calculate-code-metrics-menu-command) Visual Studio'daki menü komutu.

- Gelen [komut satırı](#command-line-code-metrics) için C# ve Visual Basic projeleri.

## <a name="fxcop-analyzers-code-metrics-rules"></a>FxCop Çözümleyicileri kod ölçümleri kuralları

[FxCopAnalyzers NuGet paketini](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers) birkaç kod ölçümleri içerir [Çözümleyicisi](roslyn-analyzers-overview.md) kuralları:

- [CA1501](ca1501-avoid-excessive-inheritance.md)
- [CA1502](ca1502-avoid-excessive-complexity.md)
- [CA1505](ca1505-avoid-unmaintainable-code.md)
- [CA1506](ca1506-avoid-excessive-class-coupling.md)

Bu kurallar varsayılan olarak devre dışıdır, ancak bunları etkinleştirebilirsiniz [ **Çözüm Gezgini** ](use-roslyn-analyzers.md#set-rule-severity-from-solution-explorer) veya bir [kural kümesi](using-rule-sets-to-group-code-analysis-rules.md) dosya. Örneğin, bir uyarı olarak CA1502 kuralını etkinleştirmek için .ruleset dosyası şu girdiyi içerecektir:

```xml
<?xml version="1.0" encoding="utf-8"?>
<RuleSet Name="Rules" Description="Rules" ToolsVersion="16.0">
  <Rules AnalyzerId="Microsoft.CodeQuality.Analyzers" RuleNamespace="Microsoft.CodeQuality.Analyzers">
    <Rule Id="CA1502" Action="Warning" />
  </Rules>
</RuleSet>
```

### <a name="configuration"></a>Yapılandırma

Başlangıçtan FxCop Çözümleyicileri kod ölçümleri kurallarında yangın paketini eşikler yapılandırabilirsiniz.

1. Bir metin dosyası oluşturun. Bu ad bir örnek olarak, *CodeMetricsConfig.txt*.

2. İstediğiniz eşikleri aşağıdaki biçimde metin dosyasına ekleyin:

   ```txt
   CA1502: 10
   ```

   Bu örnekte, kural [CA1502](ca1502-avoid-excessive-complexity.md) 10'dan büyük bir yöntemin döngüzel karmaşıklığına için yapılandırılır.

3. İçinde **özellikleri** penceresi Visual Studio'nun veya proje dosyasında işaretlemek yapılandırma dosyasının derleme eylemini [ **AdditionalFiles**](../ide/build-actions.md#build-action-values). Örneğin:

   ```xml
   <ItemGroup>
     <AdditionalFiles Include="CodeMetricsConfig.txt" />
   </ItemGroup>
   ```

## <a name="calculate-code-metrics-menu-command"></a>Menü komutunu kod ölçümlerini Hesapla

Bir veya tüm açık projeleriniz için kod ölçümleri kullanarak IDE'de oluşturma **Çözümle** > **kod ölçümlerini Hesapla** menüsü.

### <a name="generate-code-metrics-results-for-an-entire-solution"></a>Bütün bir çözüm için kod ölçümleri sonuçları oluşturma

Bütün bir çözüm için kod ölçümleri sonuçları aşağıdaki yollardan biriyle oluşturabilirsiniz:

- Menü çubuğundan seçin **Çözümle** > **kod ölçümlerini Hesapla** > **çözüm**.

- İçinde **Çözüm Gezgini**, çözüme sağ tıklayın ve ardından **kod ölçümlerini Hesapla**.

- İçinde **kod ölçümleri sonuçları** penceresinde seçin **çözüm için kod ölçümlerini Hesapla** düğmesi.

Sonuçları oluşturulur ve **kod ölçümleri sonuçları** penceresi görüntülenir. Sonuçları ayrıntılarını görüntülemek için ağaç genişletin **hiyerarşi** sütun.

### <a name="generate-code-metrics-results-for-one-or-more-projects"></a>Bir veya daha fazla proje için kod ölçümleri sonuçları oluşturma

1. İçinde **Çözüm Gezgini**, bir veya daha fazla proje seçin.

1. Menü çubuğundan seçin **Çözümle** > **kod ölçümlerini Hesapla** > **seçili projeleri için**.

Sonuçları oluşturulur ve **kod ölçümleri sonuçları** penceresi görüntülenir. Sonuçları ayrıntılarını görüntülemek için ağaç genişletin **hiyerarşi**.

::: moniker range="vs-2017"

> [!NOTE]
> **Kod ölçümlerini Hesapla** komutu, .NET Core ve .NET Standard projeleri için çalışmaz. .NET Core veya .NET Standard projesi için kod ölçümlerini hesapla için şunları yapabilirsiniz:
>
> - kod ölçümleri hesaplayın [komut satırı](#command-line-code-metrics) yerine
>
> - Yükseltme [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019)

::: moniker-end

## <a name="command-line-code-metrics"></a>Komut satırı kod ölçümleri

Komut satırı için kod ölçümleri verileri üretme C# ve Visual Basic projeleri .NET Framework, .NET Core ve .NET Standard uygulamaları için. Kod ölçümleri komut satırından çalıştırmak için yükleme [Microsoft.CodeAnalysis.Metrics NuGet paketini](#microsoftcodeanalysismetrics-nuget-package) ya da yapı [Metrics.exe](#metricsexe) yürütülebilir kendiniz.

### <a name="microsoftcodeanalysismetrics-nuget-package"></a>Microsoft.CodeAnalysis.Metrics NuGet paketi

Yükleyerek komut satırından kod ölçümleri verileri üretme en kolay yolu olan [Microsoft.CodeAnalysis.Metrics](https://www.nuget.org/packages/Microsoft.CodeAnalysis.Metrics/) NuGet paketi. Paketi yükledikten sonra Çalıştır `msbuild /t:Metrics` , proje dosyasını içeren dizinden. Örneğin:

```shell
C:\source\repos\ClassLibrary3\ClassLibrary3>msbuild /t:Metrics
Microsoft (R) Build Engine version 16.0.360-preview+g9781d96883 for .NET Framework
Copyright (C) Microsoft Corporation. All rights reserved.

Build started 1/22/2019 4:29:57 PM.
Project "C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj" on node 1 (Metrics target(s))
.
Metrics:
  C:\source\repos\ClassLibrary3\packages\Microsoft.CodeMetrics.2.6.4-ci\build\\..\Metrics\Metrics.exe /project:C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj /out:ClassLibrary3.Metrics.xml
  Loading ClassLibrary3.csproj...
  Computing code metrics for ClassLibrary3.csproj...
  Writing output to 'ClassLibrary3.Metrics.xml'...
  Completed Successfully.
Done Building Project "C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj" (Metrics target(s)).

Build succeeded.
    0 Warning(s)
    0 Error(s)
```

Çıkış dosyası adını belirterek geçersiz kılabilir `/p:MetricsOutputFile=<filename>`. Ayrıca Al [eski stil](#previous-versions) kod ölçüm verileri belirterek `/p:LEGACY_CODE_METRICS_MODE=true`. Örneğin:

```shell
C:\source\repos\ClassLibrary3\ClassLibrary3>msbuild /t:Metrics /p:LEGACY_CODE_METRICS_MODE=true /p:MetricsOutputFile="Legacy.xml"
Microsoft (R) Build Engine version 16.0.360-preview+g9781d96883 for .NET Framework
Copyright (C) Microsoft Corporation. All rights reserved.

Build started 1/22/2019 4:31:00 PM.
The "MetricsOutputFile" property is a global property, and cannot be modified.
Project "C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj" on node 1 (Metrics target(s))
.
Metrics:
  C:\source\repos\ClassLibrary3\packages\Microsoft.CodeMetrics.2.6.4-ci\build\\..\Metrics.Legacy\Metrics.Legacy.exe /project:C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj /out:Legacy.xml
  Loading ClassLibrary3.csproj...
  Computing code metrics for ClassLibrary3.csproj...
  Writing output to 'Legacy.xml'...
  Completed Successfully.
Done Building Project "C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj" (Metrics target(s)).

Build succeeded.
    0 Warning(s)
    0 Error(s)
```

### <a name="code-metrics-output"></a>Kod ölçümleri çıkışı

Oluşturulan XML çıktısı, aşağıdaki biçimi alır:

```xml
<?xml version="1.0" encoding="utf-8"?>
<CodeMetricsReport Version="1.0">
  <Targets>
    <Target Name="ConsoleApp20.csproj">
      <Assembly Name="ConsoleApp20, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null">
        <Metrics>
          <Metric Name="MaintainabilityIndex" Value="100" />
          <Metric Name="CyclomaticComplexity" Value="1" />
          <Metric Name="ClassCoupling" Value="1" />
          <Metric Name="DepthOfInheritance" Value="1" />
          <Metric Name="LinesOfCode" Value="11" />
        </Metrics>
        <Namespaces>
          <Namespace Name="ConsoleApp20">
            <Metrics>
              <Metric Name="MaintainabilityIndex" Value="100" />
              <Metric Name="CyclomaticComplexity" Value="1" />
              <Metric Name="ClassCoupling" Value="1" />
              <Metric Name="DepthOfInheritance" Value="1" />
              <Metric Name="LinesOfCode" Value="11" />
            </Metrics>
            <Types>
              <NamedType Name="Program">
                <Metrics>
                  <Metric Name="MaintainabilityIndex" Value="100" />
                  <Metric Name="CyclomaticComplexity" Value="1" />
                  <Metric Name="ClassCoupling" Value="1" />
                  <Metric Name="DepthOfInheritance" Value="1" />
                  <Metric Name="LinesOfCode" Value="7" />
                </Metrics>
                <Members>
                  <Method Name="void Program.Main(string[] args)" File="C:\source\repos\ConsoleApp20\ConsoleApp20\Program.cs" Line="7">
                    <Metrics>
                      <Metric Name="MaintainabilityIndex" Value="100" />
                      <Metric Name="CyclomaticComplexity" Value="1" />
                      <Metric Name="ClassCoupling" Value="1" />
                      <Metric Name="LinesOfCode" Value="4" />
                    </Metrics>
                  </Method>
                </Members>
              </NamedType>
            </Types>
          </Namespace>
        </Namespaces>
      </Assembly>
    </Target>
  </Targets>
</CodeMetricsReport>
```

### <a name="metricsexe"></a>Metrics.exe

NuGet paketini yüklemek istemiyorsanız, oluşturma kullanabilir ve *Metrics.exe* doğrudan çalıştırılabilir. Oluşturulacak *Metrics.exe* çalıştırılabilir:

1. Kopya [roslyn/dotnet-Çözümleyicileri](https://github.com/dotnet/roslyn-analyzers) depo.
2. Geliştirici komut istemi için Visual Studio'yu yönetici olarak açın.
3. Kök klasöründen **roslyn Çözümleyicileri** depo, aşağıdaki komutu yürütün: `Restore.cmd`
4. Dizini *src\Tools*.
5. Oluşturmak için aşağıdaki komutu yürütün **Metrics.csproj** proje:

   ```shell
   msbuild /m /v:m /p:Configuration=Release Metrics.csproj
   ```

   Adlı bir yürütülebilir dosya *Metrics.exe* içinde oluşturulan *artifacts\bin* depo kökü altındaki dizin.

#### <a name="metricsexe-usage"></a>Metrics.exe kullanımı

Çalıştırılacak *Metrics.exe*, kaynağı bir proje veya çözüm ve bir çıkış XML dosyası bağımsız değişken olarak. Örneğin:

```shell
C:\>Metrics.exe /project:ConsoleApp20.csproj /out:report.xml
Loading ConsoleApp20.csproj...
Computing code metrics for ConsoleApp20.csproj...
Writing output to 'report.xml'...
Completed Successfully.
```

#### <a name="legacy-mode"></a>Eski mod

Derleme seçtiğiniz *Metrics.exe* içinde *eski modu*. Aracın eski modu sürümünü gerekenler daha yakın olan ölçüm değerleri oluşturur [oluşturulan aracın eski sürümlerini](#previous-versions). Buna ek olarak, eski modda, *Metrics.exe* aracıyla oluşturulmuş kod ölçümleri için söz konusu önceki sürümlerini yöntemi aynı dizi türleri için kod ölçümleri oluşturur. Örneğin, kod ölçümleri verileri alan ve özellik başlatıcıları için oluşturmaz. Geriye dönük uyumluluk veya kodu iade kapılar varsa sayı kod ölçümlere göre eski modu kullanışlıdır. Derleme için komutu *Metrics.exe* eski modda:

```shell
msbuild /m /v:m /t:rebuild /p:LEGACY_CODE_METRICS_MODE=true Metrics.csproj
```

Daha fazla bilgi için [eski modda kod ölçümleri oluşturma etkinleştir](https://github.com/dotnet/roslyn-analyzers/pull/1841).

### <a name="previous-versions"></a>Önceki sürümler

Visual Studio 2015 dahil da bilinen bir komut satırı kod ölçümleri araç *Metrics.exe*. Bu Aracı'nın önceki sürümünü ikili bir analiz, diğer bir deyişle, derleme tabanlı analiz vermedi. Yeni *Metrics.exe* aracı kaynak kodu yerine analiz eder. Çünkü yeni *Metrics.exe* araçtır kaynak kod tabanlı komut satırı kod ölçümleri sonuçları bu Visual Studio IDE ve önceki sürümleri tarafından üretilen farklı *Metrics.exe*.

Çözüm ve proje yüklenebilir sürece yeni komut satırı kod ölçümleri aracı kaynak kod hataları varsa bile ölçümleri hesaplar.

#### <a name="metric-value-differences"></a>Ölçüm değeri farkları

`LinesOfCode` Ölçüm daha doğru ve güvenilir yeni komut satırı kod ölçümleri araç. Bu codegen farkları bağımsız ve çalışma zamanı ve araç takımı değiştiğinde değiştirmez. Yeni aracı boş satırlar ve yorumlarla birlikte kod, gerçek satırları sayar.

Gibi diğer ölçümler `CyclomaticComplexity` ve `MaintainabilityIndex` formüller önceki sürümlerini kullanan *Metrics.exe*, ancak yeni aracı sayısını sayar `IOperations` (mantıksal kaynak yönergeleri) yerine Ara Dil (IL) yönergeleri. Sayılar bu Visual Studio IDE ve önceki sürümleri tarafından oluşturulan biraz farklı olacaktır *Metrics.exe*.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod ölçümleri sonuçları penceresini kullanma](../code-quality/working-with-code-metrics-data.md)
- [Kod ölçüm değerleri](../code-quality/code-metrics-values.md)
