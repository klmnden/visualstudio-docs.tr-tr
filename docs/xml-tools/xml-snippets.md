---
title: XML kod parçacıkları
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 348dbf64-3f09-4fff-b47a-a7ecdf3221cc
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 66736431b295f974bda1ca855d88cd5f5f868e7d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62807732"
---
# <a name="xml-snippets"></a>XML kod parçacıkları

XML Düzenleyicisi adlı bir özellik sunar *XML kod parçacıklarını*, XML dosyalarını daha hızlı bir şekilde oluşturmanızı sağlar. XML kod parçacıklarını dosyalarınızı ekleyerek yeniden kullanabilirsiniz. XML verilerini bir XML Şeması Tanım Dili (XSD) şemaya göre de oluşturabilirsiniz.

## <a name="reusable-xml-snippets"></a>Yeniden kullanılabilir. XML kod parçacıkları

XML Düzenleyicisi'ni bazı genel görevleri kapsayan çok sayıda kod parçacıkları içerir. Bu XML dosyaları daha bir kolayca oluşturmanıza olanak sağlar. Örneğin, "Karmaşık türü dizisi öğe" ile "Basit türü öğe" kod parçacıkları kullanarak bir XML Şeması yazıyorsanız dosyanıza aşağıdaki XML metni ekler. Ardından değiştirirsiniz `name` gereksinimlerinize uyacak şekilde değeri.

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

Kod parçacıkları iki yolla ekleyebilirsiniz. **Parçacık Ekle** komut İmleç konumuna XML kod parçacığı ekler. **Surround With** komut XML kod parçacığı seçili metin etrafına sarmalar. Her iki komutu ya da gelen **IntelliSense** altında alt **Düzenle** menüsünden veya sağ tıklama menüsünde Düzenleyici içindeki.

Daha fazla bilgi için [nasıl yapılır: XML kod parçacıklarını kullanma](../xml-tools/how-to-use-xml-snippets.md).

## <a name="schema-generated-xml-snippets"></a>Şema tarafından oluşturulan XML kod parçacıkları

XML Düzenleyicisi'ni XML şemasından XML kod parçacığı oluşturma olanağı da vardır. Bu özellik, öğenin o öğe için şema bilgileri üretilen XML öğeleri ile doldurmak verir. Daha fazla bilgi için [nasıl yapılır: XML şemasından XML kod parçacığı oluşturma](../xml-tools/how-to-generate-an-xml-snippet-from-an-xml-schema.md).

## <a name="create-new-xml-snippets"></a>Yeni kod parçacıkları oluşturma

Visual Studio ile varsayılan olarak içerdiği parçacıkları yanı sıra oluşturabilir ve kendi XML kod parçacıklarını kullanma. Daha fazla bilgi için [nasıl yapılır: XML kod parçacıklarını oluşturma](../xml-tools/how-to-create-xml-snippets.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da kod parçacıkları](../ide/code-snippets.md)
- [XML Düzenleyicisi](../xml-tools/xml-editor.md)