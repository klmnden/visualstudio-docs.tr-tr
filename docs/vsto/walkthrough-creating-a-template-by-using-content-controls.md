---
title: 'İzlenecek yol: İçerik denetimlerini kullanarak şablon oluşturma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- building blocks [Office development in Visual Studio]
- Word [Office development in Visual Studio], creating documents
- content controls [Office development in Visual Studio], adding to documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ffb7d7f9ad5453d38709802bf5e004c07bb09622
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255583"
---
# <a name="walkthrough-create-a-template-by-using-content-controls"></a>İzlenecek yol: İçerik denetimlerini kullanarak şablon oluşturma
  Bu izlenecek yol, bir Microsoft Office sözcük şablonunda yapılandırılmış ve yeniden kullanılabilir içerik oluşturmak için içerik denetimleri kullanan belge düzeyi özelleştirmesi oluşturmayı gösterir.

 [!INCLUDE[appliesto_wdalldoc](../vsto/includes/appliesto-wdalldoc-md.md)]

 Word, *derleme blokları*adlı yeniden kullanılabilir belge bölümlerinin bir koleksiyonunu oluşturmanızı sağlar. Bu izlenecek yol, derleme blokları olarak iki tablo oluşturmayı gösterir. Her tablo, düz metin veya tarihler gibi farklı türlerde içerik içerebilen çeşitli içerik denetimleri içerir. Tablolardan biri bir çalışanla ilgili bilgiler içerir ve diğer tablo müşteri geri bildirimi içerir.

 Şablondan bir belge oluşturduktan sonra, şablonda kullanılabilir yapı taşlarını görüntüleyen birkaç <xref:Microsoft.Office.Tools.Word.BuildingBlockGalleryContentControl> nesne kullanarak, tabloya her birini ekleyebilirsiniz.

 Bu izlenecek yol aşağıdaki görevleri gösterir:

- Tasarım zamanında bir Word şablonunda içerik denetimleri içeren tablolar oluşturma.

- Bir Birleşik giriş kutusu içerik denetimi ve açılan liste içerik denetimini programlı olarak doldurma.

- Kullanıcıların belirtilen bir tabloyu düzenlemesini önler.

- Bir şablonun yapı taşı koleksiyonuna tablo ekleme.

- Şablonda kullanılabilir yapı taşlarını görüntüleyen bir içerik denetimi oluşturma.

  [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

## <a name="prerequisites"></a>Önkoşullar
 Bu izlenecek yolu tamamlamak için aşağıdaki bileşenlere ihtiyacınız vardır:

- [!INCLUDE[vsto_vsprereq](../vsto/includes/vsto-vsprereq-md.md)]

- Microsoft Word.

## <a name="create-a-new-word-template-project"></a>Yeni bir Word şablonu projesi oluştur
 Kullanıcıların kendi kopyalarını kolayca oluşturabilmesi için bir Word şablonu oluşturun.

### <a name="to-create-a-new-word-template-project"></a>Yeni bir Word şablonu projesi oluşturmak için

1. **MyBuildingBlockTemplate**adlı bir Word şablonu projesi oluşturun. Sihirbazda, çözümde yeni bir belge oluşturun. Daha fazla bilgi için [nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

     [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]tasarımcıda yeni Word şablonunu açar ve **Çözüm Gezgini**Için **MyBuildingBlockTemplate** projesini ekler.

## <a name="create-the-employee-table"></a>Çalışan tablosu oluşturma
 Kullanıcının bir çalışanla ilgili bilgi girebileceği, dört farklı içerik denetimi türü içeren bir tablo oluşturun.

### <a name="to-create-the-employee-table"></a>Çalışan tablosu oluşturmak için

1. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Tasarımcıda barındırılan Word şablonunda, şeritte **Ekle** sekmesine tıklayın.

2. **Tablolar** grubunda **tablo**' ya tıklayın ve iki sütunlu ve dört satır içeren bir tablo ekleyin.

3. Aşağıdaki sütuna benzer olacak şekilde ilk sütuna metin yazın:

   ||
   |-|
   |**Çalışan adı**|
   |**İşe alma tarihi**|
   |**Başlık**|
   |**Resmin**|

4. İkinci sütundaki ( **çalışan adı**' nın yanında) ilk hücreye tıklayın.

5. Şeritte **Geliştirici** sekmesine tıklayın.

   > [!NOTE]
   > **Geliştirici** sekmesi görünür değilse, önce onu göstermelisiniz. Daha fazla bilgi için [nasıl yapılır: Şeritte](../vsto/how-to-show-the-developer-tab-on-the-ribbon.md)Geliştirici sekmesini görüntüleyin.

6. **Denetimler** grubunda, ilk hücreye bir <xref:Microsoft.Office.Tools.Word.PlainTextContentControl> eklemek için ![PlainTextContentControl](../vsto/media/plaintextcontrol.gif "PlainTextContentControl") **metin** düğmesine tıklayın.

7. İkinci sütundaki ikinci hücreye ( **işe giriş tarihi**' nin yanında) tıklayın.

8. **Denetimler** grubunda, ikinci hücreye eklemek <xref:Microsoft.Office.Tools.Word.DatePickerContentControl> için **Tarih Seçici** düğmesine ![DatePickerContentControl](../vsto/media/datepicker.gif "DatePickerContentControl") ' e tıklayın.

9. İkinci sütundaki üçüncü hücreye ( **başlık**' ın yanında) tıklayın.

10. **Denetimler** grubunda, üçüncü hücreye eklemek <xref:Microsoft.Office.Tools.Word.ComboBoxContentControl> için **Birleşik giriş kutusu** düğmesini ![ComboBoxContentControl](../vsto/media/combobox.gif "ComboBoxContentControl") öğesine tıklayın.

11. İkinci sütundaki son hücreye ( **resim**' in yanında) tıklayın.

12. **Denetimler** grubunda, son hücreye bir <xref:Microsoft.Office.Tools.Word.PictureContentControl> eklemek için, **resim içerik denetim** düğmesine ![PictureContentControl](../vsto/media/pictcontentcontrol.gif "PictureContentControl") ' e tıklayın.

## <a name="create-the-customer-feedback-table"></a>Müşteri geri bildirim tablosu oluşturma
 Kullanıcının müşteri geribildirim bilgilerini girebileceği üç farklı türde içerik denetimi içeren bir tablo oluşturun.

### <a name="to-create-the-customer-feedback-table"></a>Müşteri geri bildirim tablosu oluşturmak için

1. Word şablonunda, daha önce eklediğiniz çalışan tablosundan sonraki satıra tıklayın ve yeni bir paragraf eklemek için **ENTER** tuşuna basın.

2. Şeritte **Ekle** sekmesine tıklayın.

3. **Tablolar** grubunda **tablo**' ya tıklayın ve iki sütunlu ve üç satır içeren bir tablo ekleyin.

4. Aşağıdaki sütuna benzer olacak şekilde ilk sütuna metin yazın:

   ||
   |-|
   |**Müşteri adı**|
   |**Memnuniyet derecesi**|
   |**Açıklamalar**|

5. İkinci sütunun ilk hücresini ( **müşteri adı**' nın yanında) tıklatın.

6. Şeritte **Geliştirici** sekmesine tıklayın.

7. **Denetimler** grubunda, ilk hücreye bir <xref:Microsoft.Office.Tools.Word.PlainTextContentControl> eklemek için ![PlainTextContentControl](../vsto/media/plaintextcontrol.gif "PlainTextContentControl") **metin** düğmesine tıklayın.

8. İkinci sütunun ikinci hücresinde ( **memnuniyet derecesi**' nin yanında) tıklayın.

9. **Denetimler** grubunda, ikinci hücreye eklemek <xref:Microsoft.Office.Tools.Word.DropDownListContentControl> için **aşağı açılan liste** düğmesine ![DropDownListContentControl](../vsto/media/dropdownlist.gif "DropDownListContentControl") ' e tıklayın.

10. İkinci sütunun son hücresine ( **Yorumlar**' ın yanında) tıklayın.

11. **Denetimler** grubunda, son hücreye bir <xref:Microsoft.Office.Tools.Word.RichTextContentControl> eklemek **için zengin metin** düğmesini ![RichTextContentControl](../vsto/media/richtextcontrol.gif "RichTextContentControl") ' e tıklayın.

## <a name="populate-the-combo-box-and-drop-down-list-programmatically"></a>Birleşik giriş kutusunu ve açılan listeyi programlı olarak doldur
 Içindeki[!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] **Özellikler** penceresini kullanarak tasarım zamanında içerik denetimlerini başlatabilirsiniz. Ayrıca, bunları çalışma zamanında başlatabilir, bu da başlangıç durumlarını dinamik olarak ayarlamanıza olanak sağlar. Bu izlenecek yol için, bu nesnelerin nasıl çalıştığını görebilmeniz için çalışma <xref:Microsoft.Office.Tools.Word.ComboBoxContentControl> zamanında <xref:Microsoft.Office.Tools.Word.DropDownListContentControl> ve içindeki girişleri doldurmak üzere kodu kullanın.

### <a name="to-modify-the-ui-of-the-content-controls-programmatically"></a>İçerik denetimlerinin Kullanıcı arabirimini program aracılığıyla değiştirmek için

1. **Çözüm Gezgini**' de, **ThisDocument.cs** veya **ThisDocument. vb**öğesine sağ tıklayın ve ardından **kodu görüntüle**' ye tıklayın.

2. `ThisDocument` Sınıfına aşağıdaki kodu ekleyin. Bu kod, Bu izlenecek yolda daha sonra kullanacağınız birkaç nesne bildirir.

     [!code-vb[Trin_ContentControlTemplateWalkthrough#1](../vsto/codesnippet/VisualBasic/ContentControlTemplateWalkthrough/ThisDocument.vb#1)]
     [!code-csharp[Trin_ContentControlTemplateWalkthrough#1](../vsto/codesnippet/CSharp/ContentControlTemplateWalkthrough/ThisDocument.cs#1)]

3. Aşağıdaki kodu `ThisDocument_Startup` `ThisDocument` sınıfının yöntemine ekleyin. Bu kod, tabloları <xref:Microsoft.Office.Tools.Word.ComboBoxContentControl> ve <xref:Microsoft.Office.Tools.Word.DropDownListContentControl> tablolarına ekler ve Kullanıcı bunları düzenlemeden önce bu denetimlerin her birinde görüntülenen yer tutucu metni ayarlar.

     [!code-vb[Trin_ContentControlTemplateWalkthrough#2](../vsto/codesnippet/VisualBasic/ContentControlTemplateWalkthrough/ThisDocument.vb#2)]
     [!code-csharp[Trin_ContentControlTemplateWalkthrough#2](../vsto/codesnippet/CSharp/ContentControlTemplateWalkthrough/ThisDocument.cs#2)]

## <a name="prevent-users-from-editing-the-employee-table"></a>Kullanıcıların çalışan tablosunu düzenlemesini engelle
 Daha önce, çalışan tablosunu korumak için bildirdiğiniz nesneyikullanın.<xref:Microsoft.Office.Tools.Word.GroupContentControl> Tablo korunduktan sonra kullanıcılar tablodaki içerik denetimlerini düzenlemeye devam edebilir. Ancak, ilk sütundaki metni düzenleyemez veya tablo ve sütun ekleme veya silme gibi diğer yollarla tabloyu değiştiremezsiniz. Bir <xref:Microsoft.Office.Tools.Word.GroupContentControl> belgenin bir bölümünü korumak için ' nin nasıl kullanılacağı hakkında daha fazla bilgi için bkz. [içerik denetimleri](../vsto/content-controls.md).

### <a name="to-prevent-users-from-editing-the-employee-table"></a>Kullanıcıların çalışan tablosunu düzenlemesini engellemek için

1. Önceki adımda eklediğiniz koddan sonra, `ThisDocument_Startup` `ThisDocument` sınıfının yöntemine aşağıdaki kodu ekleyin. Bu kod, kullanıcıların tabloyu daha önce bildirdiğiniz <xref:Microsoft.Office.Tools.Word.GroupContentControl> nesnenin içine yerleştirerek çalışan tablosunu düzenlemesini engeller.

     [!code-vb[Trin_ContentControlTemplateWalkthrough#3](../vsto/codesnippet/VisualBasic/ContentControlTemplateWalkthrough/ThisDocument.vb#3)]
     [!code-csharp[Trin_ContentControlTemplateWalkthrough#3](../vsto/codesnippet/CSharp/ContentControlTemplateWalkthrough/ThisDocument.cs#3)]

## <a name="add-the-tables-to-the-building-block-collection"></a>Tabloları yapı taşı koleksiyonuna ekleme
 Kullanıcıların belge içine oluşturduğunuz tabloları ekleyebilmeleri için şablondaki belge yapı taşları koleksiyonuna tablo ekleyin. Belge yapı taşları hakkında daha fazla bilgi için bkz. [içerik denetimleri](../vsto/content-controls.md).

### <a name="to-add-the-tables-to-the-building-blocks-in-the-template"></a>Şablondaki yapı taşlarına tablo eklemek için

1. Önceki adımda eklediğiniz koddan sonra, `ThisDocument_Startup` `ThisDocument` sınıfının yöntemine aşağıdaki kodu ekleyin. Bu kod, şablondaki tüm yeniden kullanılabilir yapı taşlarını içeren Microsoft. Office. Interop. Word. Buildingblockendenemeler koleksiyonuna tabloları içeren yeni yapı taşları ekler. Yeni yapı taşları, **çalışan ve müşteri bilgileri** adlı yeni bir kategoride tanımlanır ve yapı taşı türü `Microsoft.Office.Interop.Word.WdBuildingBlockTypes.wdTypeCustom1`atanır.

     [!code-vb[Trin_ContentControlTemplateWalkthrough#4](../vsto/codesnippet/VisualBasic/ContentControlTemplateWalkthrough/ThisDocument.vb#4)]
     [!code-csharp[Trin_ContentControlTemplateWalkthrough#4](../vsto/codesnippet/CSharp/ContentControlTemplateWalkthrough/ThisDocument.cs#4)]

2. Önceki adımda eklediğiniz koddan sonra, `ThisDocument_Startup` `ThisDocument` sınıfının yöntemine aşağıdaki kodu ekleyin. Bu kod, şablondan tabloları siler. Tablolar artık gerekli değildir, çünkü bunları şablondaki yeniden kullanılabilir yapı taşları galerisine eklemiş olursunuz. Kod ilk olarak belgeyi tasarım moduna geçirir, böylece korumalı çalışan tablosu silinebilir.

     [!code-vb[Trin_ContentControlTemplateWalkthrough#5](../vsto/codesnippet/VisualBasic/ContentControlTemplateWalkthrough/ThisDocument.vb#5)]
     [!code-csharp[Trin_ContentControlTemplateWalkthrough#5](../vsto/codesnippet/CSharp/ContentControlTemplateWalkthrough/ThisDocument.cs#5)]

## <a name="create-a-content-control-that-displays-the-building-blocks"></a>Yapı taşlarını görüntüleyen bir içerik denetimi oluşturma
 Daha önce oluşturduğunuz yapı taşları (yani tablolar) için erişim sağlayan bir içerik denetimi oluşturun. Kullanıcılar, tabloları belgeye eklemek için bu denetime tıklabilirler.

### <a name="to-create-a-content-control-that-displays-the-building-blocks"></a>Yapı taşlarını görüntüleyen bir içerik denetimi oluşturmak için

1. Önceki adımda eklediğiniz koddan sonra, `ThisDocument_Startup` `ThisDocument` sınıfının yöntemine aşağıdaki kodu ekleyin. Bu kod, <xref:Microsoft.Office.Tools.Word.BuildingBlockGalleryContentControl> daha önce bildirdiğiniz nesneyi başlatır. , <xref:Microsoft.Office.Tools.Word.BuildingBlockGalleryContentControl> **Çalışan ve müşteri bilgilerinde** tanımlanan ve yapı blok türüne `Microsoft.Office.Interop.Word.WdBuildingBlockTypes.wdTypeCustom1`sahip olan tüm yapı taşlarını görüntüler.

     [!code-vb[Trin_ContentControlTemplateWalkthrough#6](../vsto/codesnippet/VisualBasic/ContentControlTemplateWalkthrough/ThisDocument.vb#6)]
     [!code-csharp[Trin_ContentControlTemplateWalkthrough#6](../vsto/codesnippet/CSharp/ContentControlTemplateWalkthrough/ThisDocument.cs#6)]

## <a name="test-the-project"></a>Projeyi test etme
 Kullanıcılar, çalışan tablosunu veya müşteri geri bildirim tablosunu eklemek için belgedeki yapı taşı galeri denetimlerine tıklabilirler. Kullanıcılar, her iki tabloda bulunan içerik denetimlerindeki yanıtları yazabilir veya seçebilir. Kullanıcılar, müşteri geri bildirim tablosunun diğer bölümlerini değiştirebilir, ancak çalışan tablosunun diğer bölümlerini değiştirememelidir.

### <a name="to-test-the-employee-table"></a>Çalışan tablosunu test etmek için

1. Projeyi çalıştırmak için **F5** tuşuna basın.

2. İlk yapı taşı galeri içerik denetimini göstermek için **ilk yapı taşınızı Seç** ' e tıklayın.

3. Denetimdeki **Özel Galeri 1** başlığının yanındaki açılan oka tıklayın ve **çalışan tablosu**' nu seçin.

4. **Çalışan adı** hücresinin sağındaki hücreye tıklayın ve bir ad yazın.

     Bu hücreye yalnızca metin ekleyebildiğinizi doğrulayın. Kullanıcıların <xref:Microsoft.Office.Tools.Word.PlainTextContentControl> , resim veya tablo gibi diğer içerik türlerini değil yalnızca metin eklemesine izin verir.

5. **Işe alım tarihi** hücresinin sağındaki hücreye tıklayın ve tarih seçicide bir tarih seçin.

6. **Başlık** hücresinin sağındaki hücreye tıklayın ve Birleşik giriş kutusunda iş başlıklarından birini seçin.

     İsteğe bağlı olarak, listede olmayan bir iş başlığının adını yazın. Bu, <xref:Microsoft.Office.Tools.Word.ComboBoxContentControl> kullanıcıların bir giriş listesinden seçim yapmasına veya kendi girişlerini yazmalarına olanak sağladığından mümkündür.

7. **Resim** hücresinin sağ tarafındaki hücrede simgesine tıklayın ve görüntülenecek resme gidin.

8. Tabloya satır veya sütun eklemeyi deneyin ve tablodaki satırları ve sütunları silmeyi deneyin. Tabloyu değiştiremediğinizi doğrulayın. , <xref:Microsoft.Office.Tools.Word.GroupContentControl> Herhangi bir değişiklik yapmanızı önler.

### <a name="to-test-the-customer-feedback-table"></a>Müşteri geri bildirim tablosunu test etmek için

1. İkinci yapı taşı galerisi içerik denetimini göstermek için **ikinci yapı taşınızı Seç** ' e tıklayın.

2. Denetimdeki **Özel Galeri 1** başlığının yanındaki açılan oka tıklayın ve **Müşteri tablosu**' nu seçin.

3. **Müşteri adı** hücresinin sağındaki hücreye tıklayın ve bir ad yazın.

4. **Memnuniyet derecesi** hücresinin sağındaki hücreye tıklayın ve kullanılabilir seçeneklerden birini belirleyin.

     Kendi girdinizi yazmadiğinizi doğrulayın. , <xref:Microsoft.Office.Tools.Word.DropDownListContentControl> Kullanıcıların yalnızca bir giriş listesinden seçmesine izin verir.

5. **Açıklamalar** hücresinin sağındaki hücreye tıklayın ve bazı açıklamalar yazın.

     İsteğe bağlı olarak, resim veya katıştırılmış tablo gibi metin dışında bir içerik ekleyin. Bunun nedeni, <xref:Microsoft.Office.Tools.Word.RichTextContentControl> kullanıcıların metin dışında içerik eklemesine olanak sağlar.

6. Tabloya satır veya sütun ekleyebildiğinizi ve tablodaki satırları ve sütunları silediğinizi doğrulayın. Bu, tabloyu bir <xref:Microsoft.Office.Tools.Word.GroupContentControl>içine yerleştirerek korumamış olmanız nedeniyle mümkündür.

7. Şablonu kapatın.

## <a name="next-steps"></a>Sonraki adımlar
 Bu konudan içerik denetimlerini kullanma hakkında daha fazla bilgi edinebilirsiniz:

- İçerik denetimlerini, bir belgeye gömülü olan özel XML parçaları olarak da adlandırılan XML parçalarına bağlayın. Daha fazla bilgi için bkz [. İzlenecek yol: İçerik denetimlerini özel XML bölümlerine](../vsto/walkthrough-binding-content-controls-to-custom-xml-parts.md)bağlayın.

## <a name="see-also"></a>Ayrıca bkz.
- [Genişletilmiş nesneleri kullanarak Word 'Ü otomatikleştirme](../vsto/automating-word-by-using-extended-objects.md)
- [İçerik denetimleri](../vsto/content-controls.md)
- [Nasıl yapılır: Word belgelerine içerik denetimleri ekleme](../vsto/how-to-add-content-controls-to-word-documents.md)
- [Nasıl yapılır: İçerik denetimlerini kullanarak belge bölümlerini koruma](../vsto/how-to-protect-parts-of-documents-by-using-content-controls.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
