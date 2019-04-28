---
title: 'Nasıl yapılır: XML Şemasından XML Kod Parçacığı Oluşturma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 2c128d2a-aaa6-4814-aa95-e07056afe338
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b2c3aad870112b580078f2dbb849f9ee1a771ed0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63001914"
---
# <a name="how-to-generate-an-xml-snippet-from-an-xml-schema"></a>Nasıl yapılır: XML şemasından XML kod parçacığı oluşturma

XML Düzenleyicisi'ni XML Şeması Tanım Dili (XSD) şemasından XML kod parçacıklarını oluşturma özelliğine sahiptir. Örneğin, öğe adı yanındaki konumlandırılmış olsa bir XML dosyasına yazma gibi basabilirsiniz **sekmesini** öğenin o öğe için şema bilgileri üretilen XML verileri ile doldurmak için.

Bu özellik yalnızca öğeleri üzerinde kullanılabilir. Ayrıca, aşağıdaki kurallar geçerlidir:

- Öğesi, bir ilişkili şema türü olması gerekir; diğer bir deyişle, öğe ilişkili bazı şemaya göre geçerli olmalıdır. Şema türü soyut olamaz ve türü gerekli öznitelikler içermelidir ve/veya alt öğeleri gereklidir.

- Geçerli öğe düzenleyicide özniteliklere boş olmalıdır. Örneğin, tüm geçerli aşağıda verilmiştir

    - `<Account`

    - `<Account>`

    - `<Account></Account>`

- İmleç hemen öğe adı sağa bulunmalıdır.

Oluşturulan kod parçacığı, tüm gerekli öznitelikler ve öğeler içerir. Varsa `minOccurs` biri, gerekli en az o öğenin örnek sayısı en çok 100 örnek kod parçacığında dahil edilenlerden daha büyüktür. Herhangi bir sabit değerlerini sabit değerleri kod parçacığında şema sonucu bulunamadı. `xsd:any` ve `xsd:anyAttribute` öğeleri göz ardı edilir ve hiçbir ek kod parçacığı yapılardan neden.

Varsayılan değerleri oluşturulur ve düzenlenebilir değerleri Not. Şema varsayılan değeri belirtiyorsa, bu varsayılan değer kullanılır. Ancak, şema varsayılan değer boş bir dize ise, düzenleyici varsayılan değerleri aşağıdaki şekilde oluşturur:

- Şema türü herhangi bir sabit listesi modelleri, doğrudan veya dolaylı olarak herhangi bir birleşim tipinin üye yoluyla içeriyorsa şema nesne modeli içinde bulunan ilk numaralandırılmış değer varsayılan olarak kullanılır.

- Şema türü atomik bir tür ise, düzenleyici atomik türü alır ve atomik tür adını ekler. Türetilen bir basit türü için temel bir basit türü kullanır. Atomik türü için listeyi türdür `itemType`. Atomik türü bir birleşimin atomik ilk türüdür `memberType`.

## <a name="example"></a>Örnek

 Bu bölümdeki adımları XML Düzenleyicisi şema tarafından oluşturulan XML kod parçacığı özelliğini nasıl kullanacağınızı gösterir.

> [!NOTE]
> Bu yordamlar başlatmadan önce şema dosyasını yerel bilgisayarınıza kaydedin.

### <a name="to-create-a-new-xml-file-and-associate-it-with-an-xml-schema"></a>Yeni bir XML dosyası oluşturun ve bir XML şeması ile ilişkilendirmek için

1. Üzerinde **dosya** menüsünde **yeni**, tıklatıp **dosya**.

2. Seçin **XML dosyası** içinde **şablonları** bölmesi ve tıklatın **açık**.

     Yeni bir dosya düzenleyicide açılır. Varsayılan XML bildirimi dosyasını içeren `<?xml version="1.0" encoding="utf-8">`.

3. Belge Özellikler penceresinde, Gözat düğmesine tıklayın (**...** ) üzerinde **şemaları** alan.

     **XSD şemaları** iletişim kutusu görüntülenir.

4. **Ekle**'yi tıklatın.

     **Açık XSD şeması** iletişim kutusu görüntülenir.

5. Şema dosyası seçin ve tıklayın **açık**.

6. **Tamam**'ı tıklatın.

     XML Şeması sunulmuştur XML belge ile ilişkilendirilmiş.

### <a name="to-generate-an-xml-snippet"></a>XML kod parçacığı oluşturmak için

1. Tür `<` Düzenleyicisi bölmesinde.

2. Üye listesi, mümkün olan öğeleri görüntüler:

     **!--** açıklama eklemek için.

     **! DOCTYPE** belge türü eklemek için.

     **?** bir işlem yönergesi eklemek için.

     **İlgili kişi** kök öğe eklemek için.

3. Seçin **kişi** tuşuna basın ve üye listesi **Enter**.

     Düzenleyici başlangıç etiketi ekler `<Contact` ve imleci öğe adından sonra konumlandırır.

4. Tuşuna **sekmesini** XML verileri oluşturmak için `Contact` öğesi üzerinde şema bilgilerini temel.

## <a name="input"></a>Giriş

 Aşağıdaki şema dosyası izlenecek yol tarafından kullanılır.

```xml
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema elementFormDefault="qualified"
           xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:simpleType name="phoneType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Voice"/>
      <xs:enumeration value="Fax"/>
      <xs:enumeration value="Pager"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:element name="Contact">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="Name">
          <xs:simpleType>
            <xs:restriction base="xs:string"></xs:restriction>
          </xs:simpleType>
        </xs:element>
        <xs:element name="Title"
                    type="xs:string" />
        <xs:element name="Phone"
                    minOccurs="1"
                    maxOccurs="unbounded">
          <xs:complexType>
            <xs:sequence>
              <xs:element name="Number"
                          minOccurs="1">
                <xs:simpleType>
                  <xs:restriction base="xs:string"></xs:restriction>
                </xs:simpleType>
              </xs:element>
              <xs:element name="Type"
                          default="Voice"
                          minOccurs="1"
                          type="phoneType"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
    </xs:complexType>
  </xs:element>
</xs:schema>
```

### <a name="output"></a>Çıkış

 İle ilişkili şema bilgilere dayanarak oluşturulan XML verileri aşağıdadır `Contact` öğesi. İşaretli öğeleri olarak `bold` düzenlenebilir XML kod parçacığı alanlarını belirleyin.

```xml
<Contact>
  <Name>name</Name>
  <Title>title</Title>
  <Phone>
    <Number>number</Number>
    <Type>Voice</Type>
  </Phone>
</Contact>
```

## <a name="see-also"></a>Ayrıca bkz.

- [XML kod parçacıkları](../xml-tools/xml-snippets.md)
- [Nasıl yapılır: XML kod parçacıklarını kullanma](../xml-tools/how-to-use-xml-snippets.md)