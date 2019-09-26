---
title: 'Nasıl yapılır: Program aracılığıyla çalışma sayfalarını seçme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- worksheets, selecting
- Excel projects, selecting worksheets
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 20ebc8fea14b3dc52c802543f97318ec7fae7529
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255624"
---
# <a name="how-to-programmatically-select-worksheets"></a>Nasıl yapılır: Program aracılığıyla çalışma sayfalarını seçme
  <xref:Microsoft.Office.Tools.Excel.Worksheet.Select%2A> Yöntemi, kullanıcının seçimini yeni nesneye taşırken belirtilen nesneyi seçer. Kullanıcının seçimini değiştirmeden nesneye odağı getirmek istiyorsanız yönteminikullanın.<xref:Microsoft.Office.Tools.Excel.Worksheet.Activate%2A>

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Bir VSTO eklentisinin içinde varolan bir çalışma sayfası seçmek istiyorsanız veya çalışma sayfası belge düzeyi özelleştirmesinde çalışma zamanında oluşturulduysa, Excel çalışma kitabının Excel <xref:Microsoft.Office.Interop.Excel.Sheets> koleksiyonunu kullanarak erişmeniz gerekir; Aksi takdirde, <xref:Microsoft.Office.Tools.Excel.Worksheet>doğrudan konak öğesi.

## <a name="use-the-worksheet-host-item"></a>Çalışma sayfası konak öğesini kullan
 Belge düzeyi özelleştirmesinde, *Sheet1. vb* veya *Sheet1.cs*' ye aşağıdaki kodu ekleyin.

### <a name="to-select-the-first-worksheet-in-a-workbook-using-a-host-item"></a>Bir konak öğesi kullanarak çalışma kitabındaki ilk çalışma sayfasını seçmek için

1. <xref:Microsoft.Office.Tools.Excel.Worksheet.Select%2A> Yöntemini`Sheet1`çağırın.

     [!code-csharp[Trin_VstcoreExcelAutomation#19](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#19)]
     [!code-vb[Trin_VstcoreExcelAutomation#19](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#19)]

## <a name="use-the-sheets-collection-of-the-excel-workbook"></a>Excel çalışma kitabının sayfalar koleksiyonunu kullanın
 Excel <xref:Microsoft.Office.Interop.Excel.Sheets> koleksiyonunu kullanarak çalışma sayfasına erişin.

### <a name="to-select-the-first-worksheet-in-a-workbook-using-the-sheets-collection-of-the-excel-workbook"></a>Excel çalışma kitabının sayfalar koleksiyonunu kullanarak çalışma kitabındaki ilk çalışma sayfasını seçmek için

1. Etkin çalışma kitabının ilk çalışma <xref:Microsoft.Office.Interop.Excel.Sheets> sayfasını seçmek için koleksiyonun yönteminiçağırın.<xref:Microsoft.Office.Interop.Excel.Sheets.Select%2A>

     [!code-csharp[Trin_VstcoreExcelAutomation#20](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#20)]
     [!code-vb[Trin_VstcoreExcelAutomation#20](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#20)]

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma sayfalarıyla çalışma](../vsto/working-with-worksheets.md)
- [Nasıl yapılır: Program aracılığıyla yazdırma çalışma sayfaları](../vsto/how-to-programmatically-print-worksheets.md)
- [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla çalışma kitaplarından silme](../vsto/how-to-programmatically-delete-worksheets-from-workbooks.md)
- [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla gizleme](../vsto/how-to-programmatically-hide-worksheets.md)
- [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla koruma](../vsto/how-to-programmatically-protect-worksheets.md)
- [Çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md)
- [Office Projelerindeki Nesnelere Genel erişim](../vsto/global-access-to-objects-in-office-projects.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
