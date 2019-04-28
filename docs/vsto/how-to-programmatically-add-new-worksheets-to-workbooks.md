---
title: 'Nasıl yapılır: Program aracılığıyla çalışma kitapları için yeni çalışma sayfaları ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, adding worksheets
- workbooks, creating worksheets
- worksheets, creating
- worksheets, adding to workbooks
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e1b45196fa70328809aa5da3a1f56ea57fce2085
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62967650"
---
# <a name="how-to-programmatically-add-new-worksheets-to-workbooks"></a>Nasıl yapılır: Program aracılığıyla çalışma kitapları için yeni çalışma sayfaları ekleme
  Program aracılığıyla çalışma sayfası oluşturmak ve ardından çalışma kitabındaki koleksiyonu çalışma sayfası ekleyin.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="to-add-a-new-worksheet-to-a-workbook-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesindeki bir çalışma kitabına yeni bir çalışma sayfası eklemek için

1. Kullanım <xref:Microsoft.Office.Interop.Excel.Worksheets.Add%2A> yöntemi <xref:Microsoft.Office.Interop.Excel.Sheets> koleksiyonu.

     [!code-csharp[Trin_VstcoreExcelAutomation#15](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#15)]
     [!code-vb[Trin_VstcoreExcelAutomation#15](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#15)]

     Yeni çalışma sayfası olan bir yerel <xref:Microsoft.Office.Interop.Excel.Worksheet> nesnesi ve bir ana bilgisayar öğesi. Eklemek istiyorsanız bir <xref:Microsoft.Office.Tools.Excel.Worksheet> konak öğesi, çalışma zamanında eklemeniz gerekir.

## <a name="to-add-a-new-worksheet-to-a-workbook-in-a-vsto-add-in"></a>Bir VSTO eklentisi kitabında yeni bir çalışma sayfası eklemek için

1. Kullanım <xref:Microsoft.Office.Interop.Excel.Worksheets.Add%2A> yöntemi <xref:Microsoft.Office.Interop.Excel.Sheets> koleksiyonu.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#11](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#11)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#11](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#11)]

     Yeni çalışma sayfası olan bir yerel <xref:Microsoft.Office.Interop.Excel.Worksheet> nesnesi ve bir ana bilgisayar öğesi. Ayrıca oluşturabileceğiniz bir <xref:Microsoft.Office.Tools.Excel.Worksheet> yerel konak öğesi <xref:Microsoft.Office.Interop.Excel.Worksheet> nesne. Daha fazla bilgi için [genişletme Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında VSTO Add-Ins](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Nasıl yapılır: Program aracılığıyla çalışma kitaplarından çalışma sayfaları silme](../vsto/how-to-programmatically-delete-worksheets-from-workbooks.md)
- [Nasıl yapılır: Program aracılığıyla çalışma sayfaları seçme](../vsto/how-to-programmatically-select-worksheets.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Office projelerindeki nesnelere genel erişim](../vsto/global-access-to-objects-in-office-projects.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
