---
title: 'Nasıl yapılır: Çalışma sayfalarını program aracılığıyla yazdırma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- printing [Office development in Visual Studio], worksheets
- worksheets, printing
- print preview, worksheets
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e76b53488f1375606980e504bf94dae6343ff267
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54863428"
---
# <a name="how-to-programmatically-print-worksheets"></a>Nasıl yapılır: Çalışma sayfalarını program aracılığıyla yazdırma
  Çalışma kitabındaki yazdırabilir.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="print-a-worksheet-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesindeki bir çalışma sayfası yazdır  
  
### <a name="to-print-a-worksheet"></a>Bir çalışma sayfasını yazdırmak için  
  
1. Çağrı <xref:Microsoft.Office.Tools.Excel.Worksheet.PrintOut%2A> yöntemi `Sheet1`iki kopya isteyin ve yazdırmadan önce belgenin önizlemesini yapın.  
  
    [!code-csharp[Trin_VstcoreExcelAutomation#22](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#22)]
    [!code-vb[Trin_VstcoreExcelAutomation#22](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#22)]  
  
   <xref:Microsoft.Office.Tools.Excel.Worksheet.PrintPreview%2A> Yöntemi içinde belirtilen nesneyi görüntülemek etkinleştirir **Baskı Önizleme** penceresi. Aşağıdaki kod, sahip olduğunuzu varsayar. bir <xref:Microsoft.Office.Tools.Excel.Worksheet> konak öğesi adlı `Sheet1`.  
  
### <a name="to-preview-a-page-before-printing"></a>Bir sayfanın yazdırmadan önce önizlemesini görüntülemek için  
  
1.  Çağrı <xref:Microsoft.Office.Tools.Excel.Worksheet.PrintPreview%2A> çalışma sayfasının yöntemi.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#23](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#23)]
     [!code-vb[Trin_VstcoreExcelAutomation#23](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#23)]  
  
## <a name="print-a-worksheet-in-a-vsto-add-in"></a>Bir VSTO eklentisi, bir çalışma sayfası yazdır  
  
### <a name="to-print-a-worksheet"></a>Bir çalışma sayfasını yazdırmak için  
  
1. Çağrı <xref:Microsoft.Office.Interop.Excel._Worksheet.PrintOut%2A> yöntemi etkin çalışma sayfasının iki kopya isteyin ve yazdırmadan önce belgenin önizlemesini yapın.  
  
    [!code-csharp[Trin_VstcoreExcelAutomationAddIn#14](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#14)]
    [!code-vb[Trin_VstcoreExcelAutomationAddIn#14](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#14)]  
  
   <xref:Microsoft.Office.Interop.Excel._Worksheet.PrintPreview%2A> Yöntemi içinde belirtilen nesneyi görüntülemek etkinleştirir **Baskı Önizleme** penceresi.  
  
### <a name="to-preview-a-page-before-printing"></a>Bir sayfanın yazdırmadan önce önizlemesini görüntülemek için  
  
1.  Çağrı <xref:Microsoft.Office.Interop.Excel._Worksheet.PrintPreview%2A> etkin çalışma sayfasının yöntemi.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#15](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#15)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#15](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#15)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)   
 [Nasıl yapılır: Program aracılığıyla çalışma sayfaları Yazımı denetleme](../vsto/how-to-programmatically-check-spelling-in-worksheets.md)   
 [Çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md)   
 [Office projelerindeki nesnelere genel erişim](../vsto/global-access-to-objects-in-office-projects.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)  
