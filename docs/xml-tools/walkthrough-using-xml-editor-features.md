---
title: 'İzlenecek yol: XML Düzenleyicisi özelliklerini kullanma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ea8dc357-2e66-455a-aec2-7ccaccfc9adf
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5e443cf23b8726161a4252e6cef3b77f5d3c37bb
ms.sourcegitcommit: 3cc73e74921a9ceb622542e0e263abeebc455c00
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/08/2019
ms.locfileid: "67624188"
---
# <a name="walkthrough-use-xml-editor-features"></a>İzlenecek yol: XML düzenleyicisi özelliklerini kullanma

Bu kılavuzda açıklanan adımları yeni bir XML belgesi oluşturma işlemini göstermektedir. İzlenecek yol bazı XML yazmak için değerli hale getiren XML Düzenleyicisi özelliklerini kullanır.

> [!NOTE]
> Yönergelere başlamadan önce kaydetmek *hireDate.xsd* dosyayı yerel bilgisayarınıza (aşağıda bu konuya da dahil).

## <a name="to-create-a-new-xml-file-and-associate-it-with-an-xml-schema"></a>Yeni bir XML dosyası oluşturun ve bir XML şeması ile ilişkilendirmek için

1. Üzerinde **dosya** menüsünde **yeni**, tıklatıp **dosya**.

2. Seçin **XML dosyası** içinde **şablonları** bölmesi ve tıklatın **açık**.

     Yeni bir dosya düzenleyicide açılır. Varsayılan XML bildirimi dosyasını içeren `<?xml version="1.0" encoding="utf-8">`.

3. Belge Özellikler penceresinde, Gözat düğmesine tıklayın ( **...** ) üzerinde **şemaları** alan.

     **XSD şemaları** iletişim kutusu görüntülenir.

4. **Ekle**'yi tıklatın.

     **Açık XSD şeması** iletişim kutusu görüntülenir.

5. Seçin *hireDate.xsd* tıklayın ve dosya **açık**.

6. **Tamam**'ı tıklatın.

     XML Şeması sunulmuştur XML belge ile ilişkilendirilmiş. XML Şeması, belgeyi doğrulamak için kullanılır. Bu ayrıca, IntelliSense tarafından geçerli öğe üye listesini doldurmak için kullanılır.

## <a name="to-add-data"></a>Veri eklemek için

1. Tür `<` Düzenleyicisi bölmesinde.

     Üye listesi, mümkün olan öğeleri görüntüler:

    - **!--** açıklama eklemek için.

    - **! DOCTYPE** belge türü eklemek için.

    - **?** bir işlem yönergesi eklemek için.

    - **çalışan** kök öğe eklemek için.

2. Seçin  **&lt;!--** bir açıklama düğümü ve ENTER tuşuna **Enter**.

     Düzenleyici, açıklama bitiş etiketi ekler ve başlangıç ve bitiş açıklama etiketleri arasında imleci geçir yerleştirir.

3. Yazın **Test XML dosyası**.

4. Yeni bir satıra yazın `<`seçip **çalışan** üye listesinde.

     Düzenleyicisi bir XML öğesi ekler `<employee`. Bu noktada öğenin öznitelikleri ekleyebilir veya yazarak başlangıç etiketi kapatabilirsiniz `>`.

5. Tür `>` etiketi kapatın.

6. Düzenleyici bitiş etiketi ekler. Bitiş etiketi, bir doğrulama hatası gösteren dalgalı alt çizgi ile eklenir. **Araç ipucu** iletisini görüntüler: **' % S'öğesi 'çalışanı' içeriği eksik sahip. 'ID' beklenen**.

7. Tür `<` seçip **kimliği** üye listesinde. Yazarak `>`.

     Düzenleyici XML öğesi ekler `<ID></ID>`ve imleci kimliği başlattığınızda etiketi yerleştirir.

8. Tür **abc**.

     **Abc** metin dalgalı çizgi vardır. **Araç ipucu** iletisini görüntüler: **'ID' öğesi kendi veri türüne göre geçersiz bir değere sahip**.

9. Kimliği öğeye sağ tıklayıp **tanıma**.

     Düzenleyicisi açılır *hireDate.xsd* yeni bir belge penceresi dosyasında ve imleci kimliği şema öğesi tanımını konumlandırır.

10. XML dosyasına dönün ve Değiştir **abc** metinle **123**.

     Dalgalı çizgi ve **araç ipucu** altında ID öğesinin değerine temizlenir. **Araç ipucu** çalışan sonu etiketi artık iletisini görüntüler: **' % S'öğesi 'çalışanı' içeriği eksik sahip. Beklenen 'alım tarihi'** .

11. Yazın, sonra kimliği bitiş etiketi imleci `<`seçin **alım tarihi** üye listesini ve ardından türünde `>`.

     Düzenleyici XML öğesi ekler `<hire-date></hire-date>`ve imleci başlangıç alım tarihi sonra etiketi yerleştirir.

12. Yazın **2003-01-10** alım tarih değeri.

## <a name="to-format-the-xml-document"></a>XML belgesi biçimlendirmek için

- Seçin **belgeyi Biçimlendir** basın veya XML Düzenleyicisi araç çubuğu düğmesini **Ctrl**+**E**,**D**.

   ![Visual Studio'da biçimi XML belge düğmesi](media/format-xml-document.png)

   XML belgesi biçimlendirilir.

## <a name="to-save-the-xml-document"></a>XML belgesi kaydetmek için

1. Gelen **dosya** menüsünde **Kaydet**.

     **Dosyayı farklı Kaydet** iletişim kutusu görüntülenir. Varsayılan dosya adı *'XMLFile1'* .

2. XML belgesi için konum ve dosya adını girin ve tıklayın **Kaydet**.

## <a name="hiredatexsd-file"></a>hireDate.xsd dosyası

Bu izlenecek yolda aşağıdaki şema dosyası kullanılır:

```xml
<?xml version="1.0"?>
<xs:schema attributeFormDefault="unqualified"
     elementFormDefault="qualified" targetNamespace="urn:empl-hire"
     xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="employee">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ID" type="xs:unsignedShort" />
        <xs:element name="hire-date" type="xs:date" />
      </xs:sequence>
    </xs:complexType>
  </xs:element>
</xs:schema>
```

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi](../xml-tools/xml-editor.md)