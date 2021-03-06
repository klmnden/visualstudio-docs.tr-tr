---
title: 'Nasıl yapılır: Çalışma kitaplarını program aracılığıyla koruma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, passwords
- documents [Office development in Visual Studio], document protection
- workbooks, unprotecting
- document protection, removing from workbooks
- document protection, adding to workbooks
- workbooks, protecting
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ad45097146a7566f2d043fba5e14265c05dc4d7a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62955917"
---
# <a name="how-to-programmatically-protect-workbooks"></a>Nasıl yapılır: Çalışma kitaplarını program aracılığıyla koruma
  Kullanıcıların ekleme yapılamıyor veya çalışma sayfaları silme ve ayrıca da programlı olarak çalışma kitabının korumasını kaldırmak, Microsoft Office Excel çalışma kitabı koruyabilirsiniz. İsteğe bağlı olarak, bir parola belirtin, isterseniz (kullanıcılar sayfası taşınamıyor şekilde) korunan yapı ve korumalı çalışma kitabının windows isteyip istemediğinizi belirtin olup olmadığını gösterir.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Bir çalışma kitabını koruma hücre düzenleme kullanıcıların durdurmaz. Verileri korumak için çalışma sayfaları korumanız gerekir. Daha fazla bilgi için [nasıl yapılır: Çalışma sayfalarını program aracılığıyla koruma](../vsto/how-to-programmatically-protect-worksheets.md).

 Aşağıdaki kod örnekleri, kullanıcıdan alınan parolayı içeren bir değişkeni kullanın.

## <a name="protect-a-workbook-that-is-part-of-a-document-level-customization"></a>Belge düzeyi özelleştirmesi parçası olan çalışma kitabını koru

### <a name="to-protect-a-workbook"></a>Bir çalışma kitabını korumak için

1. Çağrı <xref:Microsoft.Office.Tools.Excel.Workbook.Protect%2A> yöntemini ve bir parola ekleyin. Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `ThisWorkbook` sayfası sınıfı değil, bir sınıf.

     [!code-csharp[Trin_VstcoreExcelAutomation#10](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/ThisWorkbook.cs#10)]
     [!code-vb[Trin_VstcoreExcelAutomation#10](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/ThisWorkbook.vb#10)]

### <a name="to-unprotect-a-workbook"></a>Bir çalışma kitabının korumasını kaldırmak için

1. Çağrı <xref:Microsoft.Office.Tools.Excel.Workbook.Unprotect%2A> yöntemi, bir parola gerekliyse geçirerek. Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `ThisWorkbook` sayfası sınıfı değil, bir sınıf.

     [!code-csharp[Trin_VstcoreExcelAutomation#11](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/ThisWorkbook.cs#11)]
     [!code-vb[Trin_VstcoreExcelAutomation#11](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/ThisWorkbook.vb#11)]

## <a name="protect-a-workbook-by-using-an-application-level-add-in"></a>Bir uygulama düzeyinde eklenti kullanarak çalışma kitabını koru

### <a name="to-protect-a-workbook"></a>Bir çalışma kitabını korumak için

1. Çağrı <xref:Microsoft.Office.Interop.Excel._Workbook.Protect%2A> yöntemini ve bir parola ekleyin. Bu kod örneği, etkin çalışma kitabının kullanır. Bu örneği kullanmak için kodu çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#6](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#6)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#6](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#6)]

### <a name="to-unprotect-a-workbook"></a>Bir çalışma kitabının korumasını kaldırmak için

1. Çağrı <xref:Microsoft.Office.Interop.Excel._Workbook.Unprotect%2A> gerekiyorsa bir parola geçirerek etkin çalışma kitabının yöntemi. Bu örneği kullanmak için kodu çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#7](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#7)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#7](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#7)]

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma kitaplarıyla çalışma](../vsto/working-with-workbooks.md)
- [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla koruma](../vsto/how-to-programmatically-protect-worksheets.md)
- [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla gizleme](../vsto/how-to-programmatically-hide-worksheets.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
