---
title: 'Nasıl yapılır: Belgelerde aralıkları program aracılığıyla genişletme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, extending
- documents [Office development in Visual Studio], extending ranges
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 26213477e7cec69da9171c5197371772973be5d3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62812757"
---
# <a name="how-to-programmatically-extend-ranges-in-documents"></a>Nasıl yapılır: Belgelerde aralıkları program aracılığıyla genişletme
  Tanımladıktan sonra bir <xref:Microsoft.Office.Interop.Word.Range> değiştirmeniz, başlangıç ve bitiş noktalarını kullanarak bir Microsoft Office Word belgesinde nesne <xref:Microsoft.Office.Interop.Word.Range.MoveStart%2A> ve <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> yöntemleri. <xref:Microsoft.Office.Interop.Word.Range.MoveStart%2A> Ve <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> yöntemleri aynı iki bağımsız değişkeni alır *birim* ve *sayısı*. *Sayısı* değişkendir taşımak için birim sayısını ve *birim* bağımsız değişkeni, aşağıdakilerden biri olabilir <xref:Microsoft.Office.Interop.Word.WdUnits> değerleri:

- <xref:Microsoft.Office.Interop.Word.WdUnits.wdCharacter>

- <xref:Microsoft.Office.Interop.Word.WdUnits.wdWord>

- <xref:Microsoft.Office.Interop.Word.WdUnits.wdSentence>

- <xref:Microsoft.Office.Interop.Word.WdUnits.wdParagraph>

- <xref:Microsoft.Office.Interop.Word.WdUnits.wdSection>

- <xref:Microsoft.Office.Interop.Word.WdUnits.wdStory>

- <xref:Microsoft.Office.Interop.Word.WdUnits.wdCell>

- <xref:Microsoft.Office.Interop.Word.WdUnits.wdColumn>

- <xref:Microsoft.Office.Interop.Word.WdUnits.wdRow>

- <xref:Microsoft.Office.Interop.Word.WdUnits.wdTable>

  [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

  Aşağıdaki örnek, bir yedi karakter aralığı tanımlar. Özgün konum başlattığınızda ardından yedi aralığın karakter başlangıç konumunu taşır. Aralığın bitiş konumu da yedi karakterini başlangıç konumundan sonra olduğundan, sonuç sıfır karakterden oluşan bir aralıktır. Kod, ardından geçerli bitiş konumu sonra bitiş konumu yedi karakterini taşır.

## <a name="to-extend-a-range"></a>Bir aralığı genişletmek için

1. Karakter aralığı tanımlayın. Daha fazla bilgi için [nasıl yapılır: Program aracılığıyla tanımlama ve belgelerde aralıkları seçin](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md).

     Aşağıdaki kod örneği belge düzeyi özelleştirmesinde kullanılabilir.

     [!code-vb[Trin_VstcoreWordAutomation#39](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#39)]
     [!code-csharp[Trin_VstcoreWordAutomation#39](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#39)]

     Aşağıdaki kod örneği, VSTO eklentisi içinde kullanılabilir. Bu örnek etkin belgeyi kullanır.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#39](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#39)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#39](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#39)]

2. Kullanım <xref:Microsoft.Office.Interop.Word.Range.MoveStart%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Range> aralığın başlangıç konumunu taşımak için nesne.

     [!code-vb[Trin_VstcoreWordAutomation#40](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#40)]
     [!code-csharp[Trin_VstcoreWordAutomation#40](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#40)]

3. Kullanım <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Range> aralığın bitiş konumu taşımak için nesne.

     [!code-vb[Trin_VstcoreWordAutomation#41](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#41)]
     [!code-csharp[Trin_VstcoreWordAutomation#41](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#41)]

## <a name="document-level-customization-code"></a>Belge düzeyi özelleştirmesi kod

### <a name="to-extend-a-range-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesindeki bir aralığı genişletmek için

1. Aşağıdaki örnek, bir belge düzeyi özelleştirmesi için tam kod gösterilir. Bu kodu kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomation#38](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#38)]
     [!code-csharp[Trin_VstcoreWordAutomation#38](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#38)]

## <a name="vsto-add-in-code"></a>VSTO eklenti kodu

### <a name="to-extend-a-range-in-an-application-level-vsto-add-in"></a>Bir uygulama düzeyinde VSTO eklentisi bir aralıktaki genişletmek için

1. Aşağıdaki örnek, VSTO eklentisi için tam kod gösterilmektedir. Bu kodu kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#38](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#38)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#38](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#38)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Word belgelerinde aralıkları program aracılığıyla sıfırlama](../vsto/how-to-programmatically-reset-ranges-in-word-documents.md)
- [Nasıl yapılır: Aralıkları veya seçimleri program aracılığıyla daraltma](../vsto/how-to-programmatically-collapse-ranges-or-selections-in-documents.md)
- [Nasıl yapılır: Program aracılığıyla tanımlama ve belgelerde aralıkları seçin](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)
- [Nasıl yapılır: Program aracılığıyla aralıkta başlangıç ve bitiş karakterlerini alma](../vsto/how-to-programmatically-retrieve-start-and-end-characters-in-ranges.md)
- [Nasıl yapılır: Aralık oluştururken program aracılığıyla dışlama paragraf işaretleri](../vsto/how-to-programmatically-exclude-paragraph-marks-when-creating-ranges.md)
