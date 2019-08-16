---
title: Çözümleyici kuralı önem derecesi ve gizleme
ms.date: 03/26/2019
ms.topic: conceptual
helpviewer_keywords:
- code analysis, managed code
- analyzers
- Roslyn analyzers
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 6362d3f14065aaf9661e85266753642e4201ca48
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69548043"
---
# <a name="use-code-analyzers"></a>Kod Çözümleyicileri kullanma

.NET Compiler Platform ("Roslyn") kod Çözümleyicileri, siz yazarken C# veya Visual Basic kodunuzu analiz eder. Her bir *Tanılama* veya kuralın, projeniz için üzerine yazılabilir bir varsayılan önem derecesi ve gizleme durumu vardır. Bu makalede kural önem derecesini ayarlama, kural kümelerini kullanma ve ihlalleri gizleme ele alınmaktadır.

## <a name="analyzers-in-solution-explorer"></a>Çözüm Gezgini çözümleyiciler

**Çözüm Gezgini**'den çözümleyici tanılamayı özelleştirmenin çoğunu yapabilirsiniz. Çözümleyiciler bir NuGet paketi olarak [yüklüyorsanız](../code-quality/install-roslyn-analyzers.md) , **Çözüm Gezgini**içindeki **Başvurular** veya **Bağımlılıklar** düğümü altında bir **çözümleyiciler** düğümü görüntülenir. **Çözümleyicileri**genişlettikten sonra çözümleyici derlemelerinden birini genişletirseniz, derlemede tüm tanılamayı görürsünüz.

![Çözüm Gezgini içinde düğüm Çözümleyicileri](media/analyzers-expanded-in-solution-explorer.png)

**Özellikler** penceresinde, açıklaması ve varsayılan önem derecesi dahil olmak üzere bir tanı özelliklerini görüntüleyebilirsiniz. Özellikleri görüntülemek için kurala sağ tıklayın ve **Özellikler**' i seçin veya kuralı seçin ve ardından **alt**+**ENTER**tuşuna basın.

![Özellikler penceresi tanılama özellikleri](media/analyzer-diagnostic-properties.png)

Bir Tanılamanın çevrimiçi belgelerini görmek için, tanılamayı sağ tıklatın ve **Yardımı görüntüle**' yi seçin.

**Çözüm Gezgini** içindeki her bir Tanılamanın yanındaki simgeler, düzenleyicide açtığınızda kural kümesinde gördüğünüz simgelere karşılık gelir:

- bir daire içindeki "i", **bilgi** [önem derecesini](#rule-severity) gösterir
- Bir üçgendeki "!", **uyarının** [önem derecesini](#rule-severity) gösterir
- bir daire içindeki "x", **hatanın** [önem derecesini](#rule-severity) gösterir
- açık renkli bir arka plandaki daire içindeki "i", **gizlenen** [önem derecesini](#rule-severity) gösterir
- bir daire içindeki aşağı açılan ok, Tanılamanın bastırılmadığını belirtir

![Çözüm Gezgini tanılama simgeleri](media/diagnostics-icons-solution-explorer.png)

## <a name="rule-sets"></a>Kural kümeleri

[Kural kümesi](../code-quality/using-rule-sets-to-group-code-analysis-rules.md) , bireysel Tanılama için önem derecesini ve gizleme durumunu DEPOLAYAN bir XML dosyasıdır.

> [!NOTE]
> Kural kümeleri, hem eski analizler hem de kod çözümleyicilerinin kurallarını içerebilir.

Kural kümesi düzenleyicisinde etkin kural kümesini düzenlemek için, **Çözüm Gezgini** içindeki **başvuru** > **Çözümleyicileri** düğümüne sağ tıklayın ve **etkin kural kümesini aç**' ı seçin. Kural kümesini ilk kez düzenliyorsanız, Visual Studio varsayılan kural kümesi dosyasının bir kopyasını oluşturur, onu  *\<ProjectName >. RuleSet*olarak adlandırır ve projenize ekler. Bu özel kural kümesi, projeniz için etkin kural kümesi de olur.

Bir projenin etkin kural kümesini değiştirmek için projenin özelliklerinin **Kod Analizi** sekmesine gidin. **Bu kural kümesini Çalıştır**' ın altındaki listeden kural kümesini seçin. Kural kümesini açmak için **Aç**' ı seçin.

> [!NOTE]
> .NET Core ve .NET Standard projeleri, **Çözüm Gezgini**kural kümeleri için menü komutlarını desteklemez, örneğin, **etkin kural kümesi açın**. .NET Core veya .NET Standard projesi için varsayılan olmayan bir kural kümesi belirtmek için, [ **CodeAnalysisRuleSet** özelliğini](using-rule-sets-to-group-code-analysis-rules.md#specify-a-rule-set-for-a-project) proje dosyasına el ile ekleyin. Kuralları, Visual Studio kural kümesi Düzenleyicisi Kullanıcı arabirimindeki kural kümesi içinde yine yapılandırabilirsiniz.

## <a name="rule-severity"></a>Kural önem derecesi

Çözümleyiciler bir NuGet paketi olarak [yüklüyorsanız](../code-quality/install-roslyn-analyzers.md) , çözümleyici kurallarının önem derecesini veya *tanılamayı*yapılandırabilirsiniz. Aşağıdaki tabloda, Tanılama için önem derecesi seçenekleri gösterilmektedir:

|Önem Derecesi|Derleme zamanı davranışı|Düzenleyici davranışı|
|-|-|-|
|Hata|İhlaller **hata listesi** ve komut satırı derleme çıkışında *hata* olarak görünür ve yapıların başarısız olmasına neden olur.|Sorunlu kodun kırmızı renkli bir dalgalı çizili ve kaydırma çubuğundaki küçük kırmızı bir kutu tarafından işaretlenmiş olması gerekir.|
|Uyarı|İhlaller **hata listesi** ve komut satırı derleme çıkışında *Uyarı* olarak görünür, ancak derlemelerin başarısız olmasına neden olmaz.|Sorunlu kodun yeşil dalgalı çizili ile altı çizilir ve kaydırma çubuğunda küçük yeşil bir kutu ile işaretlenir.|
|Bilgi|İhlaller, komut satırı derleme çıktısında değil, **hata listesi** *iletiler* olarak görünür.|Sorunlu kodun gri dalgalı olarak altı çizilir ve kaydırma çubuğundaki küçük bir gri kutusuyla işaretlenir.|
|Hidden|Kullanıcıya görünür değil.|Kullanıcıya görünür değil. Ancak tanılama, IDE tanılama altyapısına bildirilir.|
|Yok.|Tamamen gizlendi.|Tamamen gizlendi.|

Ayrıca, **varsayılan**olarak ayarlayarak kuralın önem derecesini "sıfırlayabilirsiniz". Her tanı için, **Özellikler** penceresinde görünebileceğini varsayılan bir önem derecesi vardır.

Aşağıdaki ekran görüntüsünde, üç farklı önem taşıyan kod düzenleyicisinde üç farklı tanı ihlali gösterilmektedir. Sağ taraftaki kaydırma çubuğundaki küçük kutunun yanı sıra dalgalı renge dikkat edin.

![Kod düzenleyicisinde hata, uyarı ve bilgi ihlali](media/diagnostics-severity-colors.png)

Aşağıdaki ekran görüntüsünde **hata listesi**göründükleri üç ihlal gösterilmektedir:

![Hata Listesi hata, uyarı ve bilgi ihlali](media/diagnostics-severities-in-error-list.png)

Bir kuralın **Çözüm Gezgini**önem derecesini veya **Çözüm Gezgini**bir kuralın önem derecesini değiştirdikten sonra çözüme eklenen  *\<ProjectName >. RuleSet* dosyası dahilinde değiştirebilirsiniz.

![Çözüm Gezgini kural kümesi dosyası](media/ruleset-in-solution-explorer.png)

### <a name="set-rule-severity-from-solution-explorer"></a>Kural önem derecesini Çözüm Gezgini ayarla

1. **Çözüm Gezgini**, **başvuru** > **Çözümleyicileri** ' ni genişletin (.NET Core projeleri için**Bağımlılıklar** > **Çözümleyicileri** ).

1. Önem derecesini ayarlamak istediğiniz kuralı içeren derlemeyi genişletin.

1. Kurala sağ tıklayın ve **kural kümesi önem derecesi ayarla**' yı seçin. Giriş menüsünde, önem derecesi seçeneklerinden birini seçin.

   Kuralın önem derecesi, etkin kural kümesi dosyasına kaydedilir.

### <a name="set-rule-severity-in-the-rule-set-file"></a>Kural önem derecesini kural kümesi dosyasında ayarla

1. [Kural kümesi](analyzer-rule-sets.md) dosyasını **Çözüm Gezgini**açın, **çözümleyiciler** düğümünün sağ tıklama menüsünde **etkin kural kümesini aç** ' ı seçin ya da için **Kod Analizi** Özellik sayfasında **Aç** ' ı seçin. Proje.

1. İçeren derlemeyi genişleterek kurala gidin.

1. **Eylem** sütununda, bir açılan listeyi açmak için değeri seçin ve listeden istenen önem derecesini seçin.

   ![Düzenleyicide kural kümesi dosyası aç](media/ruleset-file-in-editor.png)

## <a name="suppress-violations"></a>İhlalleri gösterme

Kural ihlallerini bastırmak için birden çok yol vardır:

- **Çözümle** menüsünden

  Geçerli ihlallerin tümünü bastırmak için,**Kod analizini Çalıştır ve menü çubuğunda etkin sorunları Gizle** ' yi seçin. >  Bu bazen "taban çizgisi" olarak adlandırılır.

- **Çözüm Gezgini** 'den

  **Çözüm Gezgini**ihlalin bir ihlaline karşı gizlemek için kuralın önem derecesini **none**olarak ayarlayın.

- **Kural kümesi düzenleyicisinden**

  Kural kümesi düzenleyicisinden bir ihlalin görünmemesi için, adının yanındaki kutunun işaretini kaldırın veya **eylemi** **none**olarak ayarlayın.

- **Kod düzenleyicisinden**

  Kod düzenleyicisinden bir ihlalin görüntülenmesini engellemek için, imleci kod satırına ihlale yerleştirin ve **CTRL**+tuşuna basın **.** **hızlı eylemler** menüsünü açmak için. **Kaynak/gizleme dosyasında** **caxxxx** > 'i Gizle ' yi seçin.

  ![Hızlı Eylemler menüsünden tanılamayı gösterme](media/suppress-diagnostic-from-editor.png)

- **Hata listesi**

  Görüntülenmesini istediklerinizi seçerek **hata listesi** bir veya daha fazla tanılamayı bastırın ve sonra sağ tıklayıp**kaynak/gizleme dosyasında** **Gizle** > ' yi seçebilirsiniz.

  - **Kaynakta**bastırdığınızda, **Değişiklikleri Önizle** iletişim kutusu açılır ve kaynak koda eklenen C# [#pragma uyarının](/dotnet/csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning) veya Visual Basic [#Disable uyarı](/dotnet/visual-basic/language-reference/directives/directives) yönergesinin önizlemesini gösterir.

    ![Kod dosyasında #pragma uyarı ekleme önizlemesi](media/pragma-warning-preview.png)

  - **Gizleme dosyasını**seçerseniz, **Değişiklikleri Önizle** iletişim kutusu açılır ve genel gizlemeleri dosyasına eklenen <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> özniteliğin önizlemesini gösterir.

    ![Gizleme dosyasına SuppressMessage özniteliği ekleme önizlemesi](media/preview-changes-in-suppression-file.png)

  **Değişiklikleri Önizle** Iletişim kutusunda **Uygula**' yı seçin.

  > [!NOTE]
  > **Çözüm Gezgini**' de **gizleme** menüsü seçeneğini görmüyorsanız, ihlalin büyük olasılıkla canlı Analize değil derlemeden geliyor. **Hata listesi** , hem canlı kod analizinden hem de derlemeden tanılama veya kural ihlalleri görüntüler. Derleme tanılaması eski olduğundan, örneğin, ihlalin giderilmesi için kodu düzenlediyseniz, ancak yeniden oluşturmadıysanız, **hata listesi**bu tanılamayı gizlenemez. Canlı Analize veya IntelliSense 'e yönelik Tanılamalar, geçerli kaynaklarla her zaman güncel değildir ve **hata listesi**gizlenmiş olabilir. *Oluşturma* tanılamayı seçiminizden dışlamak için, **hata listesi** kaynak filtresini **derleme + IntelliSense** 'den **yalnızca IntelliSense**'e geçirin. Daha sonra, gizlemek istediğiniz tanılamayı seçin ve daha önce açıklandığı gibi devam edin.
  >
  > ![Visual Studio 'da Hata Listesi kaynak filtresi](media/error-list-filter.png)

## <a name="command-line-usage"></a>Komut satırı kullanımı

Projenizi komut satırında oluşturduğunuzda, aşağıdaki koşullar karşılanıyorsa, yapı çıkışında kural ihlalleri görüntülenir:

- Çözümleyiciler VSıX uzantısı olarak değil, bir NuGet paketi olarak yüklenir.

- Projenin kodunda bir veya daha fazla kural ihlal edildi.

- Bir ihlal kuralının [önem derecesi](#rule-severity) , **Uyarı**olarak ayarlanır; Bu durumda ihlallerin başarısız olmasına neden olmaz veya **hata**, bu durum ihlallerinin başarısız olmasına neden olur.

Yapı çıkışının ayrıntı düzeyi, kural ihlallerinin gösterilip gösterilmeyeceğini etkilemez. **Sessiz** ayrıntı düzeyine sahip olsa bile, yapı çıkışında kural ihlalleri görüntülenir.

> [!TIP]
> Bir komut satırından, *FxCopCmd. exe* Ile veya **RunCodeAnalysis** bayrağıyla MSBuild aracılığıyla eski analizler çalıştırmaya alışkın değilseniz, bu işlemi kod Çözümleyicileri ile nasıl yapacağıdır.

MSBuild kullanarak projenizi oluştururken komut satırında çözümleyici ihlallerini görmek için şöyle bir komut çalıştırın:

```cmd
msbuild myproject.csproj /target:rebuild /verbosity:minimal
```

Aşağıdaki görüntüde, bir çözümleyici kuralı ihlali içeren bir proje derlemeden komut satırı derleme çıkışı gösterilmektedir:

![Kural ihlali ile MSBuild çıkışı](media/command-line-build-analyzers.png)

## <a name="dependent-projects"></a>Bağımlı projeler

Bir .NET Core projesinde, NuGet Çözümleyicileri olan bir projeye başvuru eklerseniz, bu çözümleyiciler otomatik olarak bağımlı projeye de eklenir. Bu davranışı devre dışı bırakmak için örneğin, bağımlı proje bir birim testi projem ise, **Privatevarlıkların** özniteliğini ayarlayarak, başvurulan projenin *. csproj* veya *. vbproj* dosyasında NuGet paketini özel olarak işaretleyin:

```xml
<PackageReference Include="Microsoft.CodeAnalysis.FxCopAnalyzers" Version="2.9.0" PrivateAssets="all" />
```

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio 'da kod Çözümleyicileri 'ne genel bakış](../code-quality/roslyn-analyzers-overview.md)
- [Kod Çözümleyicisi hatası gönderme](https://github.com/dotnet/roslyn-analyzers/issues)
- [Kural kümelerini kullanma](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)
- [Kod Analizi uyarılarını gösterme](../code-quality/in-source-suppression-overview.md)
