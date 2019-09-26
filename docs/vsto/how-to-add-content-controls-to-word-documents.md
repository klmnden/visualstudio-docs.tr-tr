---
title: 'Nasıl yapılır: Word belgelerine Içerik denetimleri ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- restricted permissions [Office development in Visual Studio]
- DropDownListContentControl, adding to documents
- BuildingBlockGalleryContentControl, adding to documents
- partial document protection [Office development in Visual Studio]
- RichTextContentControl, adding to documents
- Word [Office development in Visual Studio], partial document protection
- content controls [Office development in Visual Studio], protecting
- PictureContentControl, adding to documents
- GroupContentControl, adding to documents
- document protection [Office development in Visual Studio]
- PlainTextContentControl, adding to documents
- content controls [Office development in Visual Studio], adding
- ComboBoxContentControl, adding to documents
- DatePickerContentControl, adding to documents
- Word [Office development in Visual Studio], restricted permissions
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 2c84ae02bd2cafde7b6232c73bc75f0976e81bd0
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71254360"
---
# <a name="how-to-add-content-controls-to-word-documents"></a>Nasıl yapılır: Word belgelerine Içerik denetimleri ekleme
  Belge düzeyi Word projelerinde, tasarım zamanında veya çalışma zamanında projenizdeki belgeye içerik denetimleri ekleyebilirsiniz. Word VSTO eklenti projelerinde, çalışma zamanında herhangi bir açık belgeye içerik denetimleri ekleyebilirsiniz.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

 Bu konuda aşağıdaki görevler açıklanmaktadır:

- [Tasarım zamanında içerik denetimleri ekleme](#designtime)

- [Belge düzeyindeki bir projede çalışma zamanında içerik denetimleri ekleme](#runtimedoclevel)

- [VSTO eklenti projesindeki çalışma zamanında içerik denetimleri ekleme](#runtimeaddin)

  İçerik denetimleri hakkında daha fazla bilgi için bkz. [içerik denetimleri](../vsto/content-controls.md).

## <a name="designtime"></a>Tasarım zamanında Içerik denetimleri ekleme
 Belge düzeyindeki bir projede belgeye tasarım zamanında içerik denetimleri eklemenin birkaç yolu vardır:

- **Araç kutusunun** **Word denetimleri** sekmesinden bir içerik denetimi ekleyin.

- Word 'de yerel içerik denetimi ekleyeceğiniz şekilde belgenize bir içerik denetimi ekleyin.

- **Veri kaynakları** penceresinden bir içerik denetimini belgenize sürükleyin. Bu, Denetim oluşturulduğunda denetimi verilere bağlamak istediğinizde yararlıdır. Daha fazla bilgi için [nasıl yapılır: Belgeleri nesnelerdeki](../vsto/how-to-populate-documents-with-data-from-objects.md) verilerle doldurun ve [şunları yapın: Belgeleri bir veritabanındaki](../vsto/how-to-populate-documents-with-data-from-a-database.md)verilerle doldurun.

  [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

### <a name="to-add-a-content-control-to-a-document-by-using-the-toolbox"></a>Araç kutusunu kullanarak bir belgeye içerik denetimi eklemek için

1. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Tasarımcıda barındırılan belgede, içerik denetimini eklemek istediğiniz yere imleci koyun veya içerik denetiminin değiştirilmesini istediğiniz metni seçin.

2. **Araç kutusunu** açın ve **Word denetimleri** sekmesine tıklayın.

3. Denetimi aşağıdaki yollarla ekleyin:

    - **Araç kutusunda**bir içerik denetimine çift tıklayın.

         veya

    - **Araç kutusunda** bir içerik denetimine tıklayın ve ardından **ENTER** tuşuna basın.

         veya

    - **Araç kutusundan** bir içerik denetimini belgeye sürükleyin. İçerik denetimi, fare işaretçisinin konumunda değil belgedeki geçerli seçime eklenir.

> [!NOTE]
> **Araç kutusunu**kullanarak bir <xref:Microsoft.Office.Tools.Word.GroupContentControl> ekleyemezsiniz. Yalnızca bir <xref:Microsoft.Office.Tools.Word.GroupContentControl> kelime veya çalışma zamanında ekleyebilirsiniz.

> [!NOTE]
> Visual Studio, araç kutusunda onay kutusu içerik denetimi sağlamaz. Belgeye bir onay kutusu içerik denetimi eklemek için program aracılığıyla bir <xref:Microsoft.Office.Tools.Word.ContentControl> nesne oluşturmanız gerekir. Daha fazla bilgi için bkz. [içerik denetimleri](../vsto/content-controls.md).

#### <a name="to-add-a-content-control-to-a-document-in-word"></a>Word 'de belgeye içerik denetimi eklemek için

1. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Tasarımcıda barındırılan belgede, içerik denetimini eklemek istediğiniz yere imleci koyun veya içerik denetiminin değiştirilmesini istediğiniz metni seçin.

2. Şeritte **Geliştirici** sekmesine tıklayın.

    > [!NOTE]
    > **Geliştirici** sekmesi görünür değilse, önce onu göstermelisiniz. Daha fazla bilgi için [nasıl yapılır: Şeritte](../vsto/how-to-show-the-developer-tab-on-the-ribbon.md)Geliştirici sekmesini görüntüleyin.

3. **Denetimler** grubunda, eklemek istediğiniz içerik denetimi simgesine tıklayın.

## <a name="runtimedoclevel"></a>Belge düzeyindeki bir projede çalışma zamanında içerik denetimleri ekleme
 Projenizdeki <xref:Microsoft.Office.Tools.Word.Document.Controls%2A> `ThisDocument` sınıf özelliğinin yöntemlerini kullanarak çalışma zamanında belgenize programlı bir şekilde içerik denetimleri ekleyebilirsiniz. Her yöntemin, aşağıdaki yollarla bir içerik denetimi eklemek için kullanabileceğiniz üç aşırı yüklemesi vardır:

- Geçerli seçime bir denetim ekleyin.

- Belirtilen aralığa bir denetim ekleyin.

- Belgedeki yerel içerik denetimini temel alan bir denetim ekleyin.

  Belge kapatıldığında dinamik olarak oluşturulan içerik denetimleri belgede kalıcı olmaz. Ancak, yerel içerik denetimi belgede kalır. Belgenin bir sonraki açılışında yerel içerik denetimine dayalı bir içerik denetimini yeniden oluşturabilirsiniz. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

> [!NOTE]
> Word 2010 projesindeki bir belgeye onay kutusu içerik denetimi eklemek için bir <xref:Microsoft.Office.Tools.Word.ContentControl> nesnesi oluşturmanız gerekir. Daha fazla bilgi için bkz. [içerik denetimleri](../vsto/content-controls.md).

### <a name="to-add-a-content-control-at-the-current-selection"></a>Geçerli seçime bir içerik denetimi eklemek için

1. Ad <xref:Microsoft.Office.Tools.Word.ControlCollection> <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A>denetim sınıfına sahip bir yöntemi kullanın > (denetim sınıfı, eklemek istediğiniz içerik denetiminin sınıf adı, gibi) ve için tek bir parametreye sahip `Add` \< Yeni denetimin adı.

     Aşağıdaki kod örneği, belgenin başlangıcına <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A> yeni <xref:Microsoft.Office.Tools.Word.RichTextContentControl> bir eklemek için yöntemini kullanır. Bu kodu çalıştırmak için projenizdeki `ThisDocument` sınıfa kodu ekleyin ve `ThisDocument_Startup` olay işleyicisinden `AddRichTextControlAtSelection` yöntemi çağırın.

     [!code-csharp[Trin_ContentControlReference#700](../vsto/codesnippet/CSharp/trin_wordcontentcontrolreference/RichText.cs#700)]
     [!code-vb[Trin_ContentControlReference#700](../vsto/codesnippet/VisualBasic/trin_contentcontrolreference/RichText.vb#700)]

### <a name="to-add-a-content-control-at-a-specified-range"></a>Belirli bir aralığa içerik denetimi eklemek için

1. <xref:Microsoft.Office.Tools.Word.ControlCollection> Ad <xref:Microsoft.Office.Interop.Word.Range> <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A>denetim sınıfına sahip bir yöntemi kullanın > (denetim sınıfı, eklemek istediğiniz içerik denetimi sınıfının adı, gibi) ve `Add` \< parametresinin.

     Aşağıdaki kod örneği, belgenin başlangıcına <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A> yeni <xref:Microsoft.Office.Tools.Word.RichTextContentControl> bir eklemek için yöntemini kullanır. Bu kodu çalıştırmak için projenizdeki `ThisDocument` sınıfa kodu ekleyin ve `ThisDocument_Startup` olay işleyicisinden `AddRichTextControlAtRange` yöntemi çağırın.

     [!code-csharp[Trin_ContentControlReference#701](../vsto/codesnippet/CSharp/trin_wordcontentcontrolreference/RichText.cs#701)]
     [!code-vb[Trin_ContentControlReference#701](../vsto/codesnippet/VisualBasic/trin_contentcontrolreference/RichText.vb#701)]

### <a name="to-add-a-content-control-that-is-based-on-a-native-content-control"></a>Yerel içerik denetimini temel alan bir içerik denetimi eklemek için

1. <xref:Microsoft.Office.Tools.Word.ControlCollection> Ad `Microsoft.Office.Interop.Word.ContentControl` <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A>denetim sınıfına sahip bir yöntemi kullanın > (denetim sınıfı, eklemek istediğiniz içerik denetimi sınıfının adı, gibi) ve `Add` \< parametresinin.

     Aşağıdaki kod örneği, belgesinde bulunan <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A> her yerel zengin metin denetimine <xref:Microsoft.Office.Tools.Word.RichTextContentControl> yeni bir oluşturmak için yöntemini kullanır. Bu kodu çalıştırmak için projenizdeki `ThisDocument` sınıfa kodu ekleyin ve `ThisDocument_Startup` olay işleyicisinden `CreateRichTextControlsFromNativeControls` yöntemi çağırın.

     [!code-csharp[Trin_ContentControlReference#702](../vsto/codesnippet/CSharp/trin_wordcontentcontrolreference/RichText.cs#702)]
     [!code-vb[Trin_ContentControlReference#702](../vsto/codesnippet/VisualBasic/trin_contentcontrolreference/RichText.vb#702)]

## <a name="runtimeaddin"></a>VSTO eklenti projesindeki çalışma zamanında içerik denetimleri ekleme
 Bir VSTO eklentisi kullanarak çalışma zamanında herhangi bir açık belgeye programlama yoluyla içerik denetimleri ekleyebilirsiniz. Bunu yapmak için, açık bir <xref:Microsoft.Office.Tools.Word.Document> belgeyi temel alan bir konak öğesi oluşturun ve ardından bu konak öğesinin <xref:Microsoft.Office.Tools.Word.Document.Controls%2A> özelliğinin yöntemlerini kullanın. Her yöntemin, aşağıdaki yollarla bir içerik denetimi eklemek için kullanabileceğiniz üç aşırı yüklemesi vardır:

- Geçerli seçime bir denetim ekleyin.

- Belirtilen aralığa bir denetim ekleyin.

- Belgedeki yerel içerik denetimini temel alan bir denetim ekleyin.

  Belge kapatıldığında dinamik olarak oluşturulan içerik denetimleri belgede kalıcı olmaz. Ancak, yerel içerik denetimi belgede kalır. Belgenin bir sonraki açılışında yerel içerik denetimine dayalı bir içerik denetimini yeniden oluşturabilirsiniz. Daha fazla bilgi için bkz. [Dinamik denetimleri Office belgelerinde kalıcı hale](../vsto/persisting-dynamic-controls-in-office-documents.md)getirme.

  VSTO eklenti projelerinde konak öğeleri oluşturma hakkında daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

> [!NOTE]
> Bir belgeye onay kutusu içerik denetimi eklemek için bir <xref:Microsoft.Office.Tools.Word.ContentControl> nesnesi oluşturmanız gerekir. Daha fazla bilgi için bkz. [içerik denetimleri](../vsto/content-controls.md).

### <a name="to-add-a-content-control-at-the-current-selection"></a>Geçerli seçime bir içerik denetimi eklemek için

1. Ad <xref:Microsoft.Office.Tools.Word.ControlCollection> <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A>denetim sınıfına sahip bir yöntemi kullanın > (denetim sınıfı, eklemek istediğiniz içerik denetiminin sınıf adı, gibi) ve için tek bir parametreye sahip `Add` \< Yeni denetimin adı.

     Aşağıdaki kod örneği, etkin belgenin <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A> başlangıcına yeni <xref:Microsoft.Office.Tools.Word.RichTextContentControl> bir eklemek için yöntemini kullanır. Bu kodu çalıştırmak için projenizdeki `ThisAddIn` sınıfa kodu ekleyin ve `ThisAddIn_Startup` olay işleyicisinden `AddRichTextControlAtSelection` yöntemi çağırın.

     [!code-vb[Trin_WordAddInDynamicControls#1](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#1)]
     [!code-csharp[Trin_WordAddInDynamicControls#1](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#1)]

### <a name="to-add-a-content-control-at-a-specified-range"></a>Belirli bir aralığa içerik denetimi eklemek için

1. <xref:Microsoft.Office.Tools.Word.ControlCollection> Ad <xref:Microsoft.Office.Interop.Word.Range> <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A>denetim sınıfına sahip bir yöntemi kullanın > (denetim sınıfı, eklemek istediğiniz içerik denetimi sınıfının adı, gibi) ve `Add` \< parametresinin.

     Aşağıdaki kod örneği, etkin belgenin <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A> başlangıcına yeni <xref:Microsoft.Office.Tools.Word.RichTextContentControl> bir eklemek için yöntemini kullanır. Bu kodu çalıştırmak için projenizdeki `ThisAddIn` sınıfa kodu ekleyin ve `ThisAddIn_Startup` olay işleyicisinden `AddRichTextControlAtRange` yöntemi çağırın.

     [!code-vb[Trin_WordAddInDynamicControls#2](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#2)]
     [!code-csharp[Trin_WordAddInDynamicControls#2](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#2)]

#### <a name="to-add-a-content-control-that-is-based-on-a-native-content-control"></a>Yerel içerik denetimini temel alan bir içerik denetimi eklemek için

1. <xref:Microsoft.Office.Tools.Word.ControlCollection> Ad `Microsoft.Office.Interop.Word.ContentControl` <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A>denetim sınıfına sahip bir yöntemi kullanın > (denetim sınıfı, eklemek istediğiniz içerik denetimi sınıfının adı, gibi) ve `Add` \< parametresinin.

     Aşağıdaki kod örneği, belge açıldıktan <xref:Microsoft.Office.Tools.Word.ControlCollection.AddRichTextContentControl%2A> sonra bir belgedeki her yerel <xref:Microsoft.Office.Tools.Word.RichTextContentControl> zengin metin denetimine yeni bir oluşturmak için yöntemini kullanır. Bu kodu çalıştırmak için projenizdeki `ThisAddIn` sınıfa kodu ekleyin.

     [!code-vb[Trin_WordAddInDynamicControls#3](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#3)]
     [!code-csharp[Trin_WordAddInDynamicControls#3](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#3)]

     İçin C#olay işleyicisini `Application_DocumentOpen` <xref:Microsoft.Office.Interop.Word.ApplicationEvents4_Event.DocumentOpen> olaya de eklemeniz gerekir.

     [!code-csharp[Trin_WordAddInDynamicControls#6](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#6)]

## <a name="see-also"></a>Ayrıca bkz.
- [Genişletilmiş nesneleri kullanarak Word 'Ü otomatikleştirme](../vsto/automating-word-by-using-extended-objects.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md)
- [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md)
