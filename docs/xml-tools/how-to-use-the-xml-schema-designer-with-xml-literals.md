---
title: 'Nasıl yapılır: XML Şema Tasarımcısını XML Değişmez Değerleri ile Kullanma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: d11803e7-f81a-41a2-a145-ba494a45cc93
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- VB
ms.workload:
- multiple
ms.openlocfilehash: 9e92cbdca3ac2c5c366ec054ba79f2e7324986c1
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60067618"
---
# <a name="how-to-use-the-xml-schema-designer-with-xml-literals"></a>Nasıl yapılır: XML Şema Tasarımcısını XML değişmez değerleri ile kullanma

Bu konuda, bir Visual Basic projesinde sabit değeri bir XML ile ilişkili bir şeması görüntülemeyi açıklar.

## <a name="create-a-new-visual-basic-project"></a>Yeni bir Visual Basic projesi oluşturma

1. Visual Studio'yu açın.

2. Yeni bir Visual Basic Oluştur **konsol uygulaması** adlı proje **XMLLiterals**.

     Yeni Proje bir Visual Basic kaynak dosyası içeren *Module1.vb*.

## <a name="add-an-existing-xsd-file"></a>Mevcut bir XSD dosyası ekleme

1. Yeni bir metin dosyasını Not Defteri'nde açın. XML şema örnek koddan kopyalama [satın alma siparişi şeması](../xml-tools/sample-xsd-file-simple-schema.md) dosyasına yapıştırın.

2. Dosya adı ile bir konuma kaydedin *PurchaseOrderSchema.xsd*.

3. İçinde **Çözüm Gezgini**, projenin adını sağ tıklayın, **Ekle**ve ardından **var olan öğe**. **AddExisting öğesi** iletişim kutusu görüntülenir. Gözat *PurchaseOrderSchema.xsd* dosya seçin ve ardından **Ekle**.

     XMLLiterals proje artık iki dosya içerir: *Module1.vb* ve *PurchaseOrderSchema.xsd*.

## <a name="add-code"></a>Kod ekleme

XML değişmez değer, Visual Basic kodunu eklemek için XSD dosyası projeye dahil temel:

1. Değiştirin *Module1.vb* dosyasındaki kodu aşağıdaki kodla:

   ```vb
   Imports <xmlns:ns="http://tempuri.org/PurchaseOrderSchema.xsd">

   Module Module1
      Sub Main()

          Dim XMLLiteral = <ns:PurchaseOrder OrderDate="1900-01-01">
                               <ns:ShipTo country="US">
                                   <ns:name>name1</ns:name>
                                   <ns:street>street1</ns:street>
                                   <ns:city>city1</ns:city>
                                   <ns:state>state1</ns:state>
                                   <ns:zip>1</ns:zip>
                               </ns:ShipTo>
                               <ns:BillTo country="US">
                                   <ns:name>name1</ns:name>
                                   <ns:street>street1</ns:street>
                                   <ns:city>city1</ns:city>
                                   <ns:state>state1</ns:state>
                                   <ns:zip>1</ns:zip>
                               </ns:BillTo>
                           </ns:PurchaseOrder>

      End Sub
   End Module
   ```

2. Herhangi bir XML değişmez değeri ya da bir XML ad alanı alma XML düğümünü sağ tıklatın ve seçin **şema Gezgini'nde Göster**.

   **XML Şeması Gezgini** XML şema kümesi ile ilişkili XML değişmez değeri olan bir Visual Basic dosyası ile yan yana görüntülenir.