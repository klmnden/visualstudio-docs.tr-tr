---
title: 'Nasıl yapılır: Program aracılığıyla Excel hesapları çalıştırma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, running calculations
- calculations, running in Excel
- Excel [Office development in Visual Studio], running calculations programmatically
- workbooks, running calculations
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: bd6562a48a66c1c73cd281fb4510e2df737f6a04
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60107274"
---
# <a name="how-to-programmatically-run-excel-calculations"></a>Nasıl yapılır: Program aracılığıyla Excel hesapları çalıştırma
  Benzer bir süreç hesaplamaları çalıştırmak için kullandığınız bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi veya yerel Excel range nesnesi.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="run-calculations-in-a-namedrange-control"></a>NamedRange denetimi içinde hesaplamaları çalıştırma
 Aşağıdaki örnek, oluşturur bir <xref:Microsoft.Office.Tools.Excel.NamedRange> hücreden A1 ve hücre hesaplar. Bu kod, bir sayfa sınıfında değil yerleştirilmelidir `ThisWorkbook` sınıfı.

### <a name="to-run-calculations-in-a-namedrange-control"></a>NamedRange denetimi içinde hesaplamaları çalıştırmak için

1. Adlandırılmış aralık oluşturun.

     [!code-csharp[Trin_VstcoreExcelAutomation#75](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#75)]
     [!code-vb[Trin_VstcoreExcelAutomation#75](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#75)]

2. Çağrı <xref:Microsoft.Office.Tools.Excel.NamedRange.Calculate%2A> belirtilen aralığın yöntemi.

     [!code-csharp[Trin_VstcoreExcelAutomation#76](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#76)]
     [!code-vb[Trin_VstcoreExcelAutomation#76](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#76)]

## <a name="run-calculations-in-a-native-excel-range"></a>Yerel bir Excel aralığında hesaplamaları çalıştırma

### <a name="to-run-calculations-in-a-native-excel-range"></a>Yerel bir Excel aralığında hesaplamaları çalıştırmak için

1. Adlandırılmış aralık oluşturun.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#30](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#30)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#30](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#30)]

2. Çağrı <xref:Microsoft.Office.Interop.Excel.Range.Calculate%2A> belirtilen aralığın yöntemi.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#31](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#31)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#31](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#31)]

## <a name="see-also"></a>Ayrıca bkz.
- [Aralıklarla çalışma](../vsto/working-with-ranges.md)
- [NamedRange denetimi](../vsto/namedrange-control.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
