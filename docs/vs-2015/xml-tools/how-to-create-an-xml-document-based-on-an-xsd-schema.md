---
title: 'Nasıl yapılır: Bir XSD şemasını temel alan XML belgesi oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: 193b195f-e918-4c79-a1a1-8096a1433bde
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 70b42db031c200f16a9189c4d750c9011e739029
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59647579"
---
# <a name="how-to-create-an-xml-document-based-on-an-xsd-schema"></a>Nasıl yapılır: Bir XSD Şemasını Temel Alan XML Belgesi Oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**Örnek XML oluşturmak** özelliği XML Şeması (XSD) dosyanız tabanlı bir örnek XML dosyası oluşturur.  
  
 Aşağıdaki senaryolar için bu seçeneği kullanabilirsiniz:  
  
- Çeşitli yapılar, şema kullanımını anlamak için.  
  
- Şema ne yaptığını onaylamak için bunu gerçekleştirmesi amaçlanmıştır.  
  
  **Örnek XML oluşturmak** özelliği yalnızca genel öğeler üzerinde kullanılabilir ve geçerli bir XML şema kümesi gerektirir.  
  
  Bu özellik, genellikle geçerli XML belgeleri oluşturur. Şema, bir veya daha fazlasını içeriyor, ancak örnek geçerli olmayabilir:  
  
- `xs:key`, `xs:keyref`, Ve `xs:unique` kimlik kısıtlamaları.  
  
- `xs:pattern` modeller.  
  
- Numaralandırmalar `xs:QName` türü.  
  
- `xs:ENTITY`, `xs:ENTITIES`, ve `xs:NOTATION` türleri.  
  
  Ayrıca, `xs:base64Binary` içeriği yalnızca numaralandırma türü için şema oluşursa oluşturulur.  
  
### <a name="to-generate-an-xml-instance-document-based-on-the-xsd-file"></a>XSD dosyasını temel alan bir XML örneği belge oluşturmak için  
  
1.  Bağlantısındaki [nasıl yapılır: Bir XSD şema dosyası oluşturma ve düzenleme](../xml-tools/how-to-create-and-edit-an-xsd-schema-file.md).  
  
2.  İçinde [XML Şeması Gezgini](../xml-tools/xml-schema-explorer.md), sağ `PurchaseOrder` genel öğesi. Seçin **örnek XML oluşturmak**.  
  
     Bu seçeneği belirlediğinizde, aşağıdaki örnek XML içeriği PurchaseOrder.xml dosyasıyla oluşturulur ve XML Düzenleyicisi'nde açılır:  
  
    ```  
    <?xml version="1.0" encoding="utf-8"?>  
    <PurchaseOrder OrderDate="1900-01-01" xmlns="http://tempuri.org/PurchaseOrderSchema.xsd">  
      <ShipTo country="US">  
        <name>name1</name>  
        <street>street1</street>  
        <city>city1</city>  
        <state>state1</state>  
        <zip>1</zip>  
      </ShipTo>  
      <ShipTo country="US">  
        <name>name2</name>  
        <street>street2</street>  
        <city>city2</city>  
        <state>state2</state>  
        <zip>-79228162514264337593543950335</zip>  
      </ShipTo>  
      <BillTo country="US">  
        <name>name1</name>  
        <street>street1</street>  
        <city>city1</city>  
        <state>state1</state>  
        <zip>1</zip>  
      </BillTo>  
    </PurchaseOrder>  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XML Verileriyle Çalışma](../xml-tools/working-with-xml-data.md)
