---
title: 'Nasıl Yapılır: Program aracılığıyla çalışma sayfası açıklamalarını görüntüleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- worksheets, comments
- comments, worksheets
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: c246eae0465c64598aae1191c4053f8ba266b6ff
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53831569"
---
# <a name="how-to-programmatically-display-worksheet-comments"></a>Nasıl Yapılır: Program aracılığıyla çalışma sayfası açıklamalarını görüntüleme
  Programlı olarak göster ve Microsoft Office Excel çalışma sayfalarında açıklamaları gizle.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="to-display-all-comments-on-a-worksheet-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesindeki bir çalışma sayfasındaki tüm açıklamaları görüntülemek için  
  
1.  Ayarlama <xref:Microsoft.Office.Interop.Excel.Comment.Visible%2A> özelliğini **true** açıklamaları göstermek istiyorsanız aksi **false**. Bu kod, bir sayfa sınıfında değil yerleştirilmelidir `ThisWorkbook` sınıfı.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#31](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#31)]
     [!code-vb[Trin_VstcoreExcelAutomation#31](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#31)]  
  
## <a name="to-display-all-comments-on-a-worksheet-in-an-application-level-vsto-add-in"></a>Çalışma sayfasındaki bir uygulama düzeyinde VSTO eklenti tüm açıklamaları görüntülemek için  
  
1.  Ayarlama <xref:Microsoft.Office.Interop.Excel.Comment.Visible%2A> özelliğini **true** açıklamaları göstermek istiyorsanız aksi **false**.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#21](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#21)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#21](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#21)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)   
 [Nasıl yapılır: Programlı olarak ekleyin ve çalışma yorumları Sil](../vsto/how-to-programmatically-add-and-delete-worksheet-comments.md)   
 [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)  
