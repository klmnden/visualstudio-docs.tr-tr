---
title: Dışarı aktarma ve kod haritaları kaydedin
ms.date: 05/16/2018
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 70c4cd238b6e5d31eced6a35ff0c7d24ab85a280
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63003119"
---
# <a name="share-code-maps"></a>Kod haritalarını paylaşma

Kod Haritaları, Visual Studio projesinin bir parçası olarak, görüntü veya XPS dosyası olarak kaydedebilirsiniz.

## <a name="share-a-code-map-with-other-visual-studio-users"></a>Bir kod Haritası diğer Visual Studio kullanıcılarıyla paylaşma

Kullanım **dosya** harita kaydetmek için menü.

-veya-

Haritanın harita araç çubuğunda belirli projenin bir parçası kaydetmek için seçin **paylaşımı** > **taşıma \<CodeMapName > içine .dgml**ve ardından, kaydetmek istediğiniz projeyi seçin eşleyin.

![Başka bir projeye bir harita Taşı](../modeling/media/codemapsmovemapmenu.png)

Visual Studio kaydeder Haritası olarak bir *.dgml* diğer Visual Studio Enterprise ve Visual Studio Professional kullanıcılarıyla paylaşmadan dosya.

> [!NOTE]
> Bir harita Visual Studio Professional kullanıcılarıyla paylaşmadan önce grupları genişlettiğinizden, gizli düğümleri göstermek ve çapraz grup bağlantılarını ve başkalarının haritanızda görmesini istediğiniz silinmiş düğümleri aldığınızdan emin olun. Aksi takdirde, diğer kullanıcıların bu öğeleri görmesi mümkün olmayacaktır.
>
> Bir modelleme projesinde olan ya da bir modelleme projesinden başka bir konuma kopyalanan bir harita kaydettiğinizde aşağıdaki hata oluşabilir:
>
> "Kaydedilemiyor *fileName* proje dizininin dışına. Bağlantılı öğeler desteklenmez."
>
> Visual Studio hatayı gösterir, ancak kaydedilen sürümü de oluşturur. Hatayı önlemek için harita modelleme projesinin dışında oluşturun. Ardından istediğiniz konuma kaydedebilirsiniz. Yalnızca çözümdeki başka bir konuma dosya kopyalama ve onu kaydetmeye çalışmak başarısızlıkla sonuçlanacaktır.

## <a name="export-a-code-map-as-an-image"></a>Bir kod Haritası bir görüntü olarak dışarı aktar

Bir kod Haritası bir görüntü olarak dışarı aktardığınızda, Microsoft Word veya PowerPoint gibi diğer uygulamalara kopyalayabilirsiniz.

1. Kod Haritası araç çubuğunda **paylaşımı** > **görüntü olarak e-posta** veya **görüntüsünü kopyalama**.

2. Görüntüyü başka bir uygulamaya yapıştırın.

## <a name="export-the-map-as-an-xps-file"></a>Harita XPS dosyası olarak dışarı aktarma

Bir kod Haritası XPS dosyası olarak dışarı aktardığınızda, Internet Explorer gibi XML veya XAML görüntüleyicilerde görebilirsiniz.

1. Kod Haritası araç çubuğunda **paylaşımı** > **taşınabilir XPS olarak e-posta** veya **taşınabilir XPS olarak Kaydet**.

2. Dosyayı kaydetmek istediğiniz yere göz atın.

3. Kod Haritası adı. Emin olun **farklı kaydetme türü** kutusu ayarlandığında **XPS dosyaları (\*.xps)**. **Kaydet**’i seçin.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod haritaları ile bağımlılıkları eşleştirme](../modeling/map-dependencies-across-your-solutions.md)