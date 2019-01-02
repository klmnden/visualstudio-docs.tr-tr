---
title: 'Nasıl Yapılır: Bir XSD Şemasını Temel Alan XML Belgesi Oluşturma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 193b195f-e918-4c79-a1a1-8096a1433bde
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d675695b3d3e054d14e481c8c41ae06de5af5600
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53820205"
---
# <a name="how-to-create-an-xml-document-based-on-an-xsd-schema"></a>Nasıl Yapılır: Bir XSD şemasını temel alan XML belgesi oluşturma

**Örnek XML oluşturmak** özelliği XML Şeması (XSD) dosyanız tabanlı bir örnek XML dosyası oluşturur.

 Aşağıdaki senaryolar için bu seçeneği kullanabilirsiniz:

-   Çeşitli yapılar, şema kullanımını anlamak için.

-   Şema ne yaptığını onaylamak için bunu gerçekleştirmesi amaçlanmıştır.

**Örnek XML oluşturmak** özelliği yalnızca genel öğeler üzerinde kullanılabilir ve geçerli bir XML şema kümesi gerektirir.

Bu özellik, genellikle geçerli XML belgeleri oluşturur. Şema, bir veya daha fazlasını içeriyor, ancak örnek geçerli olmayabilir:

-   `xs:key`, `xs:keyref`, Ve `xs:unique` kimlik kısıtlamaları.

-   `xs:pattern` modeller.

-   Numaralandırmalar `xs:QName` türü.

-   `xs:ENTITY`, `xs:ENTITIES`, ve `xs:NOTATION` türleri.

Ayrıca, `xs:base64Binary` içeriği yalnızca numaralandırma türü için şema oluşursa oluşturulur.

## <a name="to-generate-an-xml-instance-document-based-on-the-xsd-file"></a>XSD dosyasını temel alan bir XML örneği belge oluşturmak için

1.  Bağlantısındaki [nasıl yapılır: Bir XSD şema dosyası oluşturma ve düzenleme](../xml-tools/how-to-create-and-edit-an-xsd-schema-file.md).

2.  İçinde [XML Şeması Gezgini](../xml-tools/xml-schema-explorer.md), sağ `PurchaseOrder` genel öğesi. Seçin **örnek XML oluşturmak**.

     Bu seçenek, PurchaseOrder seçtiğinizde. *xml* aşağıdaki örnek XML içeriği dosyasıyla oluşturulur ve XML Düzenleyicisi'nde açılır:

    ```xml
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

## <a name="see-also"></a>Ayrıca bkz.

- [XML verileriyle çalışma](../xml-tools/working-with-xml-data.md)