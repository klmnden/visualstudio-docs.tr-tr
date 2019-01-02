---
title: 'Nasıl Yapılır: Yeni çalışma kitaplarını program aracılığıyla oluşturma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Excel [Office development in Visual Studio], creating workbooks
- workbooks, creating
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 5e68b2c955c2e44fb9f721850be2fa4dac9cf875
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53958283"
---
# <a name="how-to-programmatically-create-new-workbooks"></a>Nasıl Yapılır: Yeni çalışma kitaplarını program aracılığıyla oluşturma
  Bir çalışma kitabı programlı olarak oluşturduğunuzda, yerel olduğu <xref:Microsoft.Office.Interop.Excel.Workbook> nesnesi değil, bir <xref:Microsoft.Office.Tools.Excel.Workbook> konak öğesi.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
 Oluşturabileceğiniz bir <xref:Microsoft.Office.Tools.Excel.Workbook> konak öğesi için bir <xref:Microsoft.Office.Interop.Excel.Workbook> VSTO eklenti projesinde nesne. Daha fazla bilgi için [genişletmek Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında VSTO Add-Ins](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).  
  
## <a name="to-create-a-new-workbook"></a>Yeni bir çalışma kitabı oluşturmak için  
  
1.  Kullanım <xref:Microsoft.Office.Interop.Excel.Workbooks.Add%2A> yöntemi <xref:Microsoft.Office.Interop.Excel.Workbooks> koleksiyonu.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#1](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#1)]
     [!code-vb[Trin_VstcoreExcelAutomation#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#1)]  
  
    > [!NOTE]  
    >  Varsayılan şablonu dışındaki bir şablonu temel alan bir çalışma kitabı oluşturabilirsiniz: bir parametre olarak kullanmak istediğiniz şablonu geçirmek <xref:Microsoft.Office.Interop.Excel.Workbooks.Add%2A> yöntemi.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Word belgelerini ve Excel çalışma kitaplarını VSTO eklentileri çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)   
 [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)   
 [Çalışma kitaplarıyla çalışma](../vsto/working-with-workbooks.md)   
 [Nasıl yapılır: Program aracılığıyla çalışma kitaplarını açma](../vsto/how-to-programmatically-open-workbooks.md)   
 [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kaydetme](../vsto/how-to-programmatically-save-workbooks.md)   
 [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kapatma](../vsto/how-to-programmatically-close-workbooks.md)   
 [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)   
 [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)  
