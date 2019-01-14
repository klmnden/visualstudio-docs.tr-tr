---
title: Kodunuzdaki başvuruları bulma
ms.date: 09/26/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- code editor, find all references
- find all references
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 143a40c1a2e3602460419465cb84d6ffa44d853c
ms.sourcegitcommit: 38db86369af19e174b0aba59ba1918a5c4fe4a61
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/14/2019
ms.locfileid: "54269858"
---
# <a name="find-references-in-your-code"></a>Kodunuzdaki başvuruları bulma

Kullanabileceğiniz **tüm başvuruları Bul** belirli kod öğelerinin tabanınızın Burada başvurulan bulmak için komutu. **Tüm başvuruları Bul** komut başvurularını bulmak istediğiniz öğe (sağ tıklama) bağlam menüsünde kullanılabilir. Veya, klavye kullanıcısıysanız basın **Shift + F12**.

Adlı bir araç penceresinde Sonuçların görüntülenme  **<element> başvuruları**burada *öğesi* aradığınız öğeyi adıdır. Araç çubuğunda **başvuruları** penceresi olanak sağlar:
- Aşağı açılan liste kutusunda arama kapsamını değiştirin. Yalnızca değiştirilen belgeler kadar tüm çözümün tamamını bakın seçebilirsiniz.
- Başvurulan öğeye seçerek kopyalama **kopyalama** düğmesi.
- Düğmeler, liste veya basın sonraki veya önceki konuma Git seçim **F8** ve **Shift + F8** Bunu yapmak için anahtarları.
- Seçim yaparak ve döndürülen sonuçlarda tüm filtreleri kaldırır **tüm filtreleri Temizle** düğmesi.
- Nasıl döndürülen öğeleri değiştirmek ayarı seçerek gruplandırılır **gruplandırma ölçütü:** aşağı açılan liste kutusu.
- Geçerli arama sonuçları penceresini seçerek korumak **sonuçları tut** düğmesi. Bu düğmeyi seçtiğinizde, bu pencerede geçerli arama sonuçları kalın ve yeni arama sonuçları yeni bir araç penceresi görüntülenir.
- Arama dizeleri arama sonuçları içindeki metin girerek **arama tüm başvuruları Bul** metin kutusu.

Ayrıca, fare başvurunun önizlemesini görmek için Arama sonuçlarından gelebilirsiniz.

![Tüm başvuruları Bul penceresi](../ide/media/vside_findallreferences.png)

## <a name="navigate-to-references"></a>Başvurular gidin
Başvuruları gitmek için aşağıdaki yöntemleri kullanabilirsiniz **başvuruları** penceresi:

- Tuşuna **F8** ileri başvuru için Git veya **Shift + F8** önceki başvuruya Git için.
- Tuşuna **Enter** anahtar üzerinde bir başvuru ya da ona kodda gitmek için çift tıklayın.
- Sağ tıklama menüsünde bir başvuru (bağlam menüsü), **önceki konuma** veya **sonraki konuma Git** komutları.
- Seçin **yukarı ok** ve **aşağı ok** anahtarları (içinde etkinleştirilip etkinleştirilmediğini **seçenekleri** iletişim kutusunda). Menü çubuğunda, bu özelliği etkinleştirmek için seçin **Araçları** > **seçenekleri** > **ortam**  >   **Sekmeler ve Windows** > **Önizleme sekmesinde**ve ardından **Önizleme sekmesinde açılmasını yeni dosyaların izin** ve **seçilen dosyalara Önizleme Sonuçları Bul** kutuları.

## <a name="change-reference-groupings"></a>Değişiklik başvuru grupları
Varsayılan olarak, başvuruları projeye göre ardından tanımına göre gruplandırılır. Ancak, ayarı değiştirerek bu gruplandırma sırasını değiştirebilirsiniz **gruplandırma ölçütü:** araç çubuğundaki açılan liste kutusunda. Örneğin varsayılan ayarı olan değiştirebilirsiniz **proje sonra tanım** için **tanım sonra proje**, diğer ayarlar için de.

**Tanımı** ve **proje** iki varsayılan gruplandırmaları kullanılır, ancak diğerleri seçerek ekleyebilirsiniz **gruplandırma** seçili öğenin sağ tıklayın veya bağlam menüsünde komutu. Daha fazla gruplandırmaları ekleme dosyaları ve yolları birçok çözümünüz varsa yararlı olabilir.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod gezinme](../ide/navigating-code.md)