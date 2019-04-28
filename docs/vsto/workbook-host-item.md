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
ms.openlocfilehash: e30ab9ce498134426caa35e0c3c9f9652f683535
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63445536"
---
# <a name="workbook-host-item"></a>Çalışma kitabı konak öğesi
  <xref:Microsoft.Office.Tools.Excel.Workbook> Konak öğesi olan bir türü genişleten <xref:Microsoft.Office.Interop.Excel.Workbook> Excel için birincil birlikte çalışma bütünleştirilmiş koddan tür. <xref:Microsoft.Office.Tools.Excel.Workbook> Konak öğesi tüm özellikleri, yöntemleri ve olayları olarak sağlayan bir <xref:Microsoft.Office.Interop.Excel.Workbook> nesne, ancak ayrıca ek özellikler sağlar.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Belge düzeyinde projelerde bir varsayılan yok <xref:Microsoft.Office.Tools.Excel.Workbook> temsil eder, projenizdeki çalışma kitabı konak öğesi. VSTO eklentisi projelerinde oluşturabileceğiniz <xref:Microsoft.Office.Tools.Excel.Workbook> öğelerinin çalışma zamanında barındırın.

## <a name="understand-the-workbook-host-item-in-document-level-projects"></a>Belge düzeyinde projelerde çalışma kitabı konak öğesi anlama
 Çalışma kitabı, projenizdeki erişmek için `ThisWorkbook` sınıfı. `ThisWorkbook` Sınıf üyelerine erişim sağlar <xref:Microsoft.Office.Tools.Excel.Workbook> özelleştirme, çalışma kitabı açılamıyor veya kod çalıştırma gibi temel görevleri gerçekleştirmek için konak öğesi. Daha fazla bilgi için [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md).

 `ThisWorkbook` Sınıfı başlangıç projenizde kod yazma bir konum sağlar. Sınıfı, tüm özellikleri, yöntemleri ve olayları olarak sağladığından <xref:Microsoft.Office.Interop.Excel.Workbook> nesne birincil birlikte çalışma derlemesi Excel için de kullanabilirsiniz `ThisWorkbook` Excel nesne modeline erişim. Daha fazla bilgi için [Excel nesne modeline genel bakış](../vsto/excel-object-model-overview.md).

 Çift **ThisWorkbook** içinde proje öğesi **Çözüm Gezgini** çalışma kitabı Tasarımcısı'nı görüntüleyin ve çalışma kitabında olayları ve özellikleri görüntülemek için **özellikleri**penceresi.

### <a name="limitations-of-the-workbook-host-item-in-document-level-projects"></a>Belge düzeyinde projelerde çalışma kitabı konak öğesi sınırlamaları
 Tek bir belge düzeyi projesi içerebilir <xref:Microsoft.Office.Tools.Excel.Workbook> konak öğesi (diğer bir deyişle, `ThisWorkbook` sınıfı). Yeni eklenemiyor <xref:Microsoft.Office.Tools.Excel.Workbook> konak öğeleri projenize tasarım zamanında ve yeni oluşturamazsınız <xref:Microsoft.Office.Tools.Excel.Workbook> konak öğelerini bir belge düzeyi özelleştirmesinde zamanında.

 Çalışma zamanında yeni bir Excel çalışma kitabı oluşturursanız, bu tür olacaktır <xref:Microsoft.Office.Interop.Excel.Workbook>. Bir konak öğesi olmadığı için tüm konak veya Windows Forms denetimleri içeremez. Çalışma kitaplarını çalışma zamanında oluşturma hakkında daha fazla bilgi için bkz. [nasıl yapılır: Program aracılığıyla yeni çalışma kitaplarını](../vsto/how-to-programmatically-create-new-workbooks.md).

 <xref:Microsoft.Office.Tools.Excel.Workbook> Konak denetimler için kapsayıcı olarak ana bilgisayar öğesi davranmaz. Bu nedenle, çalışma kitabına görünür bir denetim ekleyemezsiniz, ancak bileşenler gibi ekleyebilirsiniz bir <xref:System.Data.DataSet>, böylece bileşenlerin tüm çalışma sayfalarını tarafından paylaşılabilir. Bir belge düzeyi projede çalışma kitabına kullanılabilir bileşenler bulunabilir **bileşen** sekmesinde **veri** sekmesinde ve **tüm Windows Formları** sekmesinde  **Araç kutusu**.

> [!NOTE]
> Visual Studio'da Office geliştirme araçları, paylaşılan çalışma kitapları desteklemez.

## <a name="understand-workbook-host-items-in-vsto-add-in-projects"></a>VSTO eklentisi projelerinde çalışma kitabı konak öğeleri anlama
 VSTO eklentisi projelerinde oluşturabileceğiniz bir <xref:Microsoft.Office.Tools.Excel.Workbook> Excel'de herhangi bir çalışma kitabında çalışma zamanında konak öğesi. Oluşturulacak bir <xref:Microsoft.Office.Tools.Excel.Workbook> konak öğesi, kullanım `GetVstoObject` yöntemi. Daha fazla bilgi için [genişletmek Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında VSTO Add-Ins](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
- [Word belgelerini ve Excel çalışma kitaplarını VSTO eklentileri çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
