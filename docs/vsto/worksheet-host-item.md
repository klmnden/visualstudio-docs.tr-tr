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
ms.openlocfilehash: e4a5287648d515d1aca340ab55d5f21b494610b5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62814737"
---
# <a name="worksheet-host-item"></a>Çalışma sayfası konak öğesi
  <xref:Microsoft.Office.Tools.Excel.Worksheet> Konak öğesi olan bir türü genişleten <xref:Microsoft.Office.Interop.Excel.Worksheet> Excel için birincil birlikte çalışma bütünleştirilmiş koddan tür. <xref:Microsoft.Office.Tools.Excel.Worksheet> Konak öğesi tüm özellikleri, yöntemleri ve olayları olarak sağlayan bir <xref:Microsoft.Office.Interop.Excel.Worksheet> nesne, ancak ayrıca ek olayları ortaya koyan ve konak denetimleri ve Windows Forms denetimleri için kapsayıcı işlevi görür.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Belge düzeyinde projelerde eklediğiniz <xref:Microsoft.Office.Tools.Excel.Worksheet> konak öğeleri projenize tasarım zamanında. VSTO eklentisi projelerinde oluşturabileceğiniz <xref:Microsoft.Office.Tools.Excel.Worksheet> öğelerinin çalışma zamanında barındırın.

## <a name="understand-worksheet-host-items-in-document-level-projects"></a>Belge düzeyinde projelerde çalışma sayfası konak öğeleri anlama
 Excel için belge düzeyi projesi oluşturduğunuzda, Visual Studio otomatik olarak üç oluşturur <xref:Microsoft.Office.Tools.Excel.Worksheet> ana proje öğeleri. Varsayılan çalışma adlarıdır `Sheet1`, `Sheet2`, ve `Sheet3`. Mevcut bir çalışma kitabını temel alan bir proje oluşturursanız, ana öğe sayısını çalışma kitabındaki sayısına bağlıdır.

 Bu çalışma sayfası sınıflarından üyelerine erişim verin <xref:Microsoft.Office.Tools.Excel.Worksheet> özelleştirme, bir çalışma kitabının içeriğini değiştirme gibi temel görevleri gerçekleştirmek için konak öğesi. Bu sınıflar, denetimleri ekleme için de kullanabilirsiniz. Farklı denetim kümelerini birleştirerek ve verilere denetimler bağlayabilirsiniz kod yazarken, kullanıcıdan bilgi toplamak ve kullanıcı eylemlerine yanıt. Daha fazla bilgi için [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md).

 Çalışma sayfası sınıflarından, projenizde kod yazmaya başlayabilirsiniz bir konum sağlayın. Sınıfı, tüm özellikleri, yöntemleri ve olayları olarak sağladığından <xref:Microsoft.Office.Interop.Excel.Worksheet> nesne birincil birlikte çalışma derlemesi için Excel, ayrıca bu sınıfların Excel nesne modeline erişme için kullanabilirsiniz. Daha fazla bilgi için [Excel nesne modeline genel bakış](../vsto/excel-object-model-overview.md).

 Belge düzeyinde projelerde ek ekleyebilirsiniz <xref:Microsoft.Office.Tools.Excel.Worksheet> konak proje öğelerine tasarım zamanında çalışma kitabını tasarımcıda yeni çalışma ekleyerek.

### <a name="rename-worksheets"></a>Çalışma sayfaları yeniden adlandır
 Bir belge düzeyi projede, Visual Studio tasarımcısı çalışma sayfaları yeniden adlandırabilirsiniz, ancak bu yalnızca çalışma görünen adını değiştirir. Programlı ad hala çalışma sayfasının varsayılan addır. Çalışma sayfasına yeniden adlandırırsanız **özellikleri** pencere, yalnızca bir programlı ad değiştirilir.

### <a name="limitations-of-the-worksheet-host-item-in-document-level-projects"></a>Belge düzeyinde projelerde çalışma sayfası konak öğesi sınırlamaları
 Yeni oluşturulamıyor <xref:Microsoft.Office.Tools.Excel.Worksheet> konak öğelerini bir belge düzeyi projesi çalışma zamanında. Yeni bir Excel çalışma zamanında oluşturursanız, bu türü olacaktır <xref:Microsoft.Office.Interop.Excel.Worksheet>. Bir konak öğesi olmadığı için tüm konak veya Windows Forms denetimleri içeremez. Çalışma zamanında belgeler oluşturma hakkında daha fazla bilgi için bkz. [nasıl yapılır: Program aracılığıyla yeni çalışma kitaplarına ekleme](../vsto/how-to-programmatically-add-new-worksheets-to-workbooks.md).

## <a name="understand-worksheet-host-items-in-vsto-add-in-projects"></a>VSTO eklentisi projelerinde çalışma sayfası konak öğeleri anlama
 Uygulama düzeyi projelere içinde oluşturduğunuz bir <xref:Microsoft.Office.Tools.Excel.Worksheet> Excel'de herhangi bir çalışma sayfası için çalışma zamanında konak öğesi. Kullanabileceğiniz <xref:Microsoft.Office.Tools.Excel.Worksheet> ilgili çalışma sayfasına denetimler ekleme ya da kullanılabilir olan olayları işlemek için ana bilgisayar öğesi <xref:Microsoft.Office.Interop.Excel.Worksheet> nesneleri.

 Oluşturulacak bir <xref:Microsoft.Office.Tools.Excel.Worksheet> konak öğesi, kullanım `GetVstoObject` yöntemi. Daha fazla bilgi için [genişletmek Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında VSTO Add-Ins](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
- [Word belgelerini ve Excel çalışma kitaplarını VSTO eklentileri çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Çalışma kitabı konak öğesi](../vsto/workbook-host-item.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
