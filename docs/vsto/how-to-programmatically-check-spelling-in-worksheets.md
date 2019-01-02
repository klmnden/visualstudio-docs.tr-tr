---
title: 'Nasıl Yapılır: Program aracılığıyla çalışma sayfaları Yazımı denetleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- spellchecking
- spelling checker, worksheets
- worksheets, checking spelling
- spelling, checking in worksheets
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: ea589f30c026ddf946cb43811818b54d3df9b2e2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53899976"
---
# <a name="how-to-programmatically-check-spelling-in-worksheets"></a>Nasıl Yapılır: Program aracılığıyla çalışma sayfaları Yazımı denetleme
  Program aracılığıyla çalışma sayfasındaki bir kelimelerin yazımı kontrol edebilirsiniz. **Yazım** iletişim kutusu otomatik olarak görünüp görünmeyeceğini yanlış yazılmış kelimelerden çalışma sayfasında.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="to-check-spelling-in-a-worksheet-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesinde çalışma sayfasında yazım denetimi  
  
1.  Çağrı <xref:Microsoft.Office.Tools.Excel.Worksheet.CheckSpelling%2A> çalışma sayfasının yöntemi.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#45](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#45)]
     [!code-vb[Trin_VstcoreExcelAutomation#45](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#45)]  
  
## <a name="to-check-spelling-in-a-worksheet-in-a-vsto-add-in"></a>Bir VSTO eklentisi, çalışma sayfasında yazım denetimi  
  
1.  Çağrı <xref:Microsoft.Office.Interop.Excel._Worksheet.CheckSpelling%2A> etkin çalışma sayfasının yöntemi.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#22](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#22)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#22](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#22)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)   
 [Nasıl yapılır: Program aracılığıyla Excel hesapları çalıştırma](../vsto/how-to-programmatically-run-excel-calculations-programmatically.md)   
 [NamedRange denetimi](../vsto/namedrange-control.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)  
