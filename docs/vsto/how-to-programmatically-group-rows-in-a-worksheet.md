---
title: 'Nasıl yapılır: Çalışma sayfasında satırları program aracılığıyla Grup'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- worksheets, creating groups
- groups, creating in worksheets
- ranges, creating groups
- worksheets, clearing groups
- groups
- groups [Office development in Visual Studio], clearing in worksheets
- worksheets, ungrouping rows and columns
- rows [Office development in Visual Studio], ungrouping
- columns [Office development in Visual Studio], ungrouping
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5249edccaed24dbdc6eb42b5da3e78825f1a2053
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54874424"
---
# <a name="how-to-programmatically-group-rows-in-a-worksheet"></a>Nasıl yapılır: Çalışma sayfasında satırları program aracılığıyla Grup
  Bir veya daha fazla satırı gruplayabilirsiniz. Çalışma grubu oluşturmak için bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi veya yerel Excel range nesnesi.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="use-a-namedrange-control"></a>NamedRange denetimi kullanma  
 Eklerseniz bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi için belge düzeyi projesinde tasarım zamanında denetimi program aracılığıyla bir grup oluşturmak için kullanabilirsiniz. Aşağıdaki örnek üç olduğunu varsayar <xref:Microsoft.Office.Tools.Excel.NamedRange> aynı çalışma sayfasındaki denetimleri: `data2001`, `data2002`, ve `dataAll`. Çalışma sayfasındaki tüm satırın her adlandırılmış aralık ifade eder.  
  
### <a name="to-create-a-group-of-namedrange-controls-on-a-worksheet"></a>Çalışma sayfasındaki NamedRange denetimlerinin bir grup oluşturmak için  
  
1.  Üç adlandırılmış aralıklar çağırarak grup <xref:Microsoft.Office.Tools.Excel.NamedRange.Group%2A> her aralığın yöntemi. Bu kod, bir sayfa sınıfında değil yerleştirilmelidir `ThisWorkbook` sınıfı.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#32](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#32)]
     [!code-vb[Trin_VstcoreExcelAutomation#32](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#32)]  
  
    > [!NOTE]  
    >  Satırları çözmek için çağrı <xref:Microsoft.Office.Tools.Excel.NamedRange.Ungroup%2A> yöntemi.  
  
## <a name="use-native-excel-ranges"></a>Yerel Excel aralıkları kullanın  
 Kod üç Excel aralıkları adlı olduğunu varsayar `data2001`, `data2002`, ve `dataAll` çalışma sayfasında.  
  
### <a name="to-create-a-group-of-excel-ranges-in-a-worksheet"></a>Çalışma sayfasında Excel aralıklarında bir grup oluşturmak için  
  
1.  Üç adlandırılmış aralıklar çağırarak grup <xref:Microsoft.Office.Interop.Excel.Range.Group%2A> her aralığın yöntemi. Aşağıdaki örnek üç olduğunu varsayar <xref:Microsoft.Office.Interop.Excel.Range> adlarında `data2001`, `data2002`, ve `dataAll` aynı çalışma sayfasında. Çalışma sayfasındaki tüm satırın her adlandırılmış aralık ifade eder.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#33](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#33)]
     [!code-vb[Trin_VstcoreExcelAutomation#33](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#33)]  
  
    > [!NOTE]  
    >  Satırları çözmek için çağrı <xref:Microsoft.Office.Interop.Excel.Range.Ungroup%2A> yöntemi.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)   
 [NamedRange denetimi](../vsto/namedrange-control.md)   
 [Nasıl yapılır: Çalışma sayfalarına NamedRange denetimleri ekleme](../vsto/how-to-add-namedrange-controls-to-worksheets.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)  
