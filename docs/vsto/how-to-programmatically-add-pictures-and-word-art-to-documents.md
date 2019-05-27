---
title: Belgelere program aracılığıyla resim ve Word Art ekleme
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], adding pictures
- Word documents, adding pictures
- Word documents, adding Word Art
- graphics, adding to Word documents
- WordArt, adding to documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 63b1a72a5b332f27b6bd38d25c16ff3a5981b4fa
ms.sourcegitcommit: 13ab9a5ab039b070b9cd9251d0b83dd216477203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2019
ms.locfileid: "66177758"
---
# <a name="how-to-programmatically-add-pictures-and-word-art-to-documents"></a>Nasıl yapılır: Belgelere program aracılığıyla resim ve Word Art ekleme
  Tasarım zamanında veya çalışma zamanı sırasında belgelere resimler ve çizim nesneleri ekleyebilirsiniz. WordArt Microsoft Office Word belgelerine dekoratif metin eklemenize olanak tanır. Bu özel yazı efektleri çizim özelleştirebilir ve belgenize eklemek nesneleridir.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="add-a-picture-at-design-time"></a>Tasarım zamanında bir Resim Ekle
 Belge düzeyinde özelleştirme geliştiriyorsanız tasarım zamanında belgeye bir resim ekleyebilirsiniz.

### <a name="to-add-a-picture-to-a-word-document-at-design-time"></a>Tasarım zamanında bir Word belgesi için resim eklemek için

1. İmlecinizi, belgede resim eklemek istediğiniz konuma yerleştirin.

2. Tıklayın **Ekle** Şerit sekmesi.

3. İçinde **çizimler** grubunda **resim**.

4. İçinde **resim** iletişim kutusunda, eklemek istediğiniz resme gidin ve tıklayın **Ekle**.

     Resim geçerli imleç konumundan belgenize eklenir.

## <a name="add-a-picture-at-runtime"></a>Çalışma zamanında bir Resim Ekle
 Geçerli imleç konumundan belgeye bir resim ekleyebilirsiniz.

### <a name="to-add-a-picture-at-the-cursor-location"></a>İmleç konumuna resim eklemek için

1. Çağrı <xref:Microsoft.Office.Interop.Word.InlineShapes.AddPicture%2A> yöntemi <xref:Microsoft.Office.Interop.Word.InlineShapes> toplama ve dosya oluşturdular.

     [!code-vb[Trin_VstcoreWordAutomation#108](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#108)]
     [!code-csharp[Trin_VstcoreWordAutomation#108](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#108)]

## <a name="add-wordart-at-design-time"></a>Tasarım zamanında WordArt ekleme
 Belge düzeyinde özelleştirme geliştiriyorsanız, tasarım zamanında belgeye WordArt ekleyebilirsiniz.

### <a name="to-add-wordart-to-a-word-document-at-design-time"></a>Tasarım zamanında bir Word belgesi için WordArt eklemek için

1. İmlecinizi WordArt belgede eklemek istediğiniz yere yerleştirin.

2. Tıklayın **Ekle** Şerit sekmesi.

3. İçinde **metin** grubunda **WordArt**ve ardından WordArt stili seçin.

4. Belgeye görünmesini istediğiniz metni Ekle **WordArt Metni Düzenle** iletişim kutusu ve tıklatın **Tamam**.

     Metin Seçili WordArt stil uygulanmış belgenize eklenir.

## <a name="add-wordart-at-runtime"></a>Çalışma zamanında WordArt ekleme
 Geçerli imleç konumundan belgeye WordArt ekleyebilirsiniz. Belge düzeyi özelleştirmeleri ve VSTO eklentileri için farklı bir yordamdır.

### <a name="to-add-wordart-at-the-cursor-location-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesinde İmleç konumuna WordArt eklemek için

1. Geçerli imleç konumu sol ve üst konumunu alır.

     [!code-vb[Trin_VstcoreWordAutomation#109](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#109)]
     [!code-csharp[Trin_VstcoreWordAutomation#109](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#109)]

2. Çağrı <xref:Microsoft.Office.Interop.Word.Shapes.AddTextEffect%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Shapes> belge nesnesi.

     [!code-vb[Trin_VstcoreWordAutomation#110](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#110)]
     [!code-csharp[Trin_VstcoreWordAutomation#110](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#110)]

### <a name="to-add-wordart-at-the-cursor-location-in-a-vsto-add-in"></a>Bir VSTO eklentisi imleç konumu WordArt eklemek için

1. Geçerli imleç konumu sol ve üst konumunu alır.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#109](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#109)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#109](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#109)]

2. Çağrı <xref:Microsoft.Office.Interop.Word.Shapes.AddTextEffect%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Shapes> nesne etkin belge (veya belirttiğiniz başka bir belge).

     [!code-vb[Trin_VstcoreWordAutomationAddIn#110](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#110)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#110](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#110)]

## <a name="compile-the-code"></a>Kod derleme

- Adlı bir resim *SamplePicture.jpg* c sürücüsünde bulunan mevcut olması gerekir

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Varolan belgeleri program aracılığıyla açma](../vsto/how-to-programmatically-open-existing-documents.md)
- [Nasıl yapılır: Word belgelerine program aracılığıyla metin ekleme](../vsto/how-to-programmatically-insert-text-into-word-documents.md)
- [Nasıl yapılır: Program aracılığıyla aramalardan sonra seçimleri geri yükleme](../vsto/how-to-programmatically-restore-selections-after-searches.md)
- [Nasıl yapılır: Program aracılığıyla belgeleri kaydetme](../vsto/how-to-programmatically-save-documents.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
