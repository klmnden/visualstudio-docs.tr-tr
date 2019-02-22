---
title: 'Nasıl yapılır: Koddaki çalışma sayfası aralıklarına program aracılığıyla bakma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, referring to
- worksheets, referring to ranges
- referring to worksheet ranges
- Excel [Office development in Visual Studio], referring to worksheet ranges
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: be71d18b7fa0b3cc9dba8a27c6c462d5ea1a2434
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56608451"
---
# <a name="how-to-programmatically-refer-to-worksheet-ranges-in-code"></a>Nasıl yapılır: Koddaki çalışma sayfası aralıklarına program aracılığıyla bakma
  Benzer bir süreç içeriğine başvurmak için kullandığınız bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi veya yerel Excel range nesnesi.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="use-a-namedrange-control"></a>NamedRange denetimi kullanma
 Aşağıdaki örnek ekler bir <xref:Microsoft.Office.Tools.Excel.NamedRange> çalışma ve hücre aralığı içinde metin ekler.

### <a name="to-refer-to-a-namedrange-control"></a>NamedRange denetimine başvurmak için

1.  Bir dizeye atama <xref:Microsoft.Office.Tools.Excel.NamedRange.Value2%2A> özelliği <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi. Bu kod, bir sayfa sınıfında değil yerleştirilmelidir `ThisWorkbook` sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomation#46](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#46)]
     [!code-vb[Trin_VstcoreExcelAutomation#46](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#46)]

## <a name="use-native-excel-ranges"></a>Yerel Excel aralıkları kullanın
 Aşağıdaki örnek, bir çalışma sayfasına yerel Excel aralığı ekler ve hücre aralığı içinde metin ekler.

### <a name="to-refer-to-a-native-range-object"></a>Bir yerel aralığı nesnesine başvurmak için

1.  Bir dizeye atama <xref:Microsoft.Office.Interop.Excel.Range.Value2%2A> aralık özelliği.

     [!code-csharp[Trin_VstcoreExcelAutomation#47](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#47)]
     [!code-vb[Trin_VstcoreExcelAutomation#47](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#47)]

## <a name="see-also"></a>Ayrıca bkz.
- [Aralıklarla çalışma](../vsto/working-with-ranges.md)
- [Nasıl yapılır: Program aracılığıyla çalışma sayfaları Yazımı denetleme](../vsto/how-to-programmatically-check-spelling-in-worksheets.md)
- [Nasıl yapılır: Program aracılığıyla çalışma kitaplarındaki aralıklara biçimler uygulama](../vsto/how-to-programmatically-apply-styles-to-ranges-in-workbooks.md)
- [Nasıl yapılır: Program aracılığıyla otomatik biçimde aralıkları artımlı şekilde değişen verilerle ile doldurun.](../vsto/how-to-programmatically-automatically-fill-ranges-with-incrementally-changing-data.md)
- [Nasıl yapılır: Program aracılığıyla çalışma sayfası aralıklarında metin arama](../vsto/how-to-programmatically-search-for-text-in-worksheet-ranges.md)
- [NamedRange denetimi](../vsto/namedrange-control.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
