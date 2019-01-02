---
title: XML Kod Parçacıkları
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 348dbf64-3f09-4fff-b47a-a7ecdf3221cc
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 5572e020dba08c7a417c8a7af40f8d20083198a5
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53928321"
---
# <a name="xml-snippets"></a>XML kod parçacıkları

XML Düzenleyicisi adlı bir özellik sunar *XML kod parçacıklarını*, XML dosyalarını daha hızlı bir şekilde oluşturmanızı sağlar. XML kod parçacıklarını dosyalarınızı ekleyerek yeniden kullanabilirsiniz. XML veri bir XML Şeması Tanım Dili (XSD) şemaya göre de oluşturabilirsiniz.

## <a name="reusable-xml-snippets"></a>Yeniden kullanılabilir. XML kod parçacıkları

XML Düzenleyicisi'ni bazı genel görevleri kapsayan çok sayıda kod parçacıkları içerir. Bu XML dosyaları daha bir kolayca oluşturmanıza olanak sağlar. Örneğin, "Karmaşık türü dizisi öğesi" ve "Basit türü öğesi" kod parçacıkları kullanarak bir XML Şeması yazıyorsanız dosyanıza aşağıdaki XML metni ekler. Ardından değiştirirsiniz `name` gereksinimlerinize uyacak şekilde değeri.

```xml
<xs:element name="name">
  <xs:complexType>
    <xs:sequence>
      <xs:element name="name">
        <xs:simpleType>
          <xs:restriction base="xs:string"></xs:restriction>
        </xs:simpleType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>
</xs:element>
```

 Kod parçacıkları iki yolla ekleyebilirsiniz. **Parçacık Ekle** komut İmleç konumuna XML kod parçacığı ekler. **Surround With** komut XML kod parçacığı seçili metin etrafına sarmalar. Her iki komutu ya da kullanılabilir gelen **IntelliSense** altında alt **Düzenle** menüsünden veya Düzenleyicisi kısayol menüsünden.

 Daha fazla bilgi için [nasıl yapılır: XML kod parçacıklarını kullanma](../xml-tools/how-to-use-xml-snippets.md).

## <a name="schema-generated-xml-snippets"></a>Şema tarafından oluşturulan XML kod parçacıkları
 XML Düzenleyicisi'ni XML şemasından XML kod parçacığı oluşturma olanağı da vardır. Bu özellik, öğenin o öğe için şema bilgileri üretilen XML öğeleri ile doldurmak verir.

 Daha fazla bilgi için [nasıl yapılır: XML şemasından XML kod parçacığı oluşturma](../xml-tools/how-to-generate-an-xml-snippet-from-an-xml-schema.md).

## <a name="create-new-xml-snippets"></a>Yeni kod parçacıkları oluşturma
 İçerdiği parçacıkları yanı sıra [!INCLUDE[msCoName](../xml-tools/includes/msconame_md.md)] Visual Studio varsayılan olarak da oluşturabilir ve kendi XML kod parçacıklarını kullanma.

 Daha fazla bilgi için [nasıl yapılır: XML kod parçacıklarını oluşturma](../xml-tools/how-to-create-xml-snippets.md).

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi](../xml-tools/xml-editor.md)