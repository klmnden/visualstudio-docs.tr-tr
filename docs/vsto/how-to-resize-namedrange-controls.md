---
title: 'Nasıl yapılır: NamedRange denetimlerini yeniden boyutlandır'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- controls [Office development in Visual Studio], resizing
- NamedRange control, resizing
- ranges, resizing in Excel
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 80a7fd251d525541b6894c757d7acd148900047c
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71252046"
---
# <a name="how-to-resize-namedrange-controls"></a>Nasıl yapılır: NamedRange denetimlerini yeniden boyutlandır
  Bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimin boyutunu Microsoft Office Excel belgesine eklediğinizde ayarlayabilirsiniz; ancak, daha sonra yeniden boyutlandırmak isteyebilirsiniz.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Belge düzeyi projelerinde, tasarım zamanında veya çalışma zamanında adlandırılmış bir aralığı yeniden boyutlandırabilirsiniz. Ayrıca, uygulama düzeyi VSTO Eklentilerindeki çalışma zamanında adlandırılmış aralıkları yeniden boyutlandırabilirsiniz.

 Bu konuda aşağıdaki görevler açıklanmaktadır:

- [Tasarım zamanında NamedRange denetimlerini yeniden boyutlandır](#designtime)

- [Belge düzeyindeki bir projede, çalışma zamanında NamedRange denetimlerini yeniden boyutlandırma](#runtimedoclevel)

- [VSTO eklenti projesindeki NamedRange denetimlerini çalışma zamanında yeniden boyutlandırma](#runtimeaddin)

## <a name="designtime"></a>Tasarım zamanında NamedRange denetimlerini yeniden boyutlandır
 **Adı tanımla** iletişim kutusunda boyutunu tekrar tanımlayarak adlandırılmış bir aralığı yeniden boyutlandırabilirsiniz.

### <a name="to-resize-a-named-range-by-using-the-define-name-dialog-box"></a>Adlandırılmış bir aralığı adı tanımla iletişim kutusunu kullanarak yeniden boyutlandırmak için

1. Bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetime sağ tıklayın.

2. Kısayol menüsünde **adlandırılmış aralıkları Yönet** ' e tıklayın.

     **Ad tanımla** iletişim kutusu görüntülenir.

3. Yeniden boyutlandırmak istediğiniz adlandırılmış aralığı seçin.

4. **Başvuruda** bulunan kutusunun işaretini kaldırın.

5. Adlandırılmış aralığın boyutunu tanımlamak için kullanmak istediğiniz hücreleri seçin.

6. **Tamam**'ı tıklatın.

## <a name="runtimedoclevel"></a>Belge düzeyindeki bir projede, çalışma zamanında NamedRange denetimlerini yeniden boyutlandırma
 <xref:Microsoft.Office.Tools.Excel.NamedRange.RefersTo%2A> Özelliği kullanarak adlandırılmış bir aralığı programlı şekilde yeniden boyutlandırabilirsiniz.

> [!NOTE]
> **Özellikler** penceresinde, <xref:Microsoft.Office.Tools.Excel.NamedRange.RefersTo%2A> özelliği salt okunurdur olarak işaretlenir.

### <a name="to-resize-a-named-range-programmatically"></a>Adlandırılmış bir aralığı programlı olarak yeniden boyutlandırmak için

1. <xref:Microsoft.Office.Tools.Excel.NamedRange> **A1** hücresindebirdenetimoluşturun.`Sheet1`

     [!code-csharp[Trin_VstcoreHostControlsExcel#4](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#4)]
     [!code-vb[Trin_VstcoreHostControlsExcel#4](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#4)]

2. Adlandırılmış aralığı **B1**hücresini içerecek şekilde yeniden boyutlandırın.

     [!code-csharp[Trin_VstcoreHostControlsExcel#5](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#5)]
     [!code-vb[Trin_VstcoreHostControlsExcel#5](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#5)]

## <a name="runtimeaddin"></a>VSTO eklenti projesindeki NamedRange denetimlerini çalışma zamanında yeniden boyutlandırma
 Çalışma zamanında herhangi bir <xref:Microsoft.Office.Tools.Excel.NamedRange> açık çalışma sayfasında bir denetimi yeniden boyutlandırabilirsiniz. VSTO eklentisini kullanarak çalışma sayfasına <xref:Microsoft.Office.Tools.Excel.NamedRange> denetim ekleme hakkında daha fazla bilgi için bkz [. nasıl yapılır: Çalışma sayfalarına](../vsto/how-to-add-namedrange-controls-to-worksheets.md)NamedRange denetimleri ekleyin.

### <a name="to-resize-a-named-range-programmatically"></a>Adlandırılmış bir aralığı programlı olarak yeniden boyutlandırmak için

1. <xref:Microsoft.Office.Tools.Excel.NamedRange> **A1** hücresindebirdenetimoluşturun.`Sheet1`

     [!code-csharp[Trin_Excel_Dynamic_Controls#10](../vsto/codesnippet/CSharp/Trin_Excel_Dynamic_Controls/ThisAddIn.cs#10)]
     [!code-vb[Trin_Excel_Dynamic_Controls#10](../vsto/codesnippet/VisualBasic/Trin_Excel_Dynamic_Controls/ThisAddIn.vb#10)]

2. Adlandırılmış aralığı **B1**hücresini içerecek şekilde yeniden boyutlandırın.

     [!code-csharp[Trin_Excel_Dynamic_Controls#11](../vsto/codesnippet/CSharp/Trin_Excel_Dynamic_Controls/ThisAddIn.cs#11)]
     [!code-vb[Trin_Excel_Dynamic_Controls#11](../vsto/codesnippet/VisualBasic/Trin_Excel_Dynamic_Controls/ThisAddIn.vb#11)]

## <a name="see-also"></a>Ayrıca bkz.
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [NamedRange denetimi](../vsto/namedrange-control.md)
- [Nasıl yapılır: Çalışma sayfalarına NamedRange denetimleri ekleme](../vsto/how-to-add-namedrange-controls-to-worksheets.md)
- [Nasıl yapılır: Yer Işareti denetimlerini yeniden boyutlandır](../vsto/how-to-resize-bookmark-controls.md)
- [Nasıl yapılır: ListObject denetimlerini yeniden boyutlandır](../vsto/how-to-resize-listobject-controls.md)
