---
title: 'İzlenecek yol: XML Düzenleyicisi özelliklerini kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: ea8dc357-2e66-455a-aec2-7ccaccfc9adf
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 27e9d1ce86064c23e3a293382ff7f83389d693f1
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60109071"
---
# <a name="walkthrough-using-xml-editor-features"></a>İzlenecek yol: XML Düzenleyicisi özelliklerini kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu kılavuzda açıklanan adımları yeni bir XML belgesi oluşturma işlemini göstermektedir. İzlenecek yol bazı XML yazmak için değerli hale getiren XML Düzenleyicisi'nin özelliklerini kullanır.  
  
> [!NOTE]
>  Yönergelere başlamadan önce (aşağıda bu konuya da dahil) hireDate.xsd dosyayı yerel bilgisayarınıza kaydedin.  
  
### <a name="to-create-a-new-xml-file-and-associate-it-with-an-xml-schema"></a>Yeni bir XML dosyası oluşturun ve bir XML şeması ile ilişkilendirmek için  
  
1. Üzerinde **dosya** menüsünde **yeni**, tıklatıp **dosya**.  
  
2. Seçin **XML dosyası** içinde **şablonları** bölmesi ve tıklatın **açık**.  
  
     Yeni bir dosya düzenleyicide açılır. Varsayılan XML bildirimi dosyasını içeren `<?xml version="1.0" encoding="utf-8">`.  
  
3. Belge Özellikler penceresinde, Gözat düğmesine tıklayın (**...** ) üzerinde **şemaları** alan.  
  
     **XSD şemaları** iletişim kutusu görüntülenir.  
  
4. **Ekle**'yi tıklatın.  
  
     **Açık XSD şeması** iletişim kutusu görüntülenir.  
  
5. HireDate.xsd dosyasını seçin ve tıklayın **açık**.  
  
6. **Tamam**'ı tıklatın.  
  
     XML Şeması sunulmuştur XML belge ile ilişkilendirilmiş. XML Şeması, belgeyi doğrulamak için kullanılır. Bu ayrıca, IntelliSense tarafından geçerli öğe üye listesini doldurmak için kullanılır.  
  
### <a name="to-add-data"></a>Veri eklemek için  
  
1. Tür `<` Düzenleyicisi bölmesinde.  
  
     Üye listesi, mümkün olan öğeleri görüntüler:  
  
    - **!--** açıklama eklemek için.  
  
    - **! DOCTYPE** belge türü eklemek için.  
  
    - **?** bir işlem yönergesi eklemek için.  
  
    - **çalışan** kök öğe eklemek için.  
  
2. Seçin  **\<!--** bir açıklama düğümü Ekle ve ENTER tuşuna basın.  
  
     Düzenleyici, açıklama bitiş etiketi ekler ve başlangıç ve bitiş açıklama etiketleri arasında imleci geçir yerleştirir.  
  
3. Yazın **Test XML dosyası**.  
  
4. Yeni bir satıra yazın `<`seçip **çalışan** üye listesinde.  
  
     Düzenleyicisi bir XML öğesi ekler `<employee`. Bu noktada öğenin öznitelikleri ekleyebilir veya yazarak başlangıç etiketi kapatabilirsiniz `>`.  
  
5. Tür `>` etiketi kapatın.  
  
6. Düzenleyici bitiş etiketi ekler. Bitiş etiketi, bir doğrulama hatası gösteren dalgalı alt çizgi ile eklenir. Araç ipucu görüntülenir: ' % S'öğesi 'çalışanı' içeriği eksik sahip. 'ID' bekleniyor.  
  
7. Tür `<` seçip **kimliği** üye listesinde. Yazarak `>`.  
  
     Düzenleyici XML öğesi ekler `<ID></ID>`ve imleci kimliği başlattığınızda etiketi yerleştirir.  
  
8. Tür **abc**.  
  
     **Abc** metin dalgalı çizgi vardır. Araç ipucu görüntülenir: 'ID' öğesi, kendi veri türüne göre geçersiz bir değere sahip.  
  
9. Kimlik öğesi üzerinde sağ tıklatın ve seçin **tanıma**.  
  
     Düzenleyici hireDate.xsd dosya yeni bir belge penceresi açılır ve imleç kimliği şema öğesi tanımını yerleştirir.  
  
10. XML dosyasına dönün ve Değiştir **abc** metinle **123**.  
  
     Araç ipucu ve dalgalı çizgi altında ID öğesinin değerine temizlenir. Araç ipucu için çalışan bitiş etiketi, artık şu ileti görüntülenir: ' % S'öğesi 'çalışanı' içeriği eksik sahip. Beklenen 'alım tarih'.  
  
11. Yazın, sonra kimliği bitiş etiketi imleci `<`, işe alım tarihi üye listesinden seçin ve ardından yazın `>`.  
  
     Düzenleyici XML öğesi ekler `<hire-date></hire-date>`ve imleci başlangıç alım tarihi sonra etiketi yerleştirir.  
  
12. Yazın **2003-01-10** alım tarih değeri.  
  
### <a name="to-format-the-xml-document"></a>XML belgesi biçimlendirmek için  
  
1. Seçin **belgeyi Biçimlendir** XML Düzenleyicisi araç çubuğundan düğme.  
  
     XML belgesi biçimlendirilir.  
  
### <a name="to-save-the-xml-document"></a>XML belgesi kaydetmek için  
  
1. Gelen **dosya** menüsünde **Kaydet**.  
  
     **Dosyayı farklı Kaydet** iletişim kutusu görüntülenir. Varsayılan dosya adı 'XMLFile1' dir.  
  
2. XML belgesi için konum ve dosya adını girin ve tıklayın **Kaydet**.  
  
## <a name="hiredatexsd-file"></a>hireDate.xsd dosyası  
 Aşağıdaki şema dosyası izlenecek yol tarafından kullanılır.  
  
```  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XML Düzenleyicisi](../xml-tools/xml-editor.md)
