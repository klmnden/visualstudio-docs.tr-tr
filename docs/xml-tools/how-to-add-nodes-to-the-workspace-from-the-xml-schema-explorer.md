---
title: 'Nasıl yapılır: XML Şema Gezgininden Çalışma Alanına Düğüm Ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 3b5a5749-9693-4b29-b0c2-8e07e0e55514
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 578a50d8fae4047b6e36338f8067561c9e4e9636
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55935907"
---
# <a name="how-to-add-nodes-to-the-workspace-from-the-xml-schema-explorer"></a>Nasıl yapılır: XML şema gezgininden çalışma alanına düğüm ekleme

Bu konuda nasıl düğüm ekleneceği açıklanmaktadır [XML şema Tasarımcısı çalışma alanı](../xml-tools/xml-schema-designer-workspace.md) gelen **XML Şeması Gezgini**. Bu düğümlerden sürükleyip bırakarak gerçekleştirilebilir **XML Şeması Gezgini** kullanarak veya bir XSD Tasarımcısı görünümü üzerine **XML şema Explorer'ın** bağlam menüsü. Tarafından gerçekleştirilen bir arama sonucunda vurgulanmıştır düğümlerini de ekleyebilirsiniz **XML Şeması Gezgini**. Daha fazla bilgi için [nasıl yapılır: Şema kümesi arama sonucu düğümlerini çalışma alanına ekleme](../xml-tools/how-to-add-schema-set-search-result-nodes-to-the-workspace.md).

> [!NOTE]
> Yalnızca genel düğümler eklenebilir [XML şema Tasarımcısı çalışma alanı](../xml-tools/xml-schema-designer-workspace.md).

## <a name="to-add-nodes-through-the-xml-explorer-context-menu"></a>XML Gezgini bağlam menüsü aracılığıyla düğümler eklemek için

1.  Bağlantısındaki [nasıl yapılır: Bir XSD şema dosyası oluşturma ve düzenleme](../xml-tools/how-to-create-and-edit-an-xsd-schema-file.md).

2.  Sağ tıklayın `PurchaseOrderType` XSD Gezgininde. Seçin **graf görünümünde göster**.

     `purchaseOrderType` Düğümü graf görünümünü tasarım yüzeyinde görünür.

## <a name="to-drag-and-drop-a-node-on-to-a-view"></a>Sürükle ve bırak bir düğüm bir görünüm açmak için

1.  Sağ `PurchaseOrderType` graf görünümünü düğümü. Seçin **XML Şeması Gezgini gösterme**.

     Düğüm vurgulanan **XML Şeması Gezgini**.

2.  Sağ tıklayın `PurchaseOrderType` düğümünde **XML Şeması Gezgini** seçip **tüm başvuruları göster**.

     `purchaseOrder` Düğümü vurgulanır.

3.  Sürükleme `purchaseOrder` düğüm graf görünümünü açın.

     `purchaseOrder` Düğüm ve `PurchaseOrderType` düğüm birbirinin yanına graf görünümünü tasarım yüzeyinde görünür. İki düğüm birbiriyle ilişkili olduğundan ( `purchaseOrder` öğesi olduğu `PurchaseOrderType` türü), bir ok, aralarında çizilir.

## <a name="to-add-nodes-using-the-schema-explorer-search-capability"></a>Şema Gezgini arama özelliğini kullanarak düğümleri eklemek için

1.  "PurchaseOrder" yazın arama metin kutusuna [XML Gezgini](../xml-tools/xml-schema-explorer.md) araç çubuğu ve Ara düğmesine tıklayın.

     ![XML şema Gezgini anahtar sözcük arama](../xml-tools/media/schemaexplorersearch.gif)

     İçindeki arama sonuçlarında vurgulanır **XML Şeması Gezgini** ve dikey kaydırma çubuğu üzerinde işaretleri olarak işaretlendi.

2.  Arama sonuçlarını tıklayarak çalışma alanına ekleme **çalışma alanına vurgulanmış düğümler Ekle** özet sonuçlar bölmesinde düğmesine.

     ![XML şema Gezgini arama sonucu](../xml-tools/media/schemaexplorersearchresult.gif)

     `purchaseOrder` Düğüm ve `PurchaseOrderType` düğümünün görünen birbirinin yanına tasarım yüzeyine [graf görünümünü](../xml-tools/graph-view.md). İki düğüm birbiriyle ilişkili olduğundan ( `purchaseOrder` öğesi olduğu `PurchaseOrderType` türü), bir ok, aralarında çizilir.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Şema Gezgini](../xml-tools/xml-schema-explorer.md)