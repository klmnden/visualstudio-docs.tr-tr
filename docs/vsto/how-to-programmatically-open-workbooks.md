---
title: 'Nasıl yapılır: Program aracılığıyla çalışma kitaplarını açma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, opening
- Excel [Office development in Visual Studio], opening workbooks
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: f9d8ab4be67ffd84406869c956f9046a53d6ec79
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56611899"
---
# <a name="how-to-programmatically-open-workbooks"></a>Nasıl yapılır: Program aracılığıyla çalışma kitaplarını açma
  <xref:Microsoft.Office.Interop.Excel.Workbooks> Microsoft Office Excel koleksiyonda mümkün kılar açık olan tüm çalışma kitapları ile ve çalışma kitaplarını açma.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="to-open-an-existing-workbook"></a>Mevcut bir çalışma kitabını açmak için

1.  Kullanım <xref:Microsoft.Office.Interop.Excel.Workbooks.Open%2A> yöntemi <xref:Microsoft.Office.Interop.Excel.Workbooks> yolu çalışma kitabına geçirme koleksiyonu.

     [!code-csharp[Trin_VstcoreExcelAutomation#2](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#2)]
     [!code-vb[Trin_VstcoreExcelAutomation#2](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#2)]

## <a name="compile-the-code"></a>Kod derleme
 Bu kod örneği için aşağıdakiler gereklidir:

-   Adlı bir çalışma kitabı `YourWorkbook.xls` adlı bir dizinde bulunmalıdır `Test` c sürücüsünün

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma kitaplarıyla çalışma](../vsto/working-with-workbooks.md)
- [Nasıl yapılır: Metin dosyalarını program aracılığıyla çalışma kitapları olarak açma](../vsto/how-to-programmatically-open-text-files-as-workbooks.md)
- [Nasıl yapılır: Yeni çalışma kitaplarını program aracılığıyla oluşturma](../vsto/how-to-programmatically-create-new-workbooks.md)
- [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kaydetme](../vsto/how-to-programmatically-save-workbooks.md)
- [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kapatma](../vsto/how-to-programmatically-close-workbooks.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
