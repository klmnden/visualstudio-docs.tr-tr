---
title: 'Nasıl yapılır: Çalışma sayfalarını program aracılığıyla kopyalama'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- worksheets, copying
- Excel [Office development in Visual Studio], copying worksheets
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 694e96c9b3d7c88e5ef2ac3ae1e51101afbe3f25
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56621714"
---
# <a name="how-to-programmatically-copy-worksheets"></a>Nasıl yapılır: Çalışma sayfalarını program aracılığıyla kopyalama
  Çalışma kopyasını oluşturma ve çalışma önce veya sonra mevcut bir çalışma kitabında ekleyin. Çalışma sayfası ekleneceği konum belirtmezseniz, Excel çalışma sayfası yeni içeren yeni bir çalışma kitabı oluşturur.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

> [!NOTE]
>  Program aracılığıyla çalışma sayfası kopyalama ya da son kullanıcının çalışma el ile kopyalar, yeni çalışma arkasındaki kod yok ve yeni çalışma sayfasındaki denetimleri çalışmaz. Yeni kopyalanan bir çalışma sayfası olmasıdır bir <xref:Microsoft.Office.Interop.Excel.Worksheet> nesnesi ve bir <xref:Microsoft.Office.Tools.Excel.Worksheet> konak öğesi. Konak denetimlerinin ve Windows Forms denetimleri, ana bilgisayar öğeleri yalnızca eklenebilir. Daha fazla bilgi için [konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md).

## <a name="to-add-a-copied-worksheet-to-a-workbook-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesindeki bir çalışma kitabı kopyalanan bir çalışma sayfası eklemek için

1.  Kullanım <xref:Microsoft.Office.Interop.Excel.Worksheets.Copy%2A> geçerli çalışma kitabında çalışma sayfası ilk kopyalayın ve kopyayı üçüncü sayfadan sonra yerleştirmek için yöntemi.

     [!code-csharp[Trin_VstcoreExcelAutomation#16](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#16)]
     [!code-vb[Trin_VstcoreExcelAutomation#16](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#16)]

## <a name="to-add-a-copied-worksheet-to-a-workbook-in-a-vsto-add-in"></a>Kopyalanan çalışma sayfası bir çalışma kitabında bir VSTO eklenti eklemek için

1.  Kullanım <xref:Microsoft.Office.Interop.Excel.Worksheets.Copy%2A> geçerli çalışma kitabında çalışma sayfası ilk kopyalayın ve kopyayı üçüncü sayfadan sonra yerleştirmek için yöntemi.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#12](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#12)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#12](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#12)]

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Nasıl yapılır: Program aracılığıyla çalışma kitapları için yeni çalışma sayfaları ekleme](../vsto/how-to-programmatically-add-new-worksheets-to-workbooks.md)
- [Nasıl yapılır: Program aracılığıyla çalışma kitaplarından çalışma sayfaları silme](../vsto/how-to-programmatically-delete-worksheets-from-workbooks.md)
- [Nasıl yapılır: Program aracılığıyla çalışma sayfaları seçme](../vsto/how-to-programmatically-select-worksheets.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Office projelerindeki nesnelere genel erişim](../vsto/global-access-to-objects-in-office-projects.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
