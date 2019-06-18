---
title: Yönetilen kod için kod analizi
ms.date: 06/12/2019
ms.topic: conceptual
helpviewer_keywords:
- code analysis, managed code
- managed code, code analysis
author: mikadumont
ms.author: midumont
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 6c2202103bbff9de75921fba18f842f633419587
ms.sourcegitcommit: fd5a5b057df3d733f5224c305096907989811f85
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2019
ms.locfileid: "67196419"
---
# <a name="overview-of-code-analysis-for-managed-code-in-visual-studio"></a>Visual Studio'da yönetilen kod için kod çözümlemesine genel bakış

Visual Studio, yönetilen kod için Kod Analizi iki yolla gerçekleştirebilirsiniz: ile [ikili Çözümleyicileri](../code-quality/walkthrough-analyzing-managed-code-for-code-defects.md)FxCop statik analiz daha modern ve Yönetilen derlemeler olarak da bilinen [Roslyn Çözümleyicileri](../code-quality/roslyn-analyzers-overview.md). Bu konu, FxCop statik kod analizi içerir. Kaynak Çözümleyicileri kullanarak kodunu analiz etme hakkında daha fazla bilgi için bkz: [genel bakış, Roslyn Çözümleyicileri](../code-quality/roslyn-analyzers-overview.md).

Yönetilen kod için Kod Analizi yönetilen derlemeleri çözümler ve derlemeler hakkında bilgi gibi programlama ve tasarım kuralları ihlalleri konan raporları [.NET tasarım yönergeleri](/dotnet/standard/design-guidelines/).

Analiz aracı uyarı iletileri bir Çözümleme sırasında gerçekleştirdiği denetimleri temsil eder. Uyarı iletileri ilgili programlama ve tasarım sorunlarını belirleyin ve mümkünse sorunu gidermek nasıl bilgi olduğunda.

> [!NOTE]
> Statik kod analizi, Visual Studio'da .NET Core ve .NET Standard projeleri için desteklenmiyor. Kod Analizi bir .NET Core veya .NET Standard projesi msbuild bir parçası olarak çalıştırırsanız, benzer bir hata göreceğiniz **hata: CA0055 : İçin Platform tanımlanamadı \<your.dll >** . .NET Core veya .NET Standard projelerine kodda çözümlemek için kullanın [Roslyn Çözümleyicileri](../code-quality/roslyn-analyzers-overview.md) yerine.

## <a name="ide-integrated-development-environment-integration"></a>IDE (tümleşik geliştirme ortamı) Tümleştirmesi

El ile veya otomatik olarak projenizde kod analizi çalıştırabilirsiniz.

Bir projeyi derleme yaptığınızda Kod Analizi çalıştırmak için seçin **derlemede kod analizini etkinleştir** projenin özellik sayfasında. Daha fazla bilgi için [nasıl yapılır: Enable ve Disable otomatik kod çözümlemesini](../code-quality/how-to-enable-and-disable-automatic-code-analysis-for-managed-code.md).

Kod Analizi proje üzerinde el ile çalıştırmak için menü çubuğundan seçin **Çözümle** > **kod çözümlemeyi Çalıştır** > **kod çözümlemeyi Çalıştır \<proje >** .

## <a name="rule-sets"></a>Kural kümeleri

Yönetilen kod için Kod Analizi kuralları halinde gruplanır [kural kümeleri](../code-quality/using-rule-sets-to-group-code-analysis-rules.md). Microsoft Standart kural kümelerinden birini kullanabilir veya [bir özel kural kümesi oluşturma](../code-quality/how-to-create-a-custom-rule-set.md) belirli bir gereksinimi karşılamak için.

## <a name="suppress-warnings"></a>Uyarıları gizleme

Genellikle, geçerli olmayan bir uyarı olduğunu belirtmek kullanışlıdır. Bu geliştiriciye ve kodu daha sonra gözden geçirecek diğer kişilere bir uyarı araştırılması ve sonra da gizlenen veya yoksayıldı olduğunu bildirir.

Uyarıların kaynak sıkıştırması özel öznitelikler ile gerçekleştirilir. Bir uyarıyı bastırmak için öznitelik Ekle `SuppressMessage` aşağıdaki örnekte gösterildiği gibi kaynak koda:

```csharp
[System.Diagnostics.CodeAnalysis.SuppressMessage("Microsoft.Design", "CA1039:ListsAreStrongTyped")]
Public class MyClass
{
   // code
}
```

Daha fazla bilgi için [uyarıları bastırma](../code-quality/in-source-suppression-overview.md).

> [!NOTE]
> Bir projeyi Visual Studio 2017 veya Visual Studio 2019 geçirirseniz, birden çok sayıda kod çözümleme uyarıları karşılaştığı. Uyarıları gidermek ve hemen üretken olmak hazır değilseniz yapabilecekleriniz *temel* projenizin çözümleme durumu. Gelen **Çözümle** menüsünde **kod analizini Çalıştır ve etkin sorunlar bastır**.

## <a name="run-code-analysis-as-part-of-check-in-policy"></a>İade ilkesinin parçası olarak kod analizini Çalıştır

Bir kuruluş olarak tüm iade etmelerin bazı ilkeleri karşılamasını zorunlu isteyebilirsiniz. Özellikle, aşağıdaki ilkeleri uyguladığınızdan emin olmanız gerekir:

- Teslim edilen kodda derleme hataları vardır.

- Kod Analizi en son derlemenin bir parçası çalıştırılır.

Bu iade etme ilkeleri belirterek gerçekleştirebilirsiniz. Daha fazla bilgi için [projesi iade ilkeleriyle kod kalitesini geliştirme](../code-quality/how-to-create-or-update-standard-code-analysis-check-in-policies.md).

## <a name="team-build-integration"></a>Ekip Oluşturma entegrasyonu

Analiz aracı yapı işleminin bir parçası olarak çalıştırmak için derleme sisteminin tümleşik özelliklerini kullanabilirsiniz. Daha fazla bilgi için [Azure işlem hatları](/azure/devops/pipelines/index?view=vsts).

## <a name="see-also"></a>Ayrıca bkz.

- [Roslyn çözümleyicilerini genel bakış](../code-quality/roslyn-analyzers-overview.md)
- [Kod Analizi Kurallarını Gruplandırmak için Kural Kümeleri Kullanma](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)
- [Nasıl yapılır: Etkinleştirme ve otomatik kod analizini devre dışı](../code-quality/how-to-enable-and-disable-automatic-code-analysis-for-managed-code.md)
