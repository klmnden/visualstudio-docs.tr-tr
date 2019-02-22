---
title: 'Nasıl yapılır: Çalışma sayfalarını program aracılığıyla gizleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- hidden worksheets
- worksheets, hiding
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 6fe1ebb3316acfc53ac29ea734413cc0cf2cb15e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56638562"
---
# <a name="how-to-programmatically-hide-worksheets"></a>Nasıl yapılır: Çalışma sayfalarını program aracılığıyla gizleme
  Göstermek veya çalışma kitabındaki gizle. Bir çalışma sayfasını gizlemek için çalışma sayfası konak öğesi kullanın veya çalışma kitabını sayfaları koleksiyonunu kullanarak çalışma sayfasına erişin.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="use-the-worksheet-host-item"></a>Çalışma sayfası konak öğesi kullanın
 Belge düzeyi özelleştirmesinde tasarım zamanında çalışma eklendiyse kullanın <xref:Microsoft.Office.Tools.Excel.Worksheet.Visible%2A> belirtilen çalışma gizlemek için özelliği.

### <a name="to-hide-a-worksheet-using-a-worksheet-host-item"></a>Bir çalışma sayfası konak öğesi kullanarak çalışma sayfasındaki gizlemek için

1.  Ayarlama <xref:Microsoft.Office.Tools.Excel.Worksheet.Visible%2A> özelliği `Sheet1` konak öğesi <xref:Microsoft.Office.Interop.Excel.XlSheetVisibility.xlSheetHidden> numaralandırma değeri.

     [!code-csharp[Trin_VstcoreExcelAutomation#25](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#25)]
     [!code-vb[Trin_VstcoreExcelAutomation#25](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#25)]

## <a name="use-the-sheets-collection-of-the-excel-workbook"></a>Excel çalışma kitabını sayfaları koleksiyonunu kullanın
 Microsoft Office Excel çalışma sayfalarına erişim <xref:Microsoft.Office.Interop.Excel.Sheets> aşağıdaki durumlarda koleksiyonu:

-   Bir VSTO eklentisi çalışma gizlemek istediğiniz.

-   Gizlemek istediğiniz çalışma sayfası, belge düzeyinde özelleştirme çalışma zamanında oluşturuldu.

### <a name="to-hide-a-worksheet-using-the-sheets-collection-of-the-excel-workbook"></a>Excel çalışma kitabını sayfaları koleksiyonunu kullanarak çalışma sayfasındaki gizlemek için

1.  Ayarlama <xref:Microsoft.Office.Interop.Excel.Worksheets.Visible%2A> özelliği çalışma sayfasının <xref:Microsoft.Office.Interop.Excel.XlSheetVisibility.xlSheetHidden> numaralandırma değeri.

     [!code-csharp[Trin_VstcoreExcelAutomation#26](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#26)]
     [!code-vb[Trin_VstcoreExcelAutomation#26](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#26)]

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)
- [Nasıl yapılır: Program aracılığıyla çalışma kitaplarından çalışma sayfaları silme](../vsto/how-to-programmatically-delete-worksheets-from-workbooks.md)
- [Nasıl yapılır: Kitaplarındaki program aracılığıyla taşıma](../vsto/how-to-programmatically-move-worksheets-within-workbooks.md)
- [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla koruma](../vsto/how-to-programmatically-protect-worksheets.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Office projelerindeki nesnelere genel erişim](../vsto/global-access-to-objects-in-office-projects.md)
