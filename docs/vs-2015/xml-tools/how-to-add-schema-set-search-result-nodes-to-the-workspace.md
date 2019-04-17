---
title: 'Nasıl yapılır: Şema kümesi arama sonucu düğümlerini çalışma alanına ekleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: ff33b3cc-4db9-4b4e-9378-b45ed5999b18
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: a5df4b9c3bdefb6b807850e2b9f58fed8b2fd2a3
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59670114"
---
# <a name="how-to-add-schema-set-search-result-nodes-to-the-workspace"></a>Nasıl yapılır: Şema Kümesi Arama Sonucu Düğümlerini Çalışma Alanına Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu konuda, çalışma alanındaki anahtar sözcük arama sonucu olarak, XML şema Gezgini içinde vurgulanmıştır düğümlerini ekleme açıklanmaktadır.  
  
> [!NOTE]
>  Yalnızca genel düğümler eklenebilir [çalışma](../xml-tools/xml-schema-designer-workspace.md).  
  
 Bu örnekte örnek [satınalma siparişi şeması](../xml-tools/sample-xsd-file-purchase-order-schema.md).  
  
### <a name="to-add-schema-set-result-nodes"></a>Şema kümesi sonucu düğümlerini eklemek için  
  
1.  Bağlantısındaki [nasıl yapılır: Bir XSD şema dosyası oluşturma ve düzenleme](../xml-tools/how-to-create-and-edit-an-xsd-schema-file.md).  
  
2.  "PurchaseOrder" yazın arama metin kutusuna [XML Gezgini](../xml-tools/xml-schema-explorer.md) araç çubuğu ve Ara düğmesine tıklayın.  
  
     ![XML şema Gezgini anahtar sözcük arama](../xml-tools/media/schemaexplorersearch.gif "SchemaExplorerSearch")  
  
     Arama sonuçları XML şema Gezgini içinde vurgulanmış ve dikey kaydırma çubuğu üzerinde işaretleri tarafından işaretlenen.  
  
3.  Arama sonuçlarını tıklayarak çalışma alanına ekleme **çalışma alanına vurgulanmış düğümler Ekle** özet sonuçlar bölmesinde düğmesine.  
  
     ![XML şema Gezgini arama sonucu](../xml-tools/media/schemaexplorersearchresult.gif "SchemaExplorerSearchResult")  
  
     `purchaseOrder` Düğüm ve `PurchaseOrderType` düğümünün görünen birbirinin yanına tasarım yüzeyine [graf görünümünü](../xml-tools/graph-view.md). İki düğüm birbiriyle ilişkili olduğundan ( `purchaseOrder` öğesi olduğu `PurchaseOrderType` türü), bir ok, aralarında çizilir.
