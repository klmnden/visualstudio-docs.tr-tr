---
title: 'Nasıl yapılır: Yer Işareti denetimlerini yeniden boyutlandır'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- controls [Office development in Visual Studio], resizing
- Bookmark control, resizing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 99e5c789f65a1dff460bc22dd4a0c097e11c7e98
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71252213"
---
# <a name="how-to-resize-bookmark-controls"></a>Nasıl yapılır: Yer Işareti denetimlerini yeniden boyutlandır
  Bir <xref:Microsoft.Office.Tools.Word.Bookmark> denetimin boyutunu Microsoft Office bir Word belgesine eklediğinizde ayarlarsınız. Ayrıca, daha sonra yeniden boyutlandırabilirsiniz.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

 Bir yer işaretini yeniden boyutlandırmanın üç yolu vardır:

- <xref:Microsoft.Office.Tools.Word.Bookmark> Denetimdeki metni ekleyin veya kaldırın.

   Bir yer işaretine metin eklediğinizde, yer işaretinin boyutu otomatik olarak yeni metni içerecek şekilde artar. Metni sildiğinizde, yer işaretinin boyutu otomatik olarak azalır.

- <xref:Microsoft.Office.Tools.Word.Bookmark.Start%2A> <xref:Microsoft.Office.Tools.Word.Bookmark.End%2A> Denetimin ve<xref:Microsoft.Office.Tools.Word.Bookmark> özelliklerini değiştirin.

   Bu, boyutu yalnızca birkaç karakterle değiştiriyorsanız yararlı olur.

- <xref:Microsoft.Office.Tools.Word.Bookmark> Denetimi yeniden oluşturun.

   Bu, bir yer işaretinin boyutunun veya konumunun önemli bir değişikliği varsa yararlıdır.

  Belge düzeyi projelerde, tasarım zamanında veya çalışma zamanında <xref:Microsoft.Office.Tools.Word.Bookmark> projenizdeki belgeye denetim ekleyebilirsiniz. VSTO eklenti projelerinde, çalışma zamanında herhangi bir açık belgeye <xref:Microsoft.Office.Tools.Word.Bookmark> denetimler ekleyebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Word belgelerine](../vsto/how-to-add-bookmark-controls-to-word-documents.md)Bookmark denetimleri ekleyin.

  [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

## <a name="change-the-start-and-end-properties"></a>Başlangıç ve bitiş özelliklerini değiştirme

### <a name="to-resize-a-bookmark-in-a-document-level-project-at-design-time"></a>Tasarım zamanında belge düzeyindeki bir projede yer işaretini yeniden boyutlandırmak için

1. **Özellikler** penceresinde yer işaretini seçin.

2. <xref:Microsoft.Office.Tools.Word.Bookmark.Start%2A> Özelliğin değerini artırın veya azaltın.

3. <xref:Microsoft.Office.Tools.Word.Bookmark.End%2A> Özelliğin değerini artırın veya azaltın.

### <a name="to-resize-a-bookmark-in-a-document-level-project-at-run-time"></a>Çalışma zamanında belge düzeyindeki bir projede yer işaretini yeniden boyutlandırmak için

1. Çalışma zamanında veya <xref:Microsoft.Office.Tools.Word.Bookmark.End%2A> tasarım zamanında oluşturduğunuz <xref:Microsoft.Office.Tools.Word.Bookmark> bir öğesinin veözelliklerinideğiştirin.<xref:Microsoft.Office.Tools.Word.Bookmark.Start%2A>

     Aşağıdaki kod örneği, adlı `SampleBookmark`bir yer işaretinin başlangıcına beş karakter ekler. Bu kod, yer işaretinin önünde en az beş karakterlik metin olduğunu varsayar.

     [!code-csharp[Trin_VstcoreHostControlsWord#2](../vsto/codesnippet/CSharp/trin_vstcorehostcontrolsword/ThisDocument.cs#2)]
     [!code-vb[Trin_VstcoreHostControlsWord#2](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsWordVB/ThisDocument.vb#2)]

     Aşağıdaki kod örneği, aynı yer işaretinin sonuna beş karakter ekler. Bu kod, yer işaretinden sonra en az beş karakterlik metin olduğunu varsayar.

     [!code-csharp[Trin_VstcoreHostControlsWord#3](../vsto/codesnippet/CSharp/trin_vstcorehostcontrolsword/ThisDocument.cs#3)]
     [!code-vb[Trin_VstcoreHostControlsWord#3](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsWordVB/ThisDocument.vb#3)]

### <a name="to-resize-a-bookmark-in-a-vsto-add-in-project-at-run-time"></a>Çalışma zamanında VSTO eklenti projesindeki bir yer işaretini yeniden boyutlandırmak için

1. Çalışma zamanında oluşturduğunuz <xref:Microsoft.Office.Tools.Word.Bookmark.End%2A> bir <xref:Microsoft.Office.Tools.Word.Bookmark> öğesinin ve özelliklerini değiştirin. <xref:Microsoft.Office.Tools.Word.Bookmark.Start%2A>

     Aşağıdaki kod örneği, etkin belgenin <xref:Microsoft.Office.Tools.Word.Bookmark> ilk paragrafında bulunan metni içeren bir oluşturur ve sonra başından ve sonundan <xref:Microsoft.Office.Tools.Word.Bookmark>beş karakteri kaldırır.

     [!code-vb[Trin_WordAddInDynamicControls#16](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#16)]
     [!code-csharp[Trin_WordAddInDynamicControls#16](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#16)]

## <a name="recreate-the-bookmark"></a>Yer işaretini yeniden oluşturma
 Varolan yer işaretiyle aynı ada sahip olan ancak farklı boyutta olan yeni bir yer işareti ekleyerek belge düzeyindeki bir projedeki yer işaretini yeniden boyutlandırabilirsiniz.

### <a name="to-recreate-a-bookmark-in-a-document-level-project-at-design-time"></a>Tasarım zamanında belge düzeyindeki bir projede yer işaretini yeniden oluşturmak için

1. Yeni <xref:Microsoft.Office.Tools.Word.Bookmark> denetime dahil edilecek metni seçin.

2. **Ekle** menüsünde **yer işareti**' ne tıklayın.

3. **Yer işareti** iletişim kutusunda, yeniden boyutlandırmak istediğiniz yer işaretinin adını seçin ve **Ekle**' ye tıklayın.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Word belgelerine yer Işareti denetimleri ekleme](../vsto/how-to-add-bookmark-controls-to-word-documents.md)
- [Genişletilmiş nesneleri kullanarak Word 'Ü otomatikleştirme](../vsto/automating-word-by-using-extended-objects.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Nasıl yapılır: NamedRange denetimlerini yeniden boyutlandır](../vsto/how-to-resize-namedrange-controls.md)
- [Nasıl yapılır: ListObject denetimlerini yeniden boyutlandır](../vsto/how-to-resize-listobject-controls.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
