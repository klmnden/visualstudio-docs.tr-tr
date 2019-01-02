---
title: XML Şema Gezgini
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 2fc39e98-b194-456b-a452-cfafb0a52d66
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: eb49560074b3a4c43efe13ea568207b52536e562
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53918985"
---
# <a name="xml-schema-explorer"></a>XML Şema Gezgini

**XML Şeması Gezgini** XML Şeması Tanım Dili (XSD) şemalarla çalışma sağlamak için Microsoft Visual Studio ile XML Düzenleyicisi ile tümleşiktir. Bir XML şeması dosyasını açtığınızda **şeması Ayarla** düğüm görünür **XML Şeması Gezgini**. İle başvurulan dosyaları yanı sıra, hedef dosya için tüm dahil, içeri aktarılan veya yeniden tanımlanan şemalar bir `include` veya `import` deyimi de görünür **XML Şeması Gezgini**.

 **XML Şeması Gezgini** aşağıdakileri sağlar:

-   Şema kümesi hızlı bir bakış edinin.

-   Gözat ve ağaç gidin.

-   Anahtar sözcüğü ve şema özgü aramaları gerçekleştirin. Daha fazla bilgi için [şema kümesini arama](../xml-tools/searching-the-schema-set.md).

-   Arama sonuçlarını grafik görünümü veya içerik modeli görünümü ekleme

-   Belge sırada, tür veya ad ağaç sıralayın. Daha fazla bilgi için [sıralama, filtreleme ve gruplandırma](../xml-tools/sorting-filtering-and-grouping-xml-schema-explorer.md).

-   XML Düzenleyicisi'ni açın ve XSD dosyası kod konumlarda atlayın. Daha fazla bilgi için [Tümleştirmesi ile XML Düzenleyicisi](../xml-tools/integration-with-xml-editor.md).

-   Genel öğeler için XML örneği oluşturur.

**XML Şeması Gezgini** bir ağaç görünümü ayarlamak şema Cerberus bir görünümünü sağlar. **XML Şeması Gezgini** arama, filtreleme, gezinti ve sıralama de sağlar. Erişim için **XML Şeması Gezgini**, aşağıdakilerden birini yapın:

-   Kullanıyorsanız [başlangıç görünümündeki](../xml-tools/start-view.md), tıklayın **XML Şeması Gezgini** bağlantı.

-   Kullanıyorsanız [graf görünümünü](../xml-tools/graph-view.md) veya [içerik modeli görünümünü](../xml-tools/content-model-view.md) ve çalışma alanınızda düğümünüz, seçmek için bağlam menüsünü kullanın **XML Şeması Gezgini**.

-   Belirleyebilirsiniz **XML Şeması Gezgini** gelen **görünümü** menüsü.

-   Erişebildiğiniz **XML Şeması Gezgini** gelen bir *.vb* ile ilişkili bir Visual Basic XML değişmez değeri olan dosyası bir *.xsd* dosya. Şema görmek için kümesinde **XML Şeması Gezgini**, bir XML değişmez değeri ya da bir XML ad alanı alma bir XML düğümünü sağ tıklatın ve seçin **şema Gezgini'nde Göster** komutu. Daha fazla bilgi için [XML Şeması Gezgini ile tümleştirme, XML değişmez değerleri](../xml-tools/integration-of-xml-literals-with-xml-schema-explorer.md).

## <a name="tree-view"></a>Ağaç görünümü
 **XML Şeması Gezgini** görüntüler önceden derlenmiş şema ağaç yapısında bilgilerini ayarlayabilir. Ağaç yapısı şu şekilde düzenlenmiştir:

-   En üst düzeyinde şema düğüm ayarlanır.

-   İkinci düzey ad alanlarını içerir.

-   Üçüncü düzeyini dosyaları içerir.

-   Dördüncü düzey genel düğümleri içerir. Bu içerebilir öğeler, grupları, karmaşık türler, basit türler, öznitelikleri, öznitelik grupları ve `include`, `import`, ve `redefine` deyimleri.

Bir ağaç yapısı örneği verilmiştir:

![XML Şema Gezgini](../xml-tools/media/xmlschemaexplorer.gif)

## <a name="selection-and-activation"></a>Seçim ve etkinleştirme
 Vurgulayın ve bir düğümü seçmek için şema Gezgini içinde bir kez tıklayın.

 Bir düğüm etkinleştirmek için çift tıklayın veya basın **Enter** düğümü seçildiğinde.

-   Bir düğüm etkinleştirme bu düğümde tanımlanan (dosya zaten açık değilse) dosya açılır ve dosyayı düğümü seçer.

-   Bir dosya düğümü etkinleştirme (zaten açık değilse), seçili dosyayı açar ve vurgular `<schema>` düğümü.

-   Bir SchemaSet veya bir ad alanı düğümü etkinleştirme hiçbir şey yapmaz.

## <a name="drag-and-drop-nodes"></a>Sürükle ve bırak düğümleri
 Sürükleyin ve genel düğümler, dosya düğümleri ve ad alanı düğümleri bir XSD Tasarımcısı görünümü üzerine bırakın. Geçerli Görünüm ise [başlangıç görünümündeki](../xml-tools/start-view.md), bir düğüm görünümü açın sürükleyerek açılır [graf görünümünü](../xml-tools/graph-view.md). Geçerli Görünüm ise [içerik modeli görünümünü](../xml-tools/content-model-view.md) veya grafik görünümü, görünümün üzerine bir düğüm düşürdüğünüzde değiştirmez.

 Dosyalar görünümünde bırakarak eklenir genel tüm düğümleri dosyasındaki [XSD Tasarımcısı çalışma alanı](../xml-tools/xml-schema-designer-workspace.md). Ad alanları görünümünden bırakmayı genel tüm düğümleri çalışma alanına ad alanında ekleyeceksiniz. Çalışma alanı, tüm görünümleri arasında paylaşılır.

 Sürükleyin ve yerel düğümleri veya içeri aktarmalar bırakın olamaz.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: XML şema gezgininden çalışma alanına düğüm ekleme](../xml-tools/how-to-add-nodes-to-the-workspace-from-the-xml-schema-explorer.md)