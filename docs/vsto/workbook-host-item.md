---
title: Çalışma kitabı konak öğesi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Excel workbooks
- Workbook host items
- host items [Office development in Visual Studio], Workbook
- workbooks, Excel
- Workbook host items, events
- workbooks
- Excel [Office development in Visual Studio], workbooks
- workbooks, events
- events [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 797f1a55ec7632114e411bf0ba08e7f4e0cc146e
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255078"
---
# <a name="workbook-host-item"></a>Çalışma kitabı konak öğesi
  Konak öğesi, Excel için birincil birlikte çalışma derlemesinden <xref:Microsoft.Office.Interop.Excel.Workbook> türü genişleten bir türdür. <xref:Microsoft.Office.Tools.Excel.Workbook> Konak öğesi, aynı özellikleri, yöntemleri ve olayları bir <xref:Microsoft.Office.Interop.Excel.Workbook> nesne olarak sağlar, ancak ek özellikler de sağlar. <xref:Microsoft.Office.Tools.Excel.Workbook>

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Belge düzeyi projelerinde, projenizdeki çalışma kitabını temsil eden bir <xref:Microsoft.Office.Tools.Excel.Workbook> varsayılan konak öğesi vardır. VSTO eklenti projelerinde, <xref:Microsoft.Office.Tools.Excel.Workbook> çalışma zamanında konak öğeleri oluşturabilirsiniz.

## <a name="understand-the-workbook-host-item-in-document-level-projects"></a>Belge düzeyi projelerdeki çalışma kitabı konak öğesini anlayın
 Projenizdeki çalışma kitabına erişmek için `ThisWorkbook` sınıfını kullanın. Sınıfı, özelleştirmeinizdeki temel görevleri <xref:Microsoft.Office.Tools.Excel.Workbook> (çalışma kitabı açıldığında veya kapandığında kodu çalıştırmak gibi) gerçekleştirmek için konak öğesinin üyelerine erişmenizi sağlar. `ThisWorkbook` Daha fazla bilgi için bkz. [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md).

 Sınıfı `ThisWorkbook` , projenizde kod yazmaya başlayabilmeniz için bir konum sağlar. Sınıfı, Excel için birincil birlikte çalışma derlemesindeki <xref:Microsoft.Office.Interop.Excel.Workbook> nesne olarak aynı özellikleri, yöntemleri ve olayları sağladığından Excel 'in nesne modeline erişmek için de kullanabilirsiniz. `ThisWorkbook` Daha fazla bilgi için [Excel nesne modeline genel bakış](../vsto/excel-object-model-overview.md).

 Çalışma kitabı tasarımcısını görüntülemek ve **Özellikler** penceresinde çalışma kitabının özelliklerini ve olaylarını görüntülemek için **Çözüm Gezgini** içindeki **ThisWorkbook** proje öğesine çift tıklayın.

### <a name="limitations-of-the-workbook-host-item-in-document-level-projects"></a>Belge düzeyi projelerdeki çalışma kitabı konak öğesi sınırlamaları
 Belge düzeyindeki bir proje yalnızca bir <xref:Microsoft.Office.Tools.Excel.Workbook> konak öğesi (yani `ThisWorkbook` , sınıfı) içerebilir. Tasarım zamanında projenize yeni <xref:Microsoft.Office.Tools.Excel.Workbook> konak öğeleri ekleyemez ve çalışma zamanında belge düzeyi özelleştirmesindeki yeni <xref:Microsoft.Office.Tools.Excel.Workbook> konak öğeleri oluşturamazsınız.

 Çalışma zamanında yeni bir Excel çalışma kitabı oluşturursanız, bu, türü <xref:Microsoft.Office.Interop.Excel.Workbook>olacaktır. Konak öğesi olmadığından, hiçbir konak denetimi veya Windows Forms denetimi içeremez. Çalışma zamanında çalışma kitapları oluşturma hakkında daha fazla bilgi için bkz [. nasıl yapılır: Program aracılığıyla yeni çalışma](../vsto/how-to-programmatically-create-new-workbooks.md)kitapları oluşturma.

 <xref:Microsoft.Office.Tools.Excel.Workbook> Konak öğesi konak denetimleri için bir kapsayıcı görevi yapmaz. Bu nedenle, çalışma kitabına görünür denetimleri ekleyemezsiniz, ancak bileşenlerin tüm çalışma sayfaları tarafından paylaşılabilmesi için gibi bileşenler <xref:System.Data.DataSet>ekleyebilirsiniz. Belge düzeyindeki bir projede, çalışma kitabı için kullanılabilen bileşenler **bileşen** sekmesi, **veri** sekmesi ve **araç kutusunun** **tüm Windows Forms** sekmelerinde bulunabilir.

> [!NOTE]
> Visual Studio 'da Office geliştirme araçları paylaşılan çalışma kitaplarını desteklemez.

## <a name="understand-workbook-host-items-in-vsto-add-in-projects"></a>VSTO eklenti projelerinde çalışma kitabı konak öğelerini anlama
 VSTO eklenti projelerinde, Excel 'de açık olan herhangi bir çalışma <xref:Microsoft.Office.Tools.Excel.Workbook> kitabı için çalışma zamanında bir konak öğesi oluşturabilirsiniz. Bir <xref:Microsoft.Office.Tools.Excel.Workbook> konak öğesi oluşturmak için `GetVstoObject` yöntemini kullanın. Daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
