---
title: Visual Studio 2017’de tasarıma yönelik yenilikler
titleSuffix: ''
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- what's new [Visual Studio], architecture and modeling
- architecture [Visual Studio], modeling
- modeling software [Visual Studio], What's New
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
monikerRange: vs-2017
ms.openlocfilehash: dc75c7414e0fff18f76d14f8f9a4e0779a9e7a2b
ms.sourcegitcommit: 6a19c5ece38a70731496a38f2ef20676ff18f8a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65476544"
---
# <a name="whats-new-for-design-in-visual-studio-2017"></a>Visual Studio 2017’de tasarıma yönelik yenilikler

## <a name="live-dependency-validation"></a>Canlı bağımlılık doğrulama

İstenmeyen bağımlılık kaldırma, teknik borcun yönetimi, önemli bir parçasıdır. Visual Studio, nerede olurlarsa olsunlar gibi konular hakkında kesin bilgi dahil olmak üzere, bağımlılık Canlı doğrulama sağlar. Canlı bağımlılık doğrulama alır tam avantajları yeni özellikler ve Hata Listesi Düzenleyici.

![Eylem Canlı bağımlılık doğrulama](media/dep-validation-whatsnew-01.png)

Yazma deneyiminde, bağımlılık doğrulaması daha bulunabilir ve daha erişilebilir hale getirmek için değişti. Terminoloji "Katman diyagramından", "Bağımlılık diyagrama" değişti.

**Mimarisi** menüsü artık, doğrudan bir bağımlılık diyagramı oluşturmak için bir komut içerir:

![Canlı bağımlılık öğede mimari menüsü](media/dep-validation-whatsnew-02.png)

Katman özellik adları ve açıklamaları daha anlamlı olacak şekilde değiştirilmiştir:

![Canlı bağımlılık özelliği adları güncelleştirildi](media/dep-validation-whatsnew-03.png)

Geçerli çözümün kodunu analiz sonuçları yaptığınız değişikliklerin etkisini hemen diyagramda her kaydettiğinizde bakın. Tamamlanmasını beklemek zorunda değilsiniz **bağımlılıkları doğrulamak** komutu.

Daha fazla ayrıntı için [bu blog gönderisini](https://devblogs.microsoft.com/devops/live-architecture-dependency-validation-in-visual-studio-15-preview-5/).

## <a name="uml-designers-have-been-removed"></a>UML tasarımcılarına kaldırıldı

Visual Studio'da UML tasarımcılarına kaldırıldı.

* UML diyagramları artık XML dosyaları olarak sunulur
* UML Model Gezgini artık yok
* Modelleme projesi başvuruları artık bağımlılık doğrulaması için kullanılır
* Çözüm Gezgini "Katman başvuruları" düğümünde artık görüntülenmez
* Bağımlılık (katman) diyagram üzerinde "Doğrula" derleme eylemi artık kullanılmamaktadır - derleme görevi kaldırıldı
* Proje yapısını sürümleri arasında gidiş dönüşü korunur
* Yine de açın, oluşturabilir, düzenleyebilir ve bir bağımlılık (katman) diyagramı XML olarak kaydetme
* TFS iş öğeleri için bir bağımlılık (katman) diyagramı tasarım yüzeyinde erişilebilir değil
* Geri gelen DSL veya katmanına bağlama artık desteklenmiyor
* UML Genişletilebilirlik modelleme SDK'sı, artık desteklenmiyor

.NET mimarisini görselleştirmek için destek ve C++ kodu aracılığıyla kullanılabilir [kod haritaları](map-dependencies-across-your-solutions.md).

UML tasarımcılarına önemli bir kullanıcı varsa, UML ihtiyaçlarınız için alternatif bir aracı üzerinde karar sırada Visual Studio 2015 veya önceki sürümlerini kullanmaya devam edebilirsiniz.

Daha fazla ayrıntı için [bu blog gönderisini](https://devblogs.microsoft.com/devops/uml-designers-have-been-removed-layer-designer-now-supports-live-architectural-analysis/).

[!INCLUDE[modeling_sdk_info](includes/modeling_sdk_info.md)]

## <a name="a-nameversionsupport-edition-support-for-architecture-and-modeling-tools"></a><a name="VersionSupport" />Mimari ve Modelleme Araçları sürüm desteği

Visual Studio, birçok sürümlerinde kullanılabilir. Bunların tümü, mimari ve Modelleme Araçları için destek sağlar. Aşağıdaki tabloda her bir aracı kullanılabilirliğini gösterir.

|**Özelliği**|**Enterprise edition**|**Professional sürümü**|**Community sürümü**|
|-|-|-|-|
|**Kod haritaları**|Evet|Yalnızca okuma kod haritalarını destekler, kod filtreleme, yeni genel düğüm ekleme ve seçimden yeni yönlendirilmiş grafik oluşturma eşler.|-|
|**Bağımlılık diyagramları**|Evet|Yalnızca bağımlılık diyagramlarını okuma destekler.|Yalnızca bağımlılık diyagramlarını okuma destekler.|
|**Yönlendirilmiş grafikleri** (DGML diyagramları)|Evet|Evet|Evet|
|**Kod kopyası**|Evet|-|-|