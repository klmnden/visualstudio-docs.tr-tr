---
title: 'Nasıl yapılır: ListObject denetimlerini yeniden boyutlandır'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- controls [Office development in Visual Studio], resizing
- ListObject control, resizing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: d7dac99088dc57b538f7a26ffbd0bdc0e3e05b5a
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71252124"
---
# <a name="how-to-resize-listobject-controls"></a>Nasıl yapılır: ListObject denetimlerini yeniden boyutlandır
  Bir <xref:Microsoft.Office.Tools.Excel.ListObject> denetimin boyutunu Microsoft Office bir Excel çalışma kitabına eklediğinizde ayarlarsınız; ancak, daha sonra yeniden boyutlandırmak isteyebilirsiniz. Örneğin, iki sütunlu bir listeyi üç sütun olarak değiştirmek isteyebilirsiniz.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Tasarım zamanında veya <xref:Microsoft.Office.Tools.Excel.ListObject> çalışma zamanında denetimleri belge düzeyi projelerde yeniden boyutlandırabilirsiniz. Çalışma zamanında, <xref:Microsoft.Office.Tools.Excel.ListObject> bir VSTO eklenti projesindeki denetimleri yeniden boyutlandırabilirsiniz.

 Bu konuda aşağıdaki görevler açıklanmaktadır:

- [Tasarım zamanında ListObject denetimlerini yeniden boyutlandır](#designtime)

- [Belge düzeyindeki bir projede, çalışma zamanında ListObject denetimlerini yeniden boyutlandırma](#runtimedoclevel)

- [VSTO eklenti projesindeki ListObject denetimlerini çalışma zamanında yeniden boyutlandırma](#runtimeaddin)

  Denetimler hakkında <xref:Microsoft.Office.Tools.Excel.ListObject> daha fazla bilgi için bkz. [ListObject denetimi](../vsto/listobject-control.md).

  ![video bağlantısı](../vsto/media/playvideo.gif "video bağlantısı") İlgili video gösterimi için bkz [. nasıl yaparım?: Çalışma zamanında veriye dayalı bir liste nesnesine sütunlar eklensin mi? ](http://go.microsoft.com/fwlink/?LinkID=130318).

## <a name="designtime"></a>Tasarım zamanında ListObject denetimini yeniden boyutlandırma
 Bir listeyi yeniden boyutlandırmak için, boyutlandırma tutamaçlarından birini tıklatabilir ve sürükleyebilirsiniz ya da **Listeyi yeniden boyutlandır** iletişim kutusunda boyutunu yeniden tanımlayabilirsiniz.

### <a name="to-resize-a-list-by-using-the-resize-list-dialog-box"></a>Listeyi yeniden boyutlandır iletişim kutusunu kullanarak bir listeyi yeniden boyutlandırmak için

1. <xref:Microsoft.Office.Tools.Excel.ListObject> Tabloda herhangi bir yere tıklayın. Şeritteki **Tablo Araçları** > **Tasarım** sekmesi görüntülenir.

2. Özellikler bölümünde, **tabloyu yeniden boyutlandır**' ı tıklatın.

    ![VSTO_ResizeTable](../vsto/media/vsto-resizetable.png)

3. Tablonuz için yeni veri aralığını seçin.

4. **Tamam**'ı tıklatın.

## <a name="runtimedoclevel"></a>Belge düzeyindeki bir projede bir ListObject denetimini çalışma zamanında yeniden boyutlandırma
 Yöntemini kullanarak çalışma zamanında <xref:Microsoft.Office.Tools.Excel.ListObject> bir denetimi yeniden boyutlandırabilirsiniz. <xref:Microsoft.Office.Tools.Excel.ListObject.Resize%2A> Bu yöntemi, <xref:Microsoft.Office.Tools.Excel.ListObject> denetimi çalışma sayfasındaki yeni bir konuma taşımak için kullanamazsınız. Üst bilgiler aynı satırda kalmalıdır ve yeniden boyutlandırılmış <xref:Microsoft.Office.Tools.Excel.ListObject> denetim özgün liste nesnesiyle çakışmalıdır. Yeniden boyutlandırılmış <xref:Microsoft.Office.Tools.Excel.ListObject> denetim bir başlık satırı ve en az bir veri satırı içermelidir.

### <a name="to-resize-a-list-object-programmatically"></a>Bir liste nesnesini programlı olarak yeniden boyutlandırmak için

1. **A1** hücresini <xref:Microsoft.Office.Tools.Excel.ListObject> B3`Sheet1`üzerinden kapsayan bir denetim oluşturun.

     [!code-csharp[Trin_VstcoreHostControlsExcel#6](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#6)]
     [!code-vb[Trin_VstcoreHostControlsExcel#6](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#6)]

2. Listeyi, **a1** ile **C5**arasındaki hücreleri içerecek şekilde yeniden boyutlandırın.

     [!code-csharp[Trin_VstcoreHostControlsExcel#7](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#7)]
     [!code-vb[Trin_VstcoreHostControlsExcel#7](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#7)]

## <a name="runtimeaddin"></a>VSTO eklenti projesindeki bir ListObject 'i çalışma zamanında yeniden boyutlandırma
 Çalışma zamanında herhangi bir <xref:Microsoft.Office.Tools.Excel.ListObject> açık çalışma sayfasında bir denetimi yeniden boyutlandırabilirsiniz. VSTO eklentisini kullanarak çalışma sayfasına <xref:Microsoft.Office.Tools.Excel.ListObject> denetim ekleme hakkında daha fazla bilgi için bkz [. nasıl yapılır: Çalışma sayfalarına](../vsto/how-to-add-listobject-controls-to-worksheets.md)ListObject denetimleri ekleyin.

### <a name="to-resize-a-list-object-programmatically"></a>Bir liste nesnesini programlı olarak yeniden boyutlandırmak için

1. **A1** hücresini <xref:Microsoft.Office.Tools.Excel.ListObject> B3`Sheet1`üzerinden kapsayan bir denetim oluşturun.

     [!code-csharp[Trin_Excel_Dynamic_Controls#12](../vsto/codesnippet/CSharp/Trin_Excel_Dynamic_Controls/ThisAddIn.cs#12)]
     [!code-vb[Trin_Excel_Dynamic_Controls#12](../vsto/codesnippet/VisualBasic/Trin_Excel_Dynamic_Controls/ThisAddIn.vb#12)]

2. Listeyi, **a1** ile **C5**arasındaki hücreleri içerecek şekilde yeniden boyutlandırın.

     [!code-csharp[Trin_Excel_Dynamic_Controls#13](../vsto/codesnippet/CSharp/Trin_Excel_Dynamic_Controls/ThisAddIn.cs#13)]
     [!code-vb[Trin_Excel_Dynamic_Controls#13](../vsto/codesnippet/VisualBasic/Trin_Excel_Dynamic_Controls/ThisAddIn.vb#13)]

## <a name="see-also"></a>Ayrıca bkz.
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [ListObject denetimi](../vsto/listobject-control.md)
- [Nasıl yapılır: Çalışma sayfalarına ListObject denetimleri ekleme](../vsto/how-to-add-listobject-controls-to-worksheets.md)
- [Nasıl yapılır: Yer Işareti denetimlerini yeniden boyutlandır](../vsto/how-to-resize-bookmark-controls.md)
- [Nasıl yapılır: NamedRange denetimlerini yeniden boyutlandır](../vsto/how-to-resize-namedrange-controls.md)
