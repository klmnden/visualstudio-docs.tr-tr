---
title: 'Nasıl yapılır: ListObject sütunlarını verilerle eşleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data [Office development in Visual Studio], mapping to ListObject column
- ListObject control, mapping data
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 6e0056687e8ca28af4dbc9032d7bbee0cf976378
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253679"
---
# <a name="how-to-map-listobject-columns-to-data"></a>Nasıl yapılır: ListObject sütunlarını verilerle eşleme
  Bir <xref:Microsoft.Office.Tools.Excel.ListObject> denetimi<xref:System.Data.DataTable>öğesine bağladığınızda, bir listedeki tüm sütunları göstermek istemeyebilirsiniz veya verilere bağlı olmayan belirli sütunlara sahip olabilirsiniz. Yöntemini çağırdığınızda içinde <xref:Microsoft.Office.Tools.Excel.ListObject> görünmesini istediğiniz sütunları eşleyebilirsiniz. <xref:Microsoft.Office.Tools.Excel.ListObject.SetDataBinding%2A>

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 ![video bağlantısı](../vsto/media/playvideo.gif "video bağlantısı") İlgili video gösterimi için bkz [. nasıl yaparım?: Excel 'de SharePoint listesine bağlı bir liste oluşturun mi? ](http://go.microsoft.com/fwlink/?LinkID=130263).

## <a name="map-columns"></a>Harita sütunları

### <a name="to-map-a-data-table-to-columns-in-a-list"></a>Bir veri tablosunu bir listedeki sütunlarla eşlemek için

1. <xref:System.Data.DataTable> Sınıf düzeyinde oluşturun.

     [!code-csharp[Trin_VstcoreHostControlsExcel#16](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet3.cs#16)]
     [!code-vb[Trin_VstcoreHostControlsExcel#16](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet3.vb#16)]

2. Sınıfın (belge düzeyi projesinde) veya `Startup` `ThisAddIn` sınıfında (VSTO eklenti projesindeki) olay işleyicisine örnek sütun ve veri ekleyin. `Sheet1`

     [!code-csharp[Trin_VstcoreHostControlsExcel#17](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet3.cs#17)]
     [!code-vb[Trin_VstcoreHostControlsExcel#17](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet3.vb#17)]

3. <xref:Microsoft.Office.Tools.Excel.ListObject.SetDataBinding%2A> Yöntemi çağırın ve sütun adlarını görünmesi gereken sırada geçirin. Liste nesnesi yeni oluşturulan <xref:System.Data.DataTable>' e bağlanacak, ancak liste nesnesindeki sütunların sırası <xref:System.Data.DataTable>içinde göründükleri sırada farklılık gösterir.

     [!code-csharp[Trin_VstcoreHostControlsExcel#18](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet3.cs#18)]
     [!code-vb[Trin_VstcoreHostControlsExcel#18](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet3.vb#18)]

## <a name="specify-unmapped-columns"></a>Eşlenmemiş sütunları belirt
 Sütunları bir <xref:System.Data.DataTable>ile eşleştirdiğinizde, belirli sütunların boş bir dizeye geçerek veriye bağlanmamalıdır. Veriye bağlanmamış yeni bir sütun daha sonra <xref:Microsoft.Office.Tools.Excel.ListObject> denetime eklenir.

### <a name="to-specify-an-unmapped-column-when-mapping-listobject-columns"></a>ListObject sütunlarını eşlerken eşlenmemiş bir sütun belirtmek için

1. <xref:Microsoft.Office.Tools.Excel.ListObject.SetDataBinding%2A> Yöntemi çağırın ve sütun adlarını görünmesi gereken sırada geçirin. Eşlenmemiş bir sütunun eklendiğini göstermek için boş bir dize kullanın; Bu durumda, başlık sütunu ve soyadı sütunu arasında.

     [!code-csharp[Trin_VstcoreHostControlsExcel#19](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet3.cs#19)]
     [!code-vb[Trin_VstcoreHostControlsExcel#19](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet3.vb#19)]

## <a name="compile-the-code"></a>Kod derleme
 Bu kod örneği, bu kodun göründüğü çalışma <xref:Microsoft.Office.Tools.Excel.ListObject> sayfasında `list1` var olan bir ada sahip olduğunuzu varsayar.

## <a name="see-also"></a>Ayrıca bkz.
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Nasıl yapılır: ListObject denetimlerini verilerle Doldur](../vsto/how-to-fill-listobject-controls-with-data.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [ListObject denetimi](../vsto/listobject-control.md)
