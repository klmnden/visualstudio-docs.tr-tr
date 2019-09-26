---
title: Çalışma sayfası konak öğesi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- host items [Office development in Visual Studio], Worksheet
- Excel [Office development in Visual Studio], worksheets
- Worksheet host items
- worksheets, events
- Worksheet host items, events
- Excel worksheets
- worksheets, Excel
- worksheets
- events [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 301b0a62efae4674432b1051451e5d982899c1b3
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71254879"
---
# <a name="worksheet-host-item"></a>Çalışma sayfası konak öğesi
  Konak öğesi, Excel için birincil birlikte çalışma derlemesinden <xref:Microsoft.Office.Interop.Excel.Worksheet> türü genişleten bir türdür. <xref:Microsoft.Office.Tools.Excel.Worksheet> Konak öğesi, aynı özellikleri, yöntemleri ve olayları bir <xref:Microsoft.Office.Interop.Excel.Worksheet> nesne olarak sağlar, ancak ayrıca ek olaylar sunar ve konak denetimleri ve Windows Forms denetimleri için bir kapsayıcı görevi görür. <xref:Microsoft.Office.Tools.Excel.Worksheet>

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Belge düzeyi projelerinde, tasarım zamanında projenize ana bilgisayar <xref:Microsoft.Office.Tools.Excel.Worksheet> öğeleri ekleyebilirsiniz. VSTO eklenti projelerinde, <xref:Microsoft.Office.Tools.Excel.Worksheet> çalışma zamanında konak öğeleri oluşturabilirsiniz.

## <a name="understand-worksheet-host-items-in-document-level-projects"></a>Belge düzeyi projelerdeki çalışma sayfası konak öğelerini anlama
 Excel için belge düzeyi projesi oluşturduğunuzda, Visual Studio otomatik olarak projede üç <xref:Microsoft.Office.Tools.Excel.Worksheet> konak öğesi oluşturur. Çalışma sayfalarının varsayılan adları, `Sheet1` `Sheet2`ve `Sheet3`' dir. Var olan bir çalışma kitabını temel alan bir proje oluşturursanız, konak öğelerinin sayısı çalışma kitabındaki çalışma sayfası sayısına bağlıdır.

 Bu çalışma sayfası sınıfları, özelleştirmenizin çalışma sayfasının içeriğini <xref:Microsoft.Office.Tools.Excel.Worksheet> değiştirme gibi temel görevleri yerine getirmek için konak öğesi üyelerine erişmenizi sağlar. Ayrıca, çalışma sayfalarına denetim eklemek için bu sınıfları kullanabilirsiniz. Farklı denetim kümelerini birleştirerek ve kod yazarken, denetimleri verilere bağlayabilir, kullanıcıdan bilgi toplayabilir ve kullanıcı eylemlerine yanıt verebilirsiniz. Daha fazla bilgi için bkz. [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md).

 Çalışma sayfası sınıfları, projenizde kod yazmaya başlayabilmeniz için bir konum sağlar. Sınıfı, Excel için birincil birlikte çalışma derlemesindeki <xref:Microsoft.Office.Interop.Excel.Worksheet> nesne olarak aynı özellikleri, yöntemleri ve olayları sağladığından, Excel 'in nesne modeline erişmek için de bu sınıfları kullanabilirsiniz. Daha fazla bilgi için [Excel nesne modeline genel bakış](../vsto/excel-object-model-overview.md).

 Belge düzeyi projelerinde, Tasarımcıda çalışma kitabına yeni bir çalışma <xref:Microsoft.Office.Tools.Excel.Worksheet> sayfası ekleyerek, tasarım zamanında projeye ek konak öğeleri ekleyebilirsiniz.

### <a name="rename-worksheets"></a>Çalışma sayfalarını yeniden adlandırma
 Belge düzeyi projesinde, Visual Studio tasarımcısında çalışma sayfalarını yeniden adlandırabilirsiniz, ancak bu yalnızca çalışma sayfasının görünen adını değiştirir. Programlı ad, hala çalışma sayfasının varsayılan adıdır. Çalışma sayfasını **Özellikler** penceresinde yeniden adlandırırsanız yalnızca programlı ad değiştirilir.

### <a name="limitations-of-the-worksheet-host-item-in-document-level-projects"></a>Belge düzeyi projelerdeki çalışma sayfası konak öğesi sınırlamaları
 Belge düzeyindeki bir projede <xref:Microsoft.Office.Tools.Excel.Worksheet> çalışma zamanında yeni konak öğeleri oluşturamazsınız. Çalışma zamanında yeni bir Excel çalışma sayfası oluşturursanız, bu, türü <xref:Microsoft.Office.Interop.Excel.Worksheet>olacaktır. Konak öğesi olmadığından, hiçbir konak denetimi veya Windows Forms denetimi içeremez. Çalışma zamanında belge oluşturma hakkında daha fazla bilgi için bkz [. nasıl yapılır: Çalışma kitaplarına](../vsto/how-to-programmatically-add-new-worksheets-to-workbooks.md)program aracılığıyla yeni çalışma sayfaları ekleyin.

## <a name="understand-worksheet-host-items-in-vsto-add-in-projects"></a>VSTO eklenti projelerinde çalışma sayfası konak öğelerini anlama
 Uygulama düzeyi projelerinde, Excel 'de açık olan herhangi bir <xref:Microsoft.Office.Tools.Excel.Worksheet> çalışma sayfası için çalışma zamanında bir konak öğesi oluşturabilirsiniz. İlişkili çalışma sayfasına denetim <xref:Microsoft.Office.Tools.Excel.Worksheet> eklemek veya <xref:Microsoft.Office.Interop.Excel.Worksheet> nesnelerde kullanılamayan olayları işlemek için konak öğesini kullanabilirsiniz.

 Bir <xref:Microsoft.Office.Tools.Excel.Worksheet> konak öğesi oluşturmak için `GetVstoObject` yöntemini kullanın. Daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Çalışma kitabı konak öğesi](../vsto/workbook-host-item.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
