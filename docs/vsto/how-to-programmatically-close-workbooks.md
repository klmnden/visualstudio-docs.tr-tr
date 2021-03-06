---
title: 'Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kapatma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, closing
- Excel [Office development in Visual Studio], closing workbooks
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ea2ec3162ae7ffdee20f65452f67b0ddf4cc2dd1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62575409"
---
# <a name="how-to-programmatically-close-workbooks"></a>Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kapatma
  Etkin çalışma kitabının kapatabilir veya kapatmak için bir çalışma kitabı belirtebilirsiniz.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="close-the-active-workbook"></a>Etkin çalışma kitabının kapatın
 Etkin çalışma kitabının kapatmak için iki yordam vardır: belge düzeyi özelleştirmeleri ve VSTO eklentileri için.

### <a name="to-close-the-active-workbook-in-a-document-level-customization"></a>Etkin çalışma kitabının belge düzeyi özelleştirmesinde kapatmak için

1. Çağrı <xref:Microsoft.Office.Tools.Excel.Workbook.Close%2A> özelleştirme ile ilişkili çalışma kitabını kapatmak için yöntemi. Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `Sheet1` Excel için belge düzeyi projesinde sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomation#3](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#3)]
     [!code-vb[Trin_VstcoreExcelAutomation#3](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#3)]

### <a name="to-close-the-active-workbook-in-a-vsto-add-in"></a>Bir VSTO eklenti, etkin çalışma kitabının kapatmak için

1. Çağrı <xref:Microsoft.Office.Interop.Excel._Workbook.Close%2A> etkin çalışma kitabının kapatmak için yöntemi. Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `ThisAddIn` Excel için VSTO eklenti projesinde sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#1](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#1)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#1](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#1)]

## <a name="close-a-workbook-that-you-specify-by-name"></a>Belirttiğiniz ada göre bir çalışma kitabını kapatıp
 Belirttiğiniz ada göre bir çalışma kitabı kapatmak şekilde VSTO eklentileri ve belge düzeyi özelleştirmeleri için aynıdır.

### <a name="to-close-a-workbook-that-you-specify-by-name"></a>Belirttiğiniz ada göre bir çalışma kitabı kapatmak için

1. Bağımsız değişken olarak çalışma kitabının adını belirtin <xref:Microsoft.Office.Interop.Excel.Workbooks> koleksiyonu. Aşağıdaki kod örneğinde adlı bir çalışma kitabı olduğunu varsayar **NewWorkbook** Excel'de açıktır.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#2](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#2)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#2](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#2)]

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma kitaplarıyla çalışma](../vsto/working-with-workbooks.md)
- [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kaydetme](../vsto/how-to-programmatically-save-workbooks.md)
- [Nasıl yapılır: Program aracılığıyla çalışma kitaplarını açma](../vsto/how-to-programmatically-open-workbooks.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
