---
title: 'Nasıl yapılır: Word belgelerine yer Işareti denetimleri ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VST.Bookmark.Dialog
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Bookmark control, adding to documents
- Create Bookmark Control dialog box
- controls [Office development in Visual Studio], adding to documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ce77736bfefdc2c2e70c489a91b147cb0d2ed74a
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255990"
---
# <a name="how-to-add-bookmark-controls-to-word-documents"></a>Nasıl yapılır: Word belgelerine yer Işareti denetimleri ekleme
  Belge düzeyi projelerde, tasarım zamanında veya çalışma zamanında <xref:Microsoft.Office.Tools.Word.Bookmark> projenizdeki belgeye denetim ekleyebilirsiniz. VSTO eklenti projelerinde, çalışma zamanında herhangi bir açık belgeye <xref:Microsoft.Office.Tools.Word.Bookmark> denetimler ekleyebilirsiniz.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

 Bu konuda aşağıdaki görevler açıklanmaktadır:

- [Tasarım zamanında Bookmark denetimleri ekleme](#designtime)

- [Belge düzeyindeki bir projede çalışma zamanında yer Işareti denetimleri ekleme](#runtimedoclevel)

- [VSTO eklenti projesindeki çalışma zamanında yer Işareti denetimleri ekleme](#runtimeaddin)

  Denetimler hakkında <xref:Microsoft.Office.Tools.Word.Bookmark> daha fazla bilgi için bkz. [Bookmark Control](../vsto/bookmark-control.md).

## <a name="designtime"></a>Tasarım zamanında Bookmark denetimleri ekleme
 Belge düzeyindeki bir projede belgeye tasarım <xref:Microsoft.Office.Tools.Word.Bookmark> zamanında denetim eklemenin birkaç yolu vardır:

- Visual Studio **araç kutusundan**.

   <xref:Microsoft.Office.Tools.Word.Bookmark> Denetimi **araç kutusundan** belgenize sürükleyebilirsiniz. Belgenize Windows Forms denetimleri eklemek için **araç kutusunu** zaten kullanıyorsanız, bu yolu tercih edebilirsiniz.

- Word içinden.

   Yerel yer işaretini ekleyeceğiniz <xref:Microsoft.Office.Tools.Word.Bookmark> şekilde belgenize denetim ekleyebilirsiniz. Bu şekilde eklemenin avantajı, denetiminizi oluşturduğunuz sırada bir kez ad olarak belirleyebilirsiniz.

- **Veri kaynakları** penceresinden.

   <xref:Microsoft.Office.Tools.Word.Bookmark> **Veri kaynakları** penceresinden denetimi belgenize sürükleyebilirsiniz. Bu, denetimi verilere aynı anda bağlamak istediğinizde yararlıdır. Konak denetimini, **veri kaynakları** penceresinden bir Windows form denetimi ekleyeceğiniz şekilde ekleyebilirsiniz. Daha fazla bilgi için bkz. [veri bağlama ve Windows Forms](/dotnet/framework/winforms/data-binding-and-windows-forms).

  [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

#### <a name="to-add-a-bookmark-control-to-a-document-from-the-toolbox"></a>Araç kutusu 'ndan bir belgeye bir yer Işareti denetimi eklemek için

1. **Araç kutusunu** açın ve **Word denetimleri** sekmesine tıklayın.

2. Belgeye bir <xref:Microsoft.Office.Tools.Word.Bookmark> denetim sürükleyin.

     **Yer Işareti Ekle** iletişim kutusu görünür.

3. Yer işaretine eklemek istediğiniz metni veya diğer öğeleri seçin.

4. **Tamam**'ı tıklatın.

     Varsayılan yer işaretinin adını korumak istemiyorsanız, adı **Özellikler** penceresinde değiştirebilirsiniz.

#### <a name="to-add-a-bookmark-control-to-a-document-in-word"></a>Word 'de belgeye bir yer Işareti denetimi eklemek için

1. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Tasarımcıda barındırılan belgede, yer işaretini eklemek istediğiniz yere yerleştirin veya yer işaretinin kapsamasını istediğiniz metni seçin.

2. Şeridin **Ekle** sekmesinde, **Bağlantılar** grubunda **yer işareti** düğmesine tıklayın.

3. **Yer işareti** iletişim kutusunda yeni yer işaretinin adını yazın ve **Ekle**' ye tıklayın.

## <a name="runtimedoclevel"></a>Belge düzeyindeki bir projede çalışma zamanında yer Işareti denetimleri ekleme
 Projenizdeki <xref:Microsoft.Office.Tools.Word.Document.Controls%2A> <xref:Microsoft.Office.Tools.Word.Bookmark> sınıf`ThisDocument` özelliğinin yöntemlerini kullanarak çalışma zamanında belgenize programlı bir şekilde denetim ekleyebilirsiniz. Aşağıdaki yollarla bir <xref:Microsoft.Office.Tools.Word.Bookmark> denetim eklemek için kullanabileceğiniz iki yöntem aşırı yüklemesi vardır:

- <xref:Microsoft.Office.Tools.Word.Bookmark> Belirtilen bir aralığa ekleyin.

- Belgedeki yerel <xref:Microsoft.Office.Tools.Word.Bookmark> bir yer işaretine (yani, a <xref:Microsoft.Office.Interop.Word.Bookmark>) dayalı bir ekleyin.

  Belge kapatıldığında <xref:Microsoft.Office.Tools.Word.Bookmark> dinamik olarak oluşturulan denetimler belgede kalıcı olmaz. Ancak, yerel <xref:Microsoft.Office.Interop.Word.Bookmark> bir belgede kalır. Belgenin bir sonraki açılışında <xref:Microsoft.Office.Tools.Word.Bookmark> yerel bir yer işaretine dayalı bir oluştur işlemi yapabilirsiniz. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

#### <a name="to-add-a-bookmark-control-to-a-document-programmatically"></a>Belgeye programlı bir Bookmark denetimi eklemek için

1. Projenizdeki olay işleyicisinde, <xref:Microsoft.Office.Tools.Word.Bookmark> denetimi belgedeki ilk paragrafa eklemek için aşağıdaki kodu ekleyin. `ThisDocument_Startup`

     [!code-csharp[Trin_VstcoreHostControlsWord#1](../vsto/codesnippet/CSharp/trin_vstcorehostcontrolsword/ThisDocument.cs#1)]
     [!code-vb[Trin_VstcoreHostControlsWord#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsWordVB/ThisDocument.vb#1)]

    > [!NOTE]
    > Varolan <xref:Microsoft.Office.Tools.Word.Bookmark> <xref:Microsoft.Office.Tools.Word.ControlCollection.AddBookmark%2A> <xref:Microsoft.Office.Interop.Word.Bookmark>bir denetimi oluşturmak istiyorsanız, yöntemini kullanın ve var olan öğesini geçirin. <xref:Microsoft.Office.Interop.Word.Bookmark>

## <a name="runtimeaddin"></a>VSTO eklenti projesindeki çalışma zamanında yer Işareti denetimleri ekleme
 VSTO eklentisini kullanarak <xref:Microsoft.Office.Tools.Word.Bookmark> çalışma zamanında herhangi bir açık belgeye program aracılığıyla denetimler ekleyebilirsiniz. Bunu yapmak için, açık bir <xref:Microsoft.Office.Tools.Word.Document> belgeyi temel alan bir konak öğesi oluşturun ve ardından bu konak öğesinin <xref:Microsoft.Office.Tools.Word.Document.Controls%2A> özelliğinin yöntemlerini kullanın. Aşağıdaki yollarla bir <xref:Microsoft.Office.Tools.Word.Bookmark> denetim eklemek için kullanabileceğiniz iki yöntem aşırı yüklemesi vardır:

- <xref:Microsoft.Office.Tools.Word.Bookmark> Belirtilen bir aralığa ekleyin.

- Belgedeki yerel <xref:Microsoft.Office.Tools.Word.Bookmark> bir yer işaretine (yani, a <xref:Microsoft.Office.Interop.Word.Bookmark>) dayalı bir ekleyin.

  Belge kapatıldığında <xref:Microsoft.Office.Tools.Word.Bookmark> dinamik olarak oluşturulan denetimler belgede kalıcı olmaz. Ancak, yerel <xref:Microsoft.Office.Interop.Word.Bookmark> bir belgede kalır. Belgenin bir sonraki açılışında <xref:Microsoft.Office.Tools.Word.Bookmark> yerel bir yer işaretine dayalı bir oluştur işlemi yapabilirsiniz. Daha fazla bilgi için bkz. [Dinamik denetimleri Office belgelerinde kalıcı hale](../vsto/persisting-dynamic-controls-in-office-documents.md)getirme.

  VSTO eklenti projelerinde konak öğeleri oluşturma hakkında daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

#### <a name="to-add-a-bookmark-control-at-a-specified-range"></a>Belirtilen aralığa bir yer Işareti denetimi eklemek için

1. Yöntemini kullanın ve öğesini eklemek <xref:Microsoft.Office.Tools.Word.Bookmark>istediğiniz <xref:Microsoft.Office.Interop.Word.Range> yere geçirin. <xref:Microsoft.Office.Tools.Word.ControlCollection.AddBookmark%2A>

     Aşağıdaki kod örneği, etkin belgenin başlangıcına <xref:Microsoft.Office.Tools.Word.Bookmark> yeni bir ekler. Bu örneği kullanmak için, `ThisAddIn_Startup` olay işleyicisindeki kodu bir Word VSTO eklenti projesinde çalıştırın.

     [!code-vb[Trin_WordAddInDynamicControls#4](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#4)]
     [!code-csharp[Trin_WordAddInDynamicControls#4](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#4)]

#### <a name="to-add-a-bookmark-control-that-is-based-on-a-native-bookmark-control"></a>Yerel bir yer Işareti denetimine dayalı bir yer Işareti denetimi eklemek için

1. Yöntemini kullanın ve yeni <xref:Microsoft.Office.Interop.Word.Bookmark> <xref:Microsoft.Office.Tools.Word.Bookmark>için temel olarak kullanmak istediğiniz varolan ' ı geçirin. <xref:Microsoft.Office.Tools.Word.ControlCollection.AddBookmark%2A>

     Aşağıdaki kod örneği, etkin belgede ilkini <xref:Microsoft.Office.Tools.Word.Bookmark> <xref:Microsoft.Office.Interop.Word.Bookmark> temel alan yeni bir oluşturur. Bu örneği kullanmak için, `ThisAddIn_Startup` olay işleyicisindeki kodu bir Word VSTO eklenti projesinde çalıştırın.

     [!code-vb[Trin_WordAddInDynamicControls#5](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#5)]
     [!code-csharp[Trin_WordAddInDynamicControls#5](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#5)]

## <a name="see-also"></a>Ayrıca bkz.
- [Genişletilmiş nesneleri kullanarak Word 'Ü otomatikleştirme](../vsto/automating-word-by-using-extended-objects.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md)
- [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md)
- [Nasıl yapılır: Yer Işareti denetimlerini yeniden boyutlandır](../vsto/how-to-resize-bookmark-controls.md)
