---
title: 'Nasıl yapılır: Çalışma kitabındaki tüm çalışma sayfalarını program aracılığıyla listeleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, listing worksheets
- worksheets, listing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: c9f6a27ea1f8d6c50b4b9b8eba07186f34eb143b
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56616644"
---
# <a name="how-to-programmatically-list-all-worksheets-in-a-workbook"></a>Nasıl yapılır: Çalışma kitabındaki tüm çalışma sayfalarını program aracılığıyla listeleme
  <xref:Microsoft.Office.Interop.Excel.Workbook> Sağlar sınıfını bir <xref:Microsoft.Office.Interop.Excel.Worksheets> nesne. Tüm koleksiyonu bu nesneyi içeren <xref:Microsoft.Office.Interop.Excel.Worksheet> çalışma kitabında nesneleri.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="to-list-all-existing-worksheets-in-a-workbook-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesindeki bir çalışma kitabında var olan tüm çalışma sayfalarını listelemek için

1.  Yinelemek <xref:Microsoft.Office.Interop.Excel.Worksheets> toplama ve gönderme uzak bir hücreye her sayfanın adını bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi.

     [!code-csharp[Trin_VstcoreExcelAutomation#21](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#21)]
     [!code-vb[Trin_VstcoreExcelAutomation#21](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#21)]

## <a name="to-list-all-existing-worksheets-in-a-workbook-in-a-vsto-add-in"></a>Bir VSTO eklentisi kitabında var olan tüm çalışma sayfalarını listelemek için

1.  Yinelemek <xref:Microsoft.Office.Interop.Excel.Worksheets> toplama ve gönderme uzak bir hücreye her sayfanın adını bir <xref:Microsoft.Office.Interop.Excel.Range> nesne.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#13](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#13)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#13](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#13)]

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)
- [Nasıl yapılır: Program aracılığıyla çalışma kitapları için yeni çalışma sayfaları ekleme](../vsto/how-to-programmatically-add-new-worksheets-to-workbooks.md)
- [Nasıl yapılır: Kitaplarındaki program aracılığıyla taşıma](../vsto/how-to-programmatically-move-worksheets-within-workbooks.md)
- [Office projelerindeki nesnelere genel erişim](../vsto/global-access-to-objects-in-office-projects.md)
