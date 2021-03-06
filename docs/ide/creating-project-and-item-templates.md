---
title: Projeleri ve dosyaları için şablonlar
ms.date: 01/02/2018
ms.topic: conceptual
helpviewer_keywords:
- templates [Visual Studio], project
- templates [Visual Studio], item
- item templates [Visual Studio]
- project templates [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 83ac401b67444d4fdd467d5aefeb46bccb5e7e84
ms.sourcegitcommit: cd21b38eefdea2cdefb53e68e7a30b868e78dd6b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2019
ms.locfileid: "66037005"
---
# <a name="project-and-item-templates"></a>Proje ve öğe şablonları

Proje ve öğe şablonları, bazı temel kod ve kendi amaçları için özelleştirebilecekleri yapısı, kullanıcılara vermek yeniden kullanılabilir saptamalar sağlar.

## <a name="visual-studio-templates"></a>Visual Studio şablonları

Bir dizi önceden tanımlanmış proje ve öğe şablonları, Visual Studio ile yüklenir. Bu şablonlar gibi **ASP.NET Web uygulaması** ve **sınıf kitaplığı** yeni bir proje oluştururken seçmek şablonlar kullanılabilir. Öğe şablonları, kod dosyaları, XML dosyaları, HTML sayfaları ve stil sayfalarını gibi görünür **Yeni Öğe Ekle** penceresi.

Bu şablonlar, proje oluşturmaya başlamak için veya mevcut projeleri genişletmek için kullanıcılar için bir başlangıç noktası sağlar. Proje şablonları, belirli proje türü için gerekli dosyaları sağlar, standart derleme başvurularını içerir ve varsayılan proje özellikleri ve derleyici seçeneklerini ayarlayın. Öğe şablonları, birden çok kaynak kodu dosyaları saplama kodla, Tasarımcı bilgi dosyaları ve gömülü kaynaklar belirli dosya uzantısına sahip tek bir boş dosya karmaşıklığı değişebilir.

Yüklü Şablonlar kullanmak, kendi özel şablonlarınızı yazar veya indirin ve topluluk tarafından oluşturulan şablonlarını kullanın. Daha fazla bilgi için [nasıl yapılır: Proje şablonları oluşturma](../ide/how-to-create-project-templates.md) ve [nasıl yapılır: Öğe şablonları oluşturma](../ide/how-to-create-item-templates.md).

## <a name="contents-of-a-template"></a>Bir şablon içeriği

Tüm proje ve öğe şablonları, Visual Studio ile yüklenir veya sizin tarafınızdan oluşturulan aynı ilkeleri kullanarak işlev ve benzer içeriğe sahip. Tüm şablonları aşağıdaki öğeleri içerir:

- Şablonu kullanıldığında oluşturulan dosyalar. Bu dosyalar, kaynak kodu dosyaları, katıştırılmış kaynaklar, proje dosyaları vb. içerir.

::: moniker range="vs-2017"

- A *.vstemplate* şablondan bir proje veya öğe oluşturmak için ve şablonda görüntülemek için gerekli meta veriler içeren dosya **yeni proje** ve **Add New Item** Windows.

::: moniker-end

::: moniker range=">=vs-2019"

- A *.vstemplate* şablondan bir proje veya öğe oluşturmak ve şablonu görüntülemek için gerekli meta veriler içeren dosya **yeni bir proje oluşturma** sayfası veya **Add New Item** iletişim kutusu.

::: moniker-end

   Hakkında daha fazla bilgi için *.vstemplate* dosyaları görmek [şablon etiketleri](template-tags.md) ve [şablon parametreleri](../ide/template-parameters.md).

Ne zaman bu dosyaları sıkıştırılır içine bir *.zip* dosya ve doğru klasöre yerleştirin, Visual Studio otomatik olarak aşağıdaki konumlarda görüntüler:

::: moniker range="vs-2017"

- Proje şablonları görünür **yeni proje** penceresi.

::: moniker-end

::: moniker range=">=vs-2019"

- Proje şablonları görünmez **yeni bir proje oluşturma** sayfası.

::: moniker-end

- Öğe şablonları görünür **Yeni Öğe Ekle** penceresi.

Şablon klasörleri hakkında daha fazla bilgi için bkz. [nasıl yapılır: Şablonları bulma ve düzenleme](../ide/how-to-locate-and-organize-project-and-item-templates.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Proje şablonları oluşturma](../ide/how-to-create-project-templates.md)
- [Nasıl yapılır: Öğe şablonları oluşturma](../ide/how-to-create-item-templates.md)
- [Şablon etiketleri](template-tags.md)
- [Şablon parametreleri](../ide/template-parameters.md)
- [Şablonları özelleştirme](../ide/customizing-project-and-item-templates.md)
- [Visual Studio şablonları NuGet paketleri](/nuget/visual-studio-extensibility/visual-studio-templates)