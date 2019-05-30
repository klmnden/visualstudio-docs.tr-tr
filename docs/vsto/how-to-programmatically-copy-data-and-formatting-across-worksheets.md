---
title: Veri kopyalama ve çalışma sayfaları arasında program aracılığıyla biçimlendirme
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- worksheets, copying data
- formatting [Office development in Visual Studio]
- data [Office development in Visual Studio], copying across worksheets
- copying data, Office development in Visual Studio
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: b90704d6d9fe555920fb042939079bd53884cfbe
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66402204"
---
# <a name="how-to-programmatically-copy-data-and-formatting-across-worksheets"></a>Nasıl yapılır: Veri ve biçimlendirme çalışma sayfaları arasında program aracılığıyla kopyalama
  Verileri bir sayfada bir aralıktan çalışma kitabındaki diğer tüm sayfaları kullanarak kopyalayabilirsiniz <xref:Microsoft.Office.Interop.Excel.Worksheets.FillAcrossSheets%2A> yöntemi. Bir aralığı belirtin ve verileri, biçimlendirme veya her ikisi de kopyalamak istediğiniz.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="example"></a>Örnek
 [!code-csharp[Trin_VstcoreExcelAutomation#44](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#44)]
 [!code-vb[Trin_VstcoreExcelAutomation#44](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#44)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek adlı bir aralık gerektirir `rangeData` çalışma sayfasında.

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)
- [Nasıl yapılır: Program aracılığıyla çalışma kitapları için yeni çalışma sayfaları ekleme](../vsto/how-to-programmatically-add-new-worksheets-to-workbooks.md)
- [Nasıl yapılır: Program aracılığıyla seçili hücreler içeren çalışma sayfalarındaki satırlarda biçimlendirmeyi değiştirme](../vsto/how-to-programmatically-change-formatting-in-worksheet-rows-containing-selected-cells.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
