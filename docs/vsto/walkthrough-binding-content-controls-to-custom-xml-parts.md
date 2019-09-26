---
title: 'İzlenecek yol: İçerik denetimlerini özel XML bölümlerine bağlama'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- PlainTextContentControl, binding to a custom XML part
- custom XML parts, binding to content controls
- content controls [Office development in Visual Studio], data binding
- data binding [Office development in Visual Studio], content controls
- DropDownListContentControl, binding items to a custom XML part
- DatePickerContentControl, binding to a custom XML part
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: b4c5ea74a1892834b6eaaeb98277918985471ac4
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253920"
---
# <a name="walkthrough-bind-content-controls-to-custom-xml-parts"></a>İzlenecek yol: İçerik denetimlerini özel XML bölümlerine bağlama
  Bu izlenecek yol, Word için belge düzeyi özelleştirmesindeki içerik denetimlerini belgede depolanan XML verilerine nasıl bağlayabileceğinizi gösterir.

 [!INCLUDE[appliesto_wdalldoc](../vsto/includes/appliesto-wdalldoc-md.md)]

 Word, bir belgede *özel XML parçaları*olarak adlandırılan XML verilerini depolamanıza olanak sağlar. İçerik denetimlerini özel bir XML parçasındaki öğelere bağlayarak bu verilerin görüntülenmesini denetleyebilirsiniz. Bu izlenecek yolda örnek belge, özel bir XML bölümünde depolanan çalışan bilgilerini görüntüler. Belgeyi açtığınızda, içerik denetimleri XML öğelerinin değerlerini görüntüler. İçerik denetimlerindeki metinde yaptığınız tüm değişiklikler özel XML bölümüne kaydedilir.

 Bu izlenecek yol aşağıdaki görevleri gösterir:

- Belge düzeyi projesindeki Word belgesine içerik denetimleri ekleme tasarım zamanı.

- XML veri dosyası ve içerik denetimlerine bağlanacak öğeleri tanımlayan bir XML şeması oluşturma.

- XML şemasını belgeye tasarım zamanında ekleme.

- XML dosyasının içeriğini çalışma zamanında belgedeki özel bir XML bölümüne ekleme.

- İçerik denetimlerini özel XML parçasındaki öğelere bağlama.

- XML şemasında <xref:Microsoft.Office.Tools.Word.DropDownListContentControl> tanımlanmış bir değerler kümesine bağlama.

  [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

## <a name="prerequisites"></a>Önkoşullar
 Bu izlenecek yolu tamamlamak için aşağıdaki bileşenlere ihtiyacınız vardır:

- [!INCLUDE[vsto_vsprereq](../vsto/includes/vsto-vsprereq-md.md)]

- Microsoft Word.

## <a name="create-a-new-word-document-project"></a>Yeni bir Word belgesi projesi oluştur
 Yönergede kullanacağınız bir Word belgesi oluşturun.

### <a name="to-create-a-new-word-document-project"></a>Yeni bir Word belgesi projesi oluşturmak için

1. **EmployeeControls**adlı bir Word belgesi projesi oluşturun. Çözüm için yeni bir belge oluşturun. Daha fazla bilgi için [nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

     [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]tasarımcıda yeni Word belgesini açar ve **EmployeeControls** projesini **Çözüm Gezgini**ekler.

## <a name="add-content-controls-to-the-document"></a>Belgeye içerik denetimleri ekleme
 Kullanıcının bir çalışanla ilgili bilgileri görüntüleyebileceği veya düzenleyebileceği üç farklı türde içerik denetimi içeren bir tablo oluşturun.

### <a name="to-add-content-controls-to-the-document"></a>Belgeye içerik denetimleri eklemek için

1. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Tasarımcıda barındırılan Word belgesinde, şeritte **Ekle** sekmesini seçin.

2. **Tablolar** grubunda **tablo**' yı seçin ve 2 sütun ve 3 satır içeren bir tablo ekleyin.

3. Aşağıdaki sütuna benzer olacak şekilde ilk sütuna metin yazın:

   ||
   |-|
   |**Çalışan adı**|
   |**İşe alma tarihi**|
   |**Başlık**|

4. Tablonun ikinci sütununda, ilk satırı ( **çalışan adı**' nın yanında) seçin.

5. Şeritte **Geliştirici** sekmesini seçin.

   > [!NOTE]
   > **Geliştirici** sekmesi görünür değilse, önce onu göstermelisiniz. Daha fazla bilgi için [nasıl yapılır: Şeritte](../vsto/how-to-show-the-developer-tab-on-the-ribbon.md)Geliştirici sekmesini görüntüleyin.

6. **Denetimler** grubunda, ilk hücreye bir <xref:Microsoft.Office.Tools.Word.PlainTextContentControl> eklemek için ![PlainTextContentControl](../vsto/media/plaintextcontrol.gif "PlainTextContentControl") **metin** düğmesini seçin.

7. Tablonun ikinci sütununda, ikinci satırı ( **işe giriş tarihi**' nin yanında) seçin.

8. **Denetimler** grubunda, ikinci hücreye eklemek <xref:Microsoft.Office.Tools.Word.DatePickerContentControl> için **Tarih Seçici** düğmesini ![DatePickerContentControl](../vsto/media/datepicker.gif "DatePickerContentControl") ' i seçin.

9. Tablonun ikinci sütununda, üçüncü satırı ( **başlık**' ın yanında) seçin.

10. **Denetimler** grubunda, son hücreye eklemek <xref:Microsoft.Office.Tools.Word.DropDownListContentControl> için **aşağı açılan liste** düğmesini ![DropDownListContentControl](../vsto/media/dropdownlist.gif "DropDownListContentControl") ' i seçin.

    Bu proje için Kullanıcı arabiriminin tamamı budur. Projeyi Şimdi çalıştırırsanız, ilk satıra metin yazabilir ve ikinci satırdaki bir tarihi seçebilirsiniz. Bir sonraki adım, göstermek istediğiniz verileri bir XML dosyasındaki belgeye eklemektir.

## <a name="create-the-xml-data-file"></a>XML veri dosyası oluşturma
 Genellikle, bir dosya veya veritabanı gibi bir dış kaynaktan özel bir XML bölümünde depolanacak XML verilerini elde edersiniz. Bu kılavuzda, belgedeki içerik denetimlerine bağlayacağınız öğeler tarafından işaretlenen çalışan verilerini içeren bir XML dosyası oluşturacaksınız. Verileri çalışma zamanında kullanılabilir hale getirmek için, XML dosyasını özelleştirme derlemesine bir kaynak olarak ekleyin.

#### <a name="to-create-the-data-file"></a>Veri dosyası oluşturmak için

1. **Proje** menüsünde **Yeni öğe Ekle**' yi seçin.

     **Yeni Öğe Ekle** iletişim kutusu görünür.

2. **Şablonlar** bölmesinde **XML dosyası**' nı seçin.

3. Dosyayı **employees. xml**olarak adlandırın ve ardından **Ekle** düğmesini seçin.

     **Employees. xml** dosyası kod düzenleyicisinde açılır.

4. **Employees. xml** dosyasının içeriğini aşağıdaki metinle değiştirin.

    ```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <employees xmlns="http://schemas.microsoft.com/vsto/samples">
      <employee>
        <name>Karina Leal</name>
        <hireDate>1999-04-01</hireDate>
        <title>Manager</title>
      </employee>
    </employees>
    ```

5. **Çözüm Gezgini**, **employees. xml** dosyasını seçin.

6. **Özellikler** penceresinde **derleme eylemi** özelliğini seçin ve ardından değeri **gömülü kaynak**olarak değiştirin.

     Bu adım, projeyi derlediğinizde XML dosyasını derlemeye bir kaynak olarak katıştırır. Bu, çalışma zamanında XML dosyasının içeriğine erişmenizi sağlar.

## <a name="create-an-xml-schema"></a>XML şeması oluşturma
 Bir içerik denetimini özel bir XML bölümünde tek bir öğeye bağlamak istiyorsanız, bir XML şeması kullanmak zorunda değilsiniz. Ancak, öğesini bir değer <xref:Microsoft.Office.Tools.Word.DropDownListContentControl> kümesine bağlamak için, daha önce oluşturduğunuz XML veri dosyasını doğrulayan bir XML Şeması oluşturmanız gerekir. XML şeması, `title` öğesi için olası değerleri tanımlar. Bu öğeyi daha sonra <xref:Microsoft.Office.Tools.Word.DropDownListContentControl> Bu izlenecek yolda bağlayacaksınız.

#### <a name="to-create-an-xml-schema"></a>Bir XML şeması oluşturmak için

1. **Proje** menüsünde **Yeni öğe Ekle**' yi seçin.

     **Yeni Öğe Ekle** iletişim kutusu görünür.

2. **Şablonlar** bölmesinde, **XML şeması**' nı seçin.

3. Şemayı **employees. xsd** olarak adlandırın ve **Ekle** düğmesini seçin.

     Şema Tasarımcısı açılır.

4. **Çözüm Gezgini**, **employees. xsd**için kısayol menüsünü açın ve **kodu görüntüle**' yi seçin.

5. **Employees. xsd** dosyasının içeriğini aşağıdaki şema ile değiştirin.

    ```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <xs:schema xmlns="http://schemas.microsoft.com/vsto/samples"
        targetNamespace="http://schemas.microsoft.com/vsto/samples"
        xmlns:xs="http://www.w3.org/2001/XMLSchema"
        elementFormDefault="qualified">
      <xs:element name="employees" type="EmployeesType"></xs:element>
      <xs:complexType name="EmployeesType">
        <xs:all>
          <xs:element name="employee" type="EmployeeType"/>
        </xs:all>
      </xs:complexType>
      <xs:complexType name="EmployeeType">
        <xs:sequence>
          <xs:element name="name" type="xs:string" minOccurs="1" maxOccurs="1"/>
          <xs:element name="hireDate" type="xs:date" minOccurs="1" maxOccurs="1"/>
          <xs:element name="title" type="TitleType" minOccurs="1" maxOccurs="1"/>
        </xs:sequence>
      </xs:complexType>
      <xs:simpleType name="TitleType">
        <xs:restriction base="xs:string">
          <xs:enumeration value ="Engineer"/>
          <xs:enumeration value ="Designer"/>
          <xs:enumeration value ="Manager"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:schema>
    ```

6. Değişikliklerinizi **employees. xml** ve **employees. xsd** dosyalarına kaydetmek Için **Dosya** menüsünde **Tümünü Kaydet** ' e tıklayın.

## <a name="attach-the-xml-schema-to-the-document"></a>XML şemasını belgeye iliştirme
 XML şemasını, <xref:Microsoft.Office.Tools.Word.DropDownListContentControl> `title` öğesinin geçerli değerlerine bağlamak için belgeye iliştirmelidir.

### <a name="to-attach-the-xml-schema-to-the-document--includeword_15_shortvstoincludesword-15-short-mdmd"></a>XML şemasını belgeye eklemek için ( [!INCLUDE[Word_15_short](../vsto/includes/word-15-short-md.md)])

1. Tasarımcıda **EmployeeControls. docx** ' i etkinleştirin.

2. Şeritte **Geliştirici** sekmesini seçin ve ardından **Eklentiler düğmesini seçin** .

3. **Şablonlar ve eklentiler** iletişim kutusunda, **XML şeması** sekmesini seçin ve ardından **şema ekle** düğmesini seçin.

4. Daha önce oluşturduğunuz, proje dizininizde bulunan **employees. xsd** şemasına gidin ve sonra **Aç** düğmesini seçin.

5. **Şema ayarları** Iletişim kutusunda **Tamam** düğmesini seçin.

6. **Şablonlar ve eklentiler** iletişim kutusunu kapatmak için **Tamam** düğmesini seçin.

### <a name="to-attach-the-xml-schema-to-the-document-word-2010"></a>XML şemasını belgeye eklemek için (Word 2010)

1. Tasarımcıda **EmployeeControls. docx** ' i etkinleştirin.

2. Şeritte **Geliştirici** sekmesini seçin.

3. **XML** grubunda **şema** düğmesini seçin.

4. **Şablonlar ve eklentiler** iletişim kutusunda, **XML şeması** sekmesini seçin ve ardından **şema ekle** düğmesini seçin.

5. Daha önce oluşturduğunuz ve proje dizininizde bulunan **employees. xsd** şemasına gidin ve **Aç** düğmesini seçin.

6. **Şema ayarları** Iletişim kutusunda **Tamam** düğmesini seçin.

7. **Şablonlar ve eklentiler** iletişim kutusunu kapatmak için **Tamam** düğmesini seçin.

     **XML yapısı** görev bölmesi açılır.

8. **XML yapısı** görev bölmesini kapatın.

## <a name="add-a-custom-xml-part-to-the-document"></a>Belgeye özel bir XML bölümü ekleme
 İçerik denetimlerini XML dosyasındaki öğelere bağlayabilmeniz için önce, XML dosyasının içeriğini belgedeki yeni bir özel XML bölümüne eklemeniz gerekir.

### <a name="to-add-a-custom-xml-part-to-the-document"></a>Belgeye özel bir XML bölümü eklemek için

1. **Çözüm Gezgini**' de, **ThisDocument.cs** veya **ThisDocument. vb**kısayol menüsünü açın ve **kodu görüntüle**' yi seçin.

2. `ThisDocument` Sınıfına aşağıdaki bildirimleri ekleyin. Bu kod, belgeye özel bir XML bölümü eklemek için kullanacağınız birkaç nesne bildirir.

     [!code-csharp[Trin_ContentControlXmlPartWalkthrough#1](../vsto/codesnippet/CSharp/EmployeeControls/ThisDocument.cs#1)]
     [!code-vb[Trin_ContentControlXmlPartWalkthrough#1](../vsto/codesnippet/VisualBasic/EmployeeControls/ThisDocument.vb#1)]

3. `ThisDocument` Sınıfına aşağıdaki yöntemi ekleyin. Bu yöntem, derlemede bir kaynak olarak katıştırılmış XML veri dosyasının içeriğini alır ve içeriği bir XML dizesi olarak döndürür.

     [!code-csharp[Trin_ContentControlXmlPartWalkthrough#3](../vsto/codesnippet/CSharp/EmployeeControls/ThisDocument.cs#3)]
     [!code-vb[Trin_ContentControlXmlPartWalkthrough#3](../vsto/codesnippet/VisualBasic/EmployeeControls/ThisDocument.vb#3)]

4. `ThisDocument` Sınıfına aşağıdaki yöntemi ekleyin. `AddCustomXmlPart` Yöntemi yöntemine geçirilen bir XML dizesi içeren yeni bir özel XML bölümü oluşturur.

     Özel XML bölümünün yalnızca bir kez oluşturulduğundan emin olmak için, yöntem yalnızca belgede eşleşen bir GUID 'e sahip özel bir XML bölümü yoksa özel XML bölümünü oluşturur. Bu yöntem ilk kez çağrıldığında, <xref:Microsoft.Office.Core._CustomXMLPart.Id%2A> özelliğinin `employeeXMLPartID` değerini dizeye kaydeder. `employeeXMLPartID` Dize değeri, <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.CachedAttribute> özniteliği kullanılarak bildirildiği için belgede kalıcı hale getirilir.

     [!code-csharp[Trin_ContentControlXmlPartWalkthrough#4](../vsto/codesnippet/CSharp/EmployeeControls/ThisDocument.cs#4)]
     [!code-vb[Trin_ContentControlXmlPartWalkthrough#4](../vsto/codesnippet/VisualBasic/EmployeeControls/ThisDocument.vb#4)]

## <a name="bind-the-content-controls-to-elements-in-the-custom-xml-part"></a>İçerik denetimlerini özel XML bölümünde öğelere bağlama
 Her içerik denetiminin **XmlMapping** özelliğini kullanarak her içerik DENETIMINI özel XML parçasındaki bir öğeye bağlayın.

### <a name="to-bind-the-content-controls-to-elements-in-the-custom-xml-part"></a>İçerik denetimlerini özel XML bölümünde öğelere bağlamak için

1. `ThisDocument` Sınıfına aşağıdaki yöntemi ekleyin. Bu yöntem, <xref:Microsoft.Office.Tools.Word.DatePickerContentControl>her IÇERIK denetimini özel XML parçasındaki bir öğeye bağlar ve öğesinin tarih görüntüleme biçimini ayarlar.

     [!code-csharp[Trin_ContentControlXmlPartWalkthrough#5](../vsto/codesnippet/CSharp/EmployeeControls/ThisDocument.cs#5)]
     [!code-vb[Trin_ContentControlXmlPartWalkthrough#5](../vsto/codesnippet/VisualBasic/EmployeeControls/ThisDocument.vb#5)]

## <a name="run-your-code-when-the-document-is-opened"></a>Belge açıldığında kodunuzu çalıştırın
 Özel XML bölümünü oluşturun ve belge açıldığında özel denetimleri verilere bağlayın.

### <a name="to-run-your-code-when-the-document-is-opened"></a>Belge açıldığında kodunuzu çalıştırmak için

1. Aşağıdaki kodu `ThisDocument_Startup` `ThisDocument` sınıfının yöntemine ekleyin. Bu kod, **employees. xml** dosyasındaki XML dizesini alır, XML dizesini belgedeki yeni BIR özel XML bölümüne ekler ve içerik DENETIMLERINI özel XML bölümündeki öğelere bağlar.

     [!code-csharp[Trin_ContentControlXmlPartWalkthrough#2](../vsto/codesnippet/CSharp/EmployeeControls/ThisDocument.cs#2)]
     [!code-vb[Trin_ContentControlXmlPartWalkthrough#2](../vsto/codesnippet/VisualBasic/EmployeeControls/ThisDocument.vb#2)]

## <a name="test-the-project"></a>Projeyi test etme
 Belgeyi açtığınızda, içerik denetimleri özel XML parçasındaki öğelerden verileri görüntüler. **Employees. xsd** dosyasında <xref:Microsoft.Office.Tools.Word.DropDownListContentControl> tanımlanan, `title` öğesi için geçerli üç değerden birini seçmek için öğesine tıklayabilirsiniz. İçerik denetimlerindeki verileri düzenlerseniz, yeni değerler belgedeki özel XML bölümüne kaydedilir.

### <a name="to-test-the-content-controls"></a>İçerik denetimlerini test etmek için

1. Projeyi çalıştırmak için **F5** tuşuna basın.

2. Belgedeki tablonun aşağıdaki tabloya benzediğini doğrulayın. İkinci sütundaki dizelerin her biri belgedeki özel XML bölümündeki bir öğeden elde edilir.

    |||
    |-|-|
    |**Çalışan adı**|**Karina Taal**|
    |**İşe alma tarihi**|**1 Nisan 1999**|
    |**Başlık**|**Manager**|

3. **Çalışan adı** hücresinin sağ tarafındaki hücreyi seçin ve farklı bir ad yazın.

4. **Işe alma tarihi** hücresinin sağ tarafındaki hücreyi seçin ve tarih seçicide farklı bir tarih seçin.

5. **Başlık** hücresinin sağ tarafındaki hücreyi seçin ve açılan listeden yeni bir öğe seçin.

6. Belgeyi kaydedin ve kapatın.

7. Dosya Gezgini 'nde, projenizin konumu altındaki *\Bin\debug* klasörünü açın.

8. **EmployeeControls. docx** için kısayol menüsünü açın ve **Yeniden Adlandır**' ı seçin.

9. Dosyayı **EmployeeControls. docx. zip**olarak adlandırın.

     **EmployeeControls. docx** BELGESI Open XML biçiminde kaydedilir. Bu belgeyi *. zip* dosya adı uzantısıyla yeniden adlandırarak belgenin içeriğini inceleyebilirsiniz. Open XML hakkında daha fazla bilgi için bkz. [Office (2007) Open XML dosya biçimlerini tanıtma](/previous-versions/office/developer/office-2007/aa338205(v=office.12))teknik makalesi.

10. **EmployeeControls. docx. zip** dosyasını açın.

11. **CustomXml** klasörünü açın.

12. **Item2. xml** için kısayol menüsünü açın ve **Aç**öğesini seçin.

     Bu dosya, belgeye eklediğiniz özel XML bölümünü içerir.

13. `name`, Veöğelerinin`title` belgedeki içerik denetimlerine girdiğiniz yeni değerleri içerdiğini doğrulayın. `hireDate`

14. **Item2. xml** dosyasını kapatın.

## <a name="next-steps"></a>Sonraki adımlar
 Aşağıdaki konulardan içerik denetimlerini kullanma hakkında daha fazla bilgi edinebilirsiniz:

- Bir şablon oluşturmak için tüm kullanılabilir içerik denetimlerini kullanın. Daha fazla bilgi için bkz [. İzlenecek yol: İçerik denetimlerini](../vsto/walkthrough-creating-a-template-by-using-content-controls.md)kullanarak bir şablon oluşturun.

- Belge kapalıyken özel XML bölümlerinde verileri değiştirin. Kullanıcının belgeyi bir sonraki açışında, XML öğelerine bağlanan içerik denetimleri yeni verileri görüntüler.

- Belge parçalarını korumak için içerik denetimlerini kullanın. Daha fazla bilgi için [nasıl yapılır: İçerik denetimlerini](../vsto/how-to-protect-parts-of-documents-by-using-content-controls.md)kullanarak belge parçalarını koruyun.

## <a name="see-also"></a>Ayrıca bkz.
- [Genişletilmiş nesneleri kullanarak Word 'Ü otomatikleştirme](../vsto/automating-word-by-using-extended-objects.md)
- [İçerik denetimleri](../vsto/content-controls.md)
- [Nasıl yapılır: Word belgelerine içerik denetimleri ekleme](../vsto/how-to-add-content-controls-to-word-documents.md)
- [Nasıl yapılır: İçerik denetimlerini kullanarak belge bölümlerini koruma](../vsto/how-to-protect-parts-of-documents-by-using-content-controls.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
