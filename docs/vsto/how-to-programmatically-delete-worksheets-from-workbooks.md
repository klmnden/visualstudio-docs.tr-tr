---
title: 'Nasıl yapılır: Program aracılığıyla çalışma kitaplarından çalışma sayfaları silme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, deleting worksheets
- worksheets, deleting
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 9ecc39e72a336c390c85f1caf2c80c6643acbb61
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63412525"
---
# <a name="how-to-programmatically-delete-worksheets-from-workbooks"></a>Nasıl yapılır: Program aracılığıyla çalışma kitaplarından çalışma sayfaları silme
  Çalışma kitabındaki silebilirsiniz. Bir çalışma sayfası silmek için çalışma sayfası konak öğesi kullanın veya çalışma kitabını sayfaları koleksiyonunu kullanarak çalışma sayfasına erişin.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="use-the-worksheet-host-item"></a>Çalışma sayfası konak öğesi kullanın
 Belge düzeyi özelleştirmesinde tasarım zamanında çalışma eklendiyse kullanın <xref:Microsoft.Office.Tools.Excel.Worksheet.Delete%2A> belirtilen çalışma silmek için yöntemi. Aşağıdaki kod, çalışma sayfası konak öğesi doğrudan başvuruda bulunarak, bir çalışma kitabından çalışma siler.

> [!IMPORTANT]
> Şu proje şablonlarını kullanarak oluşturduğunuz projelerde bu kodu çalıştırır:
>
> - Excel 2013'ün çalışma kitabı
> - Excel 2013 şablonu
> - Excel 2010 Çalışma Kitabı
> - Excel 2010 Şablonu
>
>   Bu görev başka bir türü proje içinde gerçekleştirmek istiyorsanız, bir başvuru eklemelisiniz **Microsoft.Office.Interop.Excel** derleme ve daha sonra derlemeye sınıflardan bir çalışma kitabını açıp bir çalışma sayfasını silmek için kullanmalısınız. Daha fazla bilgi için [nasıl yapılır: Birincil birlikte çalışma derlemeleriyle Office uygulamalarını hedefleme](../vsto/how-to-target-office-applications-through-primary-interop-assemblies.md) ve [Excel 2010 birincil birlikte çalışma bütünleştirilmiş kod başvurusu](http://go.microsoft.com/fwlink/?LinkId=189585).

### <a name="to-delete-a-worksheet-by-using-a-worksheet-host-item"></a>Bir çalışma sayfası bir çalışma sayfası konak öğesi kullanarak silmek için

1. Çağrı <xref:Microsoft.Office.Tools.Excel.Worksheet.Delete%2A> yöntemi `Sheet1`.

     [!code-csharp[Trin_VstcoreExcelAutomation#17](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#17)]
     [!code-vb[Trin_VstcoreExcelAutomation#17](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#17)]

## <a name="use-the-sheets-collection-of-the-excel-workbook"></a>Excel çalışma kitabını sayfaları koleksiyonunu kullanın
 Microsoft Office Excel çalışma sayfalarına erişim <xref:Microsoft.Office.Interop.Excel.Sheets> aşağıdaki durumlarda koleksiyonu:

- Bir VSTO eklentisi çalışma silmek istediğiniz.

- Silmek istediğiniz çalışma sayfası, belge düzeyinde özelleştirme çalışma zamanında oluşturuldu.

  Aşağıdaki kod bir çalışma kitabından dizin numarasını sayfasını başvurarak siler **sayfaları** koleksiyonu. Bu kod, yeni bir çalışma sayfasına programlı bir şekilde oluşturulduğunu varsayar.

> [!IMPORTANT]
> Bu görev başka bir türü proje içinde gerçekleştirmek istiyorsanız, bir başvuru eklemelisiniz **Microsoft.Office.Interop.Excel** derleme ve daha sonra derlemeye sınıflardan bir çalışma kitabını açıp bir çalışma sayfasını silmek için kullanmalısınız. Daha fazla bilgi için [nasıl yapılır: Birincil birlikte çalışma derlemeleriyle Office uygulamalarını hedefleme](../vsto/how-to-target-office-applications-through-primary-interop-assemblies.md) ve [Excel 2010 birincil birlikte çalışma bütünleştirilmiş kod başvurusu](http://go.microsoft.com/fwlink/?LinkId=189585).

### <a name="to-delete-a-worksheet-by-using-the-sheets-collection-of-the-excel-workbook"></a>Çalışma sayfalarını Excel çalışma kitabını koleksiyonunu kullanarak silmek için

1. Çağrı <xref:Microsoft.Office.Interop.Excel._Worksheet.Delete%2A> yöntemi <xref:Microsoft.Office.Interop.Excel.Sheets> koleksiyonu.

     [!code-csharp[Trin_VstcoreExcelAutomation#18](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#18)]
     [!code-vb[Trin_VstcoreExcelAutomation#18](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#18)]

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)
- [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla gizleme](../vsto/how-to-programmatically-hide-worksheets.md)
- [Nasıl yapılır: Kitaplarındaki program aracılığıyla taşıma](../vsto/how-to-programmatically-move-worksheets-within-workbooks.md)
- [Nasıl yapılır: Program aracılığıyla çalışma sayfaları seçme](../vsto/how-to-programmatically-select-worksheets.md)
- [Nasıl yapılır: Program aracılığıyla çalışma kitapları için yeni çalışma sayfaları ekleme](../vsto/how-to-programmatically-add-new-worksheets-to-workbooks.md)
- [Çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md)
- [Office projelerindeki nesnelere genel erişim](../vsto/global-access-to-objects-in-office-projects.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
