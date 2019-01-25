---
title: 'Nasıl yapılır: Son çalışma kitabı dosyalarını program aracılığıyla listesi kullanılan'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, listing recently used
- RecentFiles property
- Excel [Office development in Visual Studio], recently used files listing
- recent file list, Excel
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 6451aa5427799f0905d19b7b90e87f8cca3d0bbd
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54863194"
---
# <a name="how-to-programmatically-list-recently-used-workbook-files"></a>Nasıl yapılır: Son çalışma kitabı dosyalarını program aracılığıyla listesi kullanılan
  <xref:Microsoft.Office.Interop.Excel._Application.RecentFiles%2A> Özelliği, Microsoft Office Excel son kullanılan dosyalar listesinde görünen tüm dosyaların adlarını içeren bir koleksiyon döndürür. Liste uzunluğu korumak için kullanıcının seçtiği dosyaları sayısına bağlı olarak değişir. Bir aralıktaki sonuçlarını görüntüleyebilirsiniz.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="to-list-recently-used-workbooks-in-a-range-object"></a>Çalışma kitapları için son kullanılan liste de aralık nesnesi  
  
1.  Son kullanılan dosyalar listesinde döngüye ve göre hücrelerde görünen adları bir <xref:Microsoft.Office.Interop.Excel.Range> nesne.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#9](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#9)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#9](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#9)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Çalışma kitaplarıyla çalışma](../vsto/working-with-workbooks.md)   
 [NamedRange denetimi](../vsto/namedrange-control.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)  
