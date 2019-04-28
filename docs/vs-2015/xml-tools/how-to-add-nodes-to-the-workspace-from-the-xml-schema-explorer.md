---
title: 'Nasıl yapılır: XML şema gezgininden çalışma alanına düğüm ekleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: 3b5a5749-9693-4b29-b0c2-8e07e0e55514
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 1fef367b36a683111369b656c8c1ba5a285fe6df
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63417453"
---
# <a name="how-to-add-nodes-to-the-workspace-from-the-xml-schema-explorer"></a>Nasıl yapılır: XML Şema Gezgininden Çalışma Alanına Düğüm Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu konuda nasıl düğüm ekleneceği açıklanmaktadır [XML şema Tasarımcısı çalışma alanı](../xml-tools/xml-schema-designer-workspace.md) XML şema gezgininden. Bu düğüm XSD Tasarımcısı görünümü üzerine XML şema gezgininden sürükleyip bırakarak veya XML şema Gezgini'nin bağlam menüsünü kullanarak gerçekleştirilebilir. XML şema Gezgini tarafından gerçekleştirilen bir arama sonucunda vurgulanmıştır düğümlerini de ekleyebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Şema kümesi arama sonucu düğümlerini çalışma alanına ekleme](../xml-tools/how-to-add-schema-set-search-result-nodes-to-the-workspace.md).  
  
> [!NOTE]
> Yalnızca genel düğümler eklenebilir [XML şema Tasarımcısı çalışma](../xml-tools/xml-schema-designer-workspace.md).  
  
### <a name="to-add-nodes-through-the-xml-explorer-context-menu"></a>XML Gezgini bağlam menüsü aracılığıyla düğümler eklemek için  
  
1. Bağlantısındaki [nasıl yapılır: Bir XSD şema dosyası oluşturma ve düzenleme](../xml-tools/how-to-create-and-edit-an-xsd-schema-file.md).  
  
2. Sağ tıklayın `PurchaseOrderType` düğümünde bir XSD Gezgini. Seçin **graf görünümünde göster**.  
  
     `purchaseOrderType` Düğümü graf görünümünü tasarım yüzeyinde görünür.  
  
### <a name="to-drag-and-drop-a-node-on-to-a-view"></a>Sürükle ve bırak bir düğüm bir görünüm açmak için  
  
1. Sağ tıklayın `PurchaseOrderType` graf görünümünü düğümü. Seçin **XML Şeması Gezgini gösterme**.  
  
     Düğümün içinde XML Şeması Gezgini vurgulanır.  
  
2. Sağ tıklayın `PurchaseOrderType` düğümünü seçin ve XML Şeması Gezgini **tüm başvuruları göster**.  
  
     `purchaseOrder` Düğümü vurgulanır.  
  
3. Sürükleme `purchaseOrder` düğüm graf görünümünü açın.  
  
     `purchaseOrder` Düğüm ve `PurchaseOrderType` düğüm birbirinin yanına graf görünümünü tasarım yüzeyinde görünür. İki düğüm kullanıcılarla ilgili olduğundan ( `purchaseOrder` öğesi olduğu `PurchaseOrderType` türü), bir ok, aralarında çizilir.  
  
### <a name="to-add-nodes-using-the-schema-explorer-search-capability"></a>Şema Gezgini arama özelliğini kullanarak düğümleri eklemek için  
  
1. "PurchaseOrder" yazın arama metin kutusuna [XML Gezgini](../xml-tools/xml-schema-explorer.md) araç çubuğu ve Ara düğmesine tıklayın.  
  
     ![XML şema Gezgini anahtar sözcük arama](../xml-tools/media/schemaexplorersearch.gif "SchemaExplorerSearch")  
  
     Arama sonuçları XML şema Gezgini içinde vurgulanmış ve dikey kaydırma çubuğu üzerinde işaretleri tarafından işaretlenen.  
  
2. Arama sonuçlarını tıklayarak çalışma alanına ekleme **çalışma alanına vurgulanmış düğümler Ekle** özet sonuçlar bölmesinde düğmesine.  
  
     ![XML şema Gezgini arama sonucu](../xml-tools/media/schemaexplorersearchresult.gif "SchemaExplorerSearchResult")  
  
     `purchaseOrder` Düğüm ve `PurchaseOrderType` düğümünün görünen birbirinin yanına tasarım yüzeyine [graf görünümünü](../xml-tools/graph-view.md). İki düğüm birbiriyle ilişkili olduğundan ( `purchaseOrder` öğesi olduğu `PurchaseOrderType` türü), bir ok, aralarında çizilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XML Şema Gezgini](../xml-tools/xml-schema-explorer.md)
