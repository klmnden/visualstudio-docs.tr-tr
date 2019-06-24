---
title: Başlangıç & karakter aralıkları program aracılığıyla bitiş
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, retrieving start and end characters
- end characters
- start characters
- documents [Office development in Visual Studio], retrieving ranges
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 8e0f04d5f70c99ea3404a95b04a7ea668a37e0f2
ms.sourcegitcommit: 7eb2fb21805d92f085126f3a820ac274f2216b4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2019
ms.locfileid: "67328944"
---
# <a name="how-to-programmatically-retrieve-start-and-end-characters-in-ranges"></a>Nasıl yapılır: Program aracılığıyla aralıkta başlangıç ve bitiş karakterlerini alma
  Bu örnek aralığının başlangıç ve bitiş konumları karakter konumlarını nasıl aldığını gösterir.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="to-retrieve-start-and-end-characters-of-a-range-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesinde aralığın başlangıç ve bitiş karakterlerini almak için

1. Değerlerini alın <xref:Microsoft.Office.Interop.Word.Range.Start%2A> ve <xref:Microsoft.Office.Interop.Word.Range.End%2A> özelliklerini <xref:Microsoft.Office.Interop.Word.Range> nesne. Aşağıdaki kod örneği, ikinci cümlenin belgedeki başlangıç ve bitiş konumları alır. Bu kod örneği kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomation#25](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#25)]
     [!code-csharp[Trin_VstcoreWordAutomation#25](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#25)]

## <a name="to-retrieve-start-and-end-characters-of-a-range-by-using-a-vsto-add-in"></a>Aralığın başlangıç ve bitiş karakterlerini bir VSTO eklentisi kullanarak almak için

1. Değerlerini alın <xref:Microsoft.Office.Interop.Word.Range.Start%2A> ve <xref:Microsoft.Office.Interop.Word.Range.End%2A> özelliklerini <xref:Microsoft.Office.Interop.Word.Range> nesne. Aşağıdaki kod örneği, etkin belgedeki ikinci cümle başlangıç ve bitiş konumu alır. Bu kod örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#25](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#25)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#25](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#25)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Program aracılığıyla tanımlama ve belgelerde aralıkları seçin](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)
- [Nasıl yapılır: Belgelerde aralıkları program aracılığıyla genişletme](../vsto/how-to-programmatically-extend-ranges-in-documents.md)
- [Nasıl yapılır: Word belgelerinde aralıkları program aracılığıyla sıfırlama](../vsto/how-to-programmatically-reset-ranges-in-word-documents.md)
- [Nasıl yapılır: Aralıkları veya seçimleri program aracılığıyla daraltma](../vsto/how-to-programmatically-collapse-ranges-or-selections-in-documents.md)
- [Nasıl yapılır: Aralık oluştururken program aracılığıyla dışlama paragraf işaretleri](../vsto/how-to-programmatically-exclude-paragraph-marks-when-creating-ranges.md)
- [Nasıl yapılır: Program aracılığıyla karakter sayma sayısı](../vsto/how-to-programmatically-count-characters-in-documents.md)
