---
title: Kodu görselleştirme
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- code, understanding
- code, visualizing
- code, exploring
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a5c034a34c5ae9b8bdaad5dbd14da2fb571c8dac
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62968099"
---
# <a name="visualize-code"></a>Kodu görselleştirme

Görselleştirme ve modelleme araçlarını Visual Studio'da, mevcut kodu anlamanıza ve uygulamanızı tanımlamanıza yardımcı olması için kullanabilirsiniz. Bu görsel olarak yaptığınız değişiklikler kod ve iş ve bu değişikliklerden kaynaklanan riskleri değerlendirme Yardım nasıl etkileyebilecek öğrenmenize olanak tanır. Örneğin:

- Kodunuzdaki ilişkileri anlamak için bu ilişkileri görsel olarak eşleyin.

- Sisteminizin mimarisini ve kod, tasarım ile tutarlı tutmak için bağımlılık diyagramları oluşturmak ve kodu bu diyagramları karşı doğrulayın.

- Sınıf yapılarını açıklamak için sınıf diyagramları oluşturun.

Bu araçlar, ayrıca daha kolay proje ile ilgili kişilerle iletişim kurmasına yardımcı olur.

Visual Studio'nun hangi sürümlerinin her özelliğini desteklemek için bkz [mimari ve Modelleme Araçları sürüm desteği](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport)

## <a name="what-do-you-want-to-do"></a>Ne yapmak istiyorsunuz?

|||
|-|-|
|**Kod ve ilişkilerini anlayın:**<br /><br /> Belirli kod parçaları arasındaki ilişkileri eşleyin.<br /><br /> Çözümün tamamını kodunuzdaki ilişkileri genel bir bakış görürsünüz.|- [Çözümlerinizdeki bağımlılıkları eşleme](../modeling/map-dependencies-across-your-solutions.md)<br />- [Uygulamalarınızda hata ayıklamak için kod haritalarını kullanma](../modeling/use-code-maps-to-debug-your-applications.md)<br />- [Kod Haritası çözümleyicilerini kullanarak olası sorunları bulma](../modeling/find-potential-problems-using-code-map-analyzers.md)<br />- [Hata ayıklarken çağrı yığınında yöntemler eşleştirme](../debugger/map-methods-on-the-call-stack-while-debugging-in-visual-studio.md)|
|**Sınıf yapıları anlayın:**<br /><br /> Koddan sınıf diyagramları oluşturarak bir projedeki sınıf yapısını görselleştirin.|[Nasıl yapılır: Projelere Sınıf Diyagramları Ekleme (Sınıf Tasarımcısı)](../ide/class-designer/how-to-add-class-diagrams-to-projects.md)|
|**Üst düzey sistem tasarımı tanımlamak ve bu tasarım karşı kodu doğrulayın:**<br /><br /> Bağımlılık diyagramları oluşturarak, üst düzey sistem tasarımı ve hedeflenen bağımlılıklarını açıklar. Kodu bir koddaki bağımlılıkları tasarım ile tutarlı kalmasını sağlamak için bu tasarım karşı doğrulayın.|- [Kodunuz aracılığıyla bağımlılık diyagramları oluşturma](../modeling/create-layer-diagrams-from-your-code.md)<br />- [Bağımlılık diyagramları: Başvuru](../modeling/layer-diagrams-reference.md)<br />- [Bağımlılık diyagramları: Yönergeler](../modeling/layer-diagrams-guidelines.md)<br />- [Bağımlılık diyagramları ile kod doğrulama](../modeling/validate-code-with-layer-diagrams.md)|

## <a name="see-also"></a>Ayrıca bkz.

- [Senaryo: Görselleştirme ve modelleme kullanarak tasarımınızı değiştirme](../modeling/scenario-change-your-design-using-visualization-and-modeling.md)
- [Analiz ve Model mimarisi](../modeling/analyze-and-model-your-architecture.md)
- [Uygulama mimarinizi modelleme](../modeling/model-your-app-s-architecture.md)
- [Geliştirme sürecinizde modelleri kullanma](../modeling/use-models-in-your-development-process.md)

[!INCLUDE[modeling_sdk_info](includes/modeling_sdk_info.md)]
