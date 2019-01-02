---
title: 'Nasıl Yapılır: Çalışma sayfalarından program aracılığıyla korumayı kaldırma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- worksheets, unprotecting
- documents [Office development in Visual Studio], document protection
- document protection, removing from worksheets
- Unprotect method
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: cd0aacdd168c65cda9f7ac57880e3216b3fb3daa
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53956146"
---
# <a name="how-to-programmatically-remove-protection-from-worksheets"></a>Nasıl Yapılır: Çalışma sayfalarından program aracılığıyla korumayı kaldırma
  Ayrıca, Microsoft Office Excel çalışma sayfasından program aracılığıyla korumayı kaldırma.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
 Aşağıdaki örnekte değişken `getPasswordFromUser`, kullanıcıdan alınan bir parola içerir.  
  
## <a name="to-unprotect-a-worksheet-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesindeki bir çalışma sayfasının korumasını kaldırmak için  
  
1.  Çağrı <xref:Microsoft.Office.Tools.Excel.Worksheet.Unprotect%2A> yöntemi çalışma ve gerekirse parolayı geçirin. Bu örnek adlı bir çalışma sayfası ile çalıştığını varsayar `Sheet1`.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#28](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#28)]
     [!code-vb[Trin_VstcoreExcelAutomation#28](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#28)]  
  
## <a name="to-unprotect-a-worksheet-in-a-vsto-add-in"></a>Bir VSTO eklentisi, bir çalışma sayfasının korumasını kaldırmak için  
  
1.  Çağrı <xref:Microsoft.Office.Interop.Excel._Worksheet.Unprotect%2A> yöntemi etkin çalışma ve gerekirse parolayı geçirin.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#18](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#18)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#18](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#18)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)   
 [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla koruma](../vsto/how-to-programmatically-protect-worksheets.md)   
 [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla koruma](../vsto/how-to-programmatically-protect-workbooks.md)   
 [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla gizleme](../vsto/how-to-programmatically-hide-worksheets.md)   
 [Office projelerindeki nesnelere genel erişim](../vsto/global-access-to-objects-in-office-projects.md)  
