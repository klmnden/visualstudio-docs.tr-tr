---
title: Mimarinizi çözümleme ve mimarinizin modelini oluşturma
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- diagrams - modeling
- architecture
- code visualization
- application design
- code exploration
- modeling
- application architecture
- architecture [Visual Studio ALM], modeling
- application modeling
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: be731ea81baaaa6e9f04b7546bc26ccea0549389
ms.sourcegitcommit: 6a19c5ece38a70731496a38f2ef20676ff18f8a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65476624"
---
# <a name="analyze-and-model-your-architecture"></a>Mimarinizi çözümleme ve mimarinizin modelini oluşturma

Uygulamanızı kullanarak Visual Studio mimari ve Modelleme Araçları tasarlayıp uygulamanıza model mimari gereksinimleri karşıladığından emin olun.

* Var olan program kodu daha kolay kodun yapısını, davranış ve ilişkileri görselleştirmek için Visual Studio kullanarak anlayın.

* Mimari bağımlılıkları saygı göstermek için gerekli takımınızın eğitin.

* Farklı geliştirme sürecinizin bir parçası olarak uygulama yaşam döngüsü boyunca ayrıntı düzeylerinde modeller oluşturun.

Bkz: [senaryosu: Görselleştirme ve modelleme kullanarak tasarımınızı değiştirme](../modeling/scenario-change-your-design-using-visualization-and-modeling.md).

## <a name="article-reference"></a>Makale başvurusu

|||
|-|-|
|**Kodu görselleştirme**:<br /><br />-Kod haritaları oluşturarak kodun organizasyon ve ilişkileri bakın. Derlemeler, ad alanları, sınıflar, yöntemler vb. arasındaki bağımlılıkları görselleştirin.<br />-Koddan sınıf diyagramları oluşturarak belirli bir projenin üyeleri ve sınıf yapısı bakın.<br />-Kodu doğrulamak için bağımlılık diyagramları oluşturarak, kodunuzun tasarımı arasındaki çakışmaları bulun.|- [Kodu görselleştirme](../modeling/visualize-code.md)<br />- [Sınıflarla ve diğer türlerle (Sınıf Tasarımcısı) ile çalışma](../ide/class-designer/designing-and-viewing-classes-and-types.md)<br />- [Video: Visual Studio 2015 kod haritaları ile koddan tasarımı anlama](https://channel9.msdn.com/Events/Visual-Studio/Connect-event-2015/502)<br />- [Video: Gerçek zamanlı mimari bağımlılıklarınızı doğrula](https://sec.ch9.ms/sessions/69613110-c334-4f25-bb36-08e5a93456b5/170ValidateArchitectureDependenciesWithVisualStudio.mp4)|
|**Mimariyi tanımlayın**:<br /><br />-Tanımlamak ve bağımlılık diyagramları oluşturarak kodunuzun bileşenler arasındaki bağımlılıklar kısıtlamaları zorunlu kılma.|- [Video: Mimari bağımlılıkları (kanal 9) Visual Studio ile doğrula](https://channel9.msdn.com/Events/Connect/2016/170)|
|**Sisteminiz gereksinimleri ile doğrulamak ve hedeflenen tasarım:**<br /><br />-Hedeflenen mimarisini bağımlılık diyagramları ile kod bağımlılıklarını doğrulamak ve tasarım ile çakışabilecek değişiklikleri engelleyebilirsiniz.|- [Video: Mimari bağımlılıkları (kanal 9) Visual Studio ile doğrula](https://channel9.msdn.com/Events/Connect/2016/170)|
|**Modellerini ve diyagramlarını özelleştirme**:<br /><br />-Kendi etki alanına özgü diller oluşturun.|- [Visual Studio - etki alanına özgü diller için modelleme SDK'sı](../modeling/modeling-sdk-for-visual-studio-domain-specific-languages.md)|
|**T4 şablonlarını kullanarak metin oluşturmak**:<br /><br />-Metin tabanlı dosyaları oluşturmak için metin blokları ve şablonları içinde denetim mantığının kullanın.<br /> -Visual Studio'da bulunan MSBuild ile T4 şablonu derleme|- [Kod oluşturma ve T4 metin şablonları](../modeling/code-generation-and-t4-text-templates.md)|
|**Paylaşım modelleri ve diyagramları Team Foundation sürüm denetimini kullanarak kod haritaları**:<br /><br />-Kod Haritaları, projeler ve bağımlılık diyagramları Team Foundation sürüm denetimi altına yerleştirin ve böylelikle bunları paylaşabilirsiniz.| |

Visual Studio'nun hangi sürümlerinin her özelliğini desteklemek için bkz [mimari ve Modelleme Araçları sürüm desteği](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport)

## <a name="types-of-models-and-typical-uses"></a>Modelleri ve tipik türleri

### <a name="code-maps"></a>Kod haritaları

Kodunuzda organizasyon ve ilişkileri görmenize yardımcı kod eşlemeleri.

**Tipik kullanımları:**

- Program kodu İnceleme yapısı ve bağımlılıklarını daha iyi anlamak için nasıl güncelleştirmek ve maliyetini tahmin etmek önerilen değişiklikleri.

**Bkz:**

- [Çözümlerinizdeki bağımlılıkları eşleme](../modeling/map-dependencies-across-your-solutions.md)
- [Uygulamalarınızda hata ayıklamak için kod haritalarını kullanma](../modeling/use-code-maps-to-debug-your-applications.md)
- [Kod haritası çözümleyicilerini kullanarak olası sorunları bulma](../modeling/find-potential-problems-using-code-map-analyzers.md)

### <a name="dependency-diagrams"></a>Bağımlılık diyagramları

Bağımlılık diyagramları Katmanlar veya açık bağımlılıkları olan bloklar kümesi olarak uygulamanın yapısını tanımlamanıza olanak sağlar. Canlı doğrulama kodda bağımlılıklar ve bağımlılıkları bağımlılık diyagramda açıklanan arasındaki çakışmaları gösterir.

**Tipik kullanımları:**

- Uygulama çok sayıda değişiklikleriyle yapısını, kullanım ömrü boyunca Sabitle.
- Kod değişiklikleri iade etmeden önce istenmeyen bağımlılık çakışmaları keşfedin.

**Bkz:**

- [Kodunuz aracılığıyla bağımlılık diyagramları oluşturma](../modeling/create-layer-diagrams-from-your-code.md)
- [Bağımlılık diyagramları: Başvuru](../modeling/layer-diagrams-reference.md)
- [Bağımlılık diyagramları ile kod doğrulama](../modeling/validate-code-with-layer-diagrams.md)

### <a name="domain-specific-language-dsl"></a>Etki alanına özgü dil (DSL)

Bir DSL belirli bir amaç için tasarım bir gösterimidir. Visual Studio'da, genellikle grafik.

**Tipik kullanımları:**

- Oluşturma veya uygulamanın parçaları yapılandırın. İş, araçları ve gösterimi geliştirmek için gereklidir. Sonuç, etki alanınıza daha iyi bir UML özelleştirme daha uygun olabilir.
- Büyük projeler veya burada DSL ve araçlarını geliştirmeye yatırım tarafından döndürülen birden fazla proje kullanımını ürün serileri.

**Bkz:**

- [Visual Studio için Modelleme SDK'sı - Etki Alanına Özgü Diller](../modeling/modeling-sdk-for-visual-studio-domain-specific-languages.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Modelleme Visual Studio 2017'deki yenilikler](../modeling/what-s-new-for-design-in-visual-studio.md)
- [DevOps ve uygulama yaşam döngüsü yönetimi](/azure/devops/user-guide/devops-alm-overview)
