---
title: 'Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kaydetme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, saving in XML format
- workbooks, saving
- workbooks, saving backup copies
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 0ac57569802bbab5317f59e5311e4871a6e74ba1
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60093065"
---
# <a name="how-to-programmatically-save-workbooks"></a>Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kaydetme
  Bir çalışma kitabını kaydetmek için çeşitli yollar vardır. Bir çalışma kitabı yolu değiştirmeden kaydedebilirsiniz. Çalışma kitabını önce kaydedilmedi, yolu belirterek, çalışma kitabını kaydetmeniz gerekir. Açık bir yol Microsoft Office Excel dosya oluşturulduğunda verilen ada sahip geçerli klasöre kaydeder. Ayrıca, çalışma kitabını Aç bellekte değiştirmeden çalışma kitabının bir kopyasını kaydedebilirsiniz.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="save-a-workbook-without-changing-the-path"></a>Bir çalışma kitabı yolu değiştirmeden kaydedin.

### <a name="to-save-a-workbook-associated-with-a-document-level-customization"></a>Belge düzeyi özelleştirme ile ilişkilendirilmiş bir çalışma kitabını kaydetmek için

1. Çağrı <xref:Microsoft.Office.Tools.Excel.Workbook.Save%2A> yöntemi `ThisWorkbook` sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomation#4](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/ThisWorkbook.cs#4)]
     [!code-vb[Trin_VstcoreExcelAutomation#4](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/ThisWorkbook.vb#4)]

### <a name="to-save-the-active-workbook-in-a-vsto-add-in"></a>Etkin çalışma kitabının VSTO eklentisi kaydetmek için

1. Çağrı <xref:Microsoft.Office.Interop.Excel._Workbook.Save%2A> etkin çalışma kitabını kaydetmek için yöntemi. Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `ThisAddIn` Excel için VSTO eklenti projesinde sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#3](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#3)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#3](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#3)]

## <a name="save-a-workbook-with-a-new-path"></a>Yeni bir yol ile bir çalışma kitabını kaydedin
 Belirtilen çalışma kitabı, bir dosya biçimi, bir parola, bir erişim modu ve isteğe bağlı olarak belirterek yeni bir konuma veya yeni bir adla kaydedebilirsiniz.

> [!NOTE]
>  Ayarlamak isteyebilirsiniz <xref:Microsoft.Office.Interop.Excel._Application.DisplayAlerts%2A> özelliğini **False** etkileşimi gerektirir çünkü bazı biçimlerde ile yeni bir yol çalışma kitabını kaydetmeden önce. Bu özelliği ayarlamak **False** Excel'in tüm varsayılanlar kullanmasına neden olur.

### <a name="to-save-a-workbook-associated-with-a-document-level-customization"></a>Belge düzeyi özelleştirme ile ilişkilendirilmiş bir çalışma kitabını kaydetmek için

1. Çağrı <xref:Microsoft.Office.Tools.Excel.Workbook.SaveAs%2A> yöntemi `ThisWorkbook` sınıfı. Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `ThisWorkbook` sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomation#5](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/ThisWorkbook.cs#5)]
     [!code-vb[Trin_VstcoreExcelAutomation#5](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/ThisWorkbook.vb#5)]

### <a name="to-save-the-active-workbook-in-a-vsto-add-in"></a>Etkin çalışma kitabının VSTO eklentisi kaydetmek için

1. Çağrı <xref:Microsoft.Office.Interop.Excel._Workbook.SaveAs%2A> etkin çalışma kitabının yeni bir yola kaydetmek için yöntemi. Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `ThisAddIn` Excel için VSTO eklenti projesinde sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#4](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#4)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#4](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#4)]

## <a name="save-a-copy-of-the-workbook"></a>Çalışma kitabının bir kopyasını Kaydet
 Bellekte açık çalışma kitabını değiştirmeden, çalışma kitabının bir kopyasını bir dosyaya kaydedebilirsiniz. Çalışma kitabı konumunu değiştirmeden bir yedek kopya oluşturmak istediğinizde bu kullanışlıdır.

### <a name="to-save-a-workbook-associated-with-a-document-level-customization"></a>Belge düzeyi özelleştirme ile ilişkilendirilmiş bir çalışma kitabını kaydetmek için

1. Çağrı <xref:Microsoft.Office.Tools.Excel.Workbook.SaveCopyAs%2A> yöntemi `ThisWorkbook` sınıfı. Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `ThisWorkbook` sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomation#6](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/ThisWorkbook.cs#6)]
     [!code-vb[Trin_VstcoreExcelAutomation#6](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/ThisWorkbook.vb#6)]

### <a name="to-save-the-active-workbook-in-a-vsto-add-in"></a>Etkin çalışma kitabının VSTO eklentisi kaydetmek için

1. Çağrı <xref:Microsoft.Office.Interop.Excel._Workbook.SaveCopyAs%2A> etkin çalışma kitabının bir kopyasını kaydetmek için yöntemi. Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `ThisAddIn` Excel için VSTO eklenti projesinde sınıfı.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#5](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#5)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#5](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#5)]

## <a name="robust-programming"></a>Güçlü programlama
 Etkileşimli olarak kaydetmek veya çalışma kitabını kopyalama yöntemlerden herhangi birini iptal ediliyor, kodunuzda bir çalışma zamanı hatası oluşturur. Örneğin, yordamı çağıran, <xref:Microsoft.Office.Tools.Excel.Workbook.SaveAs%2A> yöntemi ancak devre dışı ister Excel'de yapar ve kendi kullanıcı tıklama **iptal** istendiğinde, Excel çalışma zamanı hatası oluşturur.

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma kitaplarıyla çalışma](../vsto/working-with-workbooks.md)
- [Çalışma kitabı konak öğesi](../vsto/workbook-host-item.md)
- [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kapatma](../vsto/how-to-programmatically-close-workbooks.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
