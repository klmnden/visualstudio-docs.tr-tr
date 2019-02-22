---
title: 'Nasıl yapılır: Program aracılığıyla çalışma sayfası açıklamalarını görüntüleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- worksheets, comments
- comments, worksheets
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 117643390f5c6bd9e62ec0ee8c8d58c28ec4e1b8
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56602253"
---
# <a name="how-to-programmatically-display-worksheet-comments"></a>Nasıl yapılır: Program aracılığıyla çalışma sayfası açıklamalarını görüntüleme
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
- [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)
- [Nasıl yapılır: Programlı olarak ekleyin ve çalışma yorumları Sil](../vsto/how-to-programmatically-add-and-delete-worksheet-comments.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
