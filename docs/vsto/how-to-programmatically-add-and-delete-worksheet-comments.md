---
title: 'Nasıl Yapılır: Programlı olarak ekleyin ve çalışma yorumları Sil'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, comments
- worksheets, comments
- comments, worksheets
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: cb243498585677d6df79139bae570a9eec6270d9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53968624"
---
# <a name="how-to-programmatically-add-and-delete-worksheet-comments"></a>Nasıl Yapılır: Programlı olarak ekleyin ve çalışma yorumları Sil
  Programlı olarak ekleyebilir ve Microsoft Office Excel çalışma sayfalarında yorumları Sil. Açıklamalar, birden çok hücre aralıklarının için tek hücrelere yalnızca eklenebilir.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="add-and-delete-a-comment-in-a-document-level-project"></a>Ekleme ve bir belge düzeyi projede bir açıklamayı Sil  
 Aşağıdaki örnekler tek hücre olduğunu varsayın <xref:Microsoft.Office.Tools.Excel.NamedRange> adlı Denetim `dateComment` adlı bir çalışma sayfasına `Sheet1`.  
  
### <a name="to-add-a-new-comment-to-a-named-range"></a>Adlandırılmış bir aralık için yeni bir açıklama eklemek için  
  
1.  Çağrı <xref:Microsoft.Office.Tools.Excel.NamedRange.AddComment%2A> yöntemi <xref:Microsoft.Office.Tools.Excel.NamedRange> denetlemek ve açıklama metni girin. Bu kod yerleştirilmelidir `Sheet1` sınıfı.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#30](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#30)]
     [!code-vb[Trin_VstcoreExcelAutomation#30](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#30)]  
  
#### <a name="to-delete-a-comment-from-a-named-range"></a>Adlandırılmış bir aralıktan bir açıklamayı silmek için  
  
1.  Bir yorum aralıkta var olduğunu doğrulayın ve silin. Bu kod yerleştirilmelidir `Sheet1` sınıfı.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#29](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#29)]
     [!code-vb[Trin_VstcoreExcelAutomation#29](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#29)]  
  
## <a name="add-and-delete-a-comment-in-a-vsto-add-in-project"></a>Ekleme ve VSTO eklenti projesinde bir açıklamayı Sil  
 Aşağıdaki örnekler tek hücre olduğunu varsayın <xref:Microsoft.Office.Interop.Excel.Range> adlı `dateComment` etkin çalışma sayfasında.  
  
### <a name="to-add-a-new-comment-to-an-excel-range"></a>Bir Excel aralığı için yeni bir açıklama eklemek için  
  
1.  Çağrı <xref:Microsoft.Office.Interop.Excel.Range.AddComment%2A> yöntemi <xref:Microsoft.Office.Interop.Excel.Range> ve açıklama metni girin.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#20](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#20)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#20](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#20)]  
  
### <a name="to-delete-a-comment-from-an-excel-range"></a>Bir Excel aralığında bir açıklamayı silmek için  
  
1.  Bir yorum aralıkta var olduğunu doğrulayın ve silin.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#19](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#19)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#19](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#19)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)   
 [Nasıl yapılır: Program aracılığıyla çalışma sayfası açıklamalarını görüntüleme](../vsto/how-to-programmatically-display-worksheet-comments.md)   
 [NamedRange denetimi](../vsto/namedrange-control.md)  
