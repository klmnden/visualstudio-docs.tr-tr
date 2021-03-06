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
ms.openlocfilehash: cc030fed25409f5c034abfd07f1f9358bfea593b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62812702"
---
# <a name="how-to-programmatically-display-worksheet-comments"></a>Nasıl yapılır: Program aracılığıyla çalışma sayfası açıklamalarını görüntüleme
  Programlı olarak göster ve Microsoft Office Excel çalışma sayfalarında açıklamaları gizle.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="to-display-all-comments-on-a-worksheet-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesindeki bir çalışma sayfasındaki tüm açıklamaları görüntülemek için

1. Ayarlama <xref:Microsoft.Office.Interop.Excel.Comment.Visible%2A> özelliğini **true** açıklamaları göstermek istiyorsanız aksi **false**. Bu kod, bir sayfa sınıfında değil yerleştirilmelidir `ThisWorkbook` sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomation#31](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#31)]
     [!code-vb[Trin_VstcoreExcelAutomation#31](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#31)]

## <a name="to-display-all-comments-on-a-worksheet-in-an-application-level-vsto-add-in"></a>Çalışma sayfasındaki bir uygulama düzeyinde VSTO eklenti tüm açıklamaları görüntülemek için

1. Ayarlama <xref:Microsoft.Office.Interop.Excel.Comment.Visible%2A> özelliğini **true** açıklamaları göstermek istiyorsanız aksi **false**.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#21](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#21)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#21](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#21)]

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)
- [Nasıl yapılır: Programlı olarak ekleyin ve çalışma yorumları Sil](../vsto/how-to-programmatically-add-and-delete-worksheet-comments.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
