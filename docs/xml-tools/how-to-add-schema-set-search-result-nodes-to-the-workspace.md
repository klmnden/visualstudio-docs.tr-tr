---
title: XML şema kümesi arama sonucu düğümlerini çalışma alanına ekleme
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ff33b3cc-4db9-4b4e-9378-b45ed5999b18
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5ba709e90de580aacda2034eca319a419583dac0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62783696"
---
# <a name="how-to-add-schema-set-search-result-nodes-to-the-workspace"></a>Nasıl yapılır: Şema kümesi arama sonucu düğümlerini çalışma alanına ekleme

Bu konu içinde vurgulanmıştır düğümlerini ekleme işlemi açıklanmaktadır **XML Şeması Gezgini** çalışma alanındaki anahtar sözcük arama sonucu olarak.

> [!NOTE]
> Yalnızca genel düğümler eklenebilir [çalışma](../xml-tools/xml-schema-designer-workspace.md).

 Bu örnekte örnek [satın alma siparişi şeması](../xml-tools/sample-xsd-file-purchase-order-schema.md).

## <a name="to-add-schema-set-result-nodes"></a>Şema kümesi sonucu düğümlerini eklemek için

1. Bağlantısındaki [nasıl yapılır: Bir XSD şema dosyası oluşturma ve düzenleme](../xml-tools/how-to-create-and-edit-an-xsd-schema-file.md).

2. "PurchaseOrder" yazın arama metin kutusuna [XML Gezgini](../xml-tools/xml-schema-explorer.md) araç çubuğu ve Ara düğmesine tıklayın.

     ![XML şema Gezgini anahtar sözcük arama](../xml-tools/media/schemaexplorersearch.gif)

     İçindeki arama sonuçlarında vurgulanır **XML Şeması Gezgini** ve dikey kaydırma çubuğu üzerinde işaretleri olarak işaretlendi.

3. Arama sonuçlarını tıklayarak çalışma alanına ekleme **çalışma alanına vurgulanmış düğümler Ekle** özet sonuçlar bölmesinde düğmesine.

     ![XML şema Gezgini arama sonucu](../xml-tools/media/schemaexplorersearchresult.gif)

     `purchaseOrder` Düğüm ve `PurchaseOrderType` düğümünün görünen birbirinin yanına tasarım yüzeyine [graf görünümünü](../xml-tools/graph-view.md). İki düğüm birbiriyle ilişkili olduğundan ( `purchaseOrder` öğesi olduğu `PurchaseOrderType` türü), bir ok, aralarında çizilir.