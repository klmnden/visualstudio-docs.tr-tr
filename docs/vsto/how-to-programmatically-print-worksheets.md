---
title: 'Nasıl yapılır: Program aracılığıyla yazdırma çalışma sayfaları'
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
ms.openlocfilehash: 764723d0749cd82739d8e67ee71104f41a0f9065
ms.sourcegitcommit: 5b34052a1c7d86179d7898ed532babb2d9dad4a3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2019
ms.locfileid: "69490589"
---
# <a name="how-to-programmatically-print-worksheets"></a>Nasıl yapılır: Program aracılığıyla yazdırma çalışma sayfaları

Çalışma kitabındaki tüm çalışma sayfalarını yazdırabilirsiniz.

[!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="print-a-worksheet-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesindeki çalışma sayfasını yazdırma

### <a name="to-print-a-worksheet"></a>Çalışma sayfası yazdırmak için

1. `PrintOut` Yönteminiçağırın,ikikopyaisteyinve`Sheet1`yazdırmadan önce belgeyi önizleyin.

    [!code-csharp[Trin_VstcoreExcelAutomation#22](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#22)]
    [!code-vb[Trin_VstcoreExcelAutomation#22](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#22)]

   Yöntemi <xref:Microsoft.Office.Tools.Excel.Worksheet.PrintPreview%2A> , belirtilen nesneyi **Baskı Önizleme** penceresinde görüntülemenizi sağlar. Aşağıdaki kod, adlı <xref:Microsoft.Office.Tools.Excel.Worksheet> `Sheet1`bir konak öğesine sahip olduğunuzu varsayar.

### <a name="to-preview-a-page-before-printing"></a>Yazdırmadan önce bir sayfayı önizlemek için

1. Çalışma sayfasının <xref:Microsoft.Office.Tools.Excel.Worksheet.PrintPreview%2A> yöntemini çağırın.

     [!code-csharp[Trin_VstcoreExcelAutomation#23](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#23)]
     [!code-vb[Trin_VstcoreExcelAutomation#23](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#23)]

## <a name="print-a-worksheet-in-a-vsto-add-in"></a>Bir VSTO eklentisinin çalışma sayfasını yazdırma

### <a name="to-print-a-worksheet"></a>Çalışma sayfası yazdırmak için

1. Etkin çalışma sayfasının yöntemini çağırın, iki kopya isteyin ve yazdırmadan önce belgeyi önizleyin. <xref:Microsoft.Office.Interop.Excel._Worksheet.PrintOut%2A>

    [!code-csharp[Trin_VstcoreExcelAutomationAddIn#14](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#14)]
    [!code-vb[Trin_VstcoreExcelAutomationAddIn#14](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#14)]

   Yöntemi <xref:Microsoft.Office.Interop.Excel._Worksheet.PrintPreview%2A> , belirtilen nesneyi **Baskı Önizleme** penceresinde görüntülemenizi sağlar.

### <a name="to-preview-a-page-before-printing"></a>Yazdırmadan önce bir sayfayı önizlemek için

1. Etkin çalışma sayfasının yöntemini çağırın. <xref:Microsoft.Office.Interop.Excel._Worksheet.PrintPreview%2A>

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#15](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#15)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#15](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#15)]

## <a name="see-also"></a>Ayrıca bkz.

- [Çalışma sayfalarıyla çalışma](../vsto/working-with-worksheets.md)
- [Nasıl yapılır: Çalışma sayfalarında program aracılığıyla yazımı denetleme](../vsto/how-to-programmatically-check-spelling-in-worksheets.md)
- [Çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md)
- [Office Projelerindeki Nesnelere Genel erişim](../vsto/global-access-to-objects-in-office-projects.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
