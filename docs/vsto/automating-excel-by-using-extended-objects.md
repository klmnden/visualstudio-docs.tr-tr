---
title: Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Excel [Office development in Visual Studio], automating
- automation [Office development in Visual Studio], Excel
- host controls, Excel
- Excel [Office development in Visual Studio], host controls
- extended objects [Office development in Visual Studio], Excel
- host controls [Office development in Visual Studio], Excel
- automating Excel
- host items [Office development in Visual Studio], Excel
- controls [Office development in Visual Studio], Excel host controls
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a8a08b58871652cea6332f4239e9da98b28f28e0
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60070062"
---
# <a name="automate-excel-by-using-extended-objects"></a>Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek
  Visual Studio'daki Excel çözümleri geliştirirken kullanabileceğiniz *konak öğelerini* ve *konak kontrolü*Çözümlerinizdeki s. Bunlar gibi Excel nesne modeli (Excel için birincil birlikte çalışma derlemesi tarafından sunulan diğer bir deyişle, nesne modeli) yaygın olarak kullanılan belirli nesneleri genişleten nesnelerdir <xref:Microsoft.Office.Interop.Excel.Worksheet> ve <xref:Microsoft.Office.Interop.Excel.Range> nesneleri. Genişletilmiş nesneler temel Excel nesneleri gibi davranırlar, ancak bunlar yeni olaylar ve veri bağlama becerileri gibi ek özellikler sahiptirler.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Konak denetimlerinin ve konak öğelerinin her iki VSTO eklenti kullanılabilir ve belge düzeyi özelleştirmeleri, bu kullanılabilir içeriği her çözüm türü için farklı olmasına karşın. Daha fazla bilgi için [konak öğelerini ve denetimlerine genel bakış için ana bilgisayar](../vsto/host-items-and-host-controls-overview.md).

## <a name="excel-host-items"></a>Excel konak öğeleri
 Excel projeleri için birden fazla konak öğeleri erişmenizi sağlar:

- <xref:Microsoft.Office.Tools.Excel.Worksheet>. Bu konak öğesi içerir ve projenizdeki çalışma temsil eder. Ayrıca konak denetimleri ve Windows Forms denetimleri de dahil olmak üzere yönetilen denetimler için kapsayıcı olarak davranır ve yüzeyinde denetimler hakkında bilgi içerir. Daha fazla bilgi için [çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md).

- <xref:Microsoft.Office.Tools.Excel.Workbook>. Bu konak öğesi, projenizdeki çalışma kitabı temsil eder ve kitabındaki tüm çalışma sayfalarını tarafından paylaşılan bileşenleri için kapsayıcı işlevi görür. Daha fazla bilgi için [çalışma kitabı konak öğesi](../vsto/workbook-host-item.md).

- <xref:Microsoft.Office.Tools.Excel.ChartSheet>. Bu konak, yalnızca bir grafik içeren ve olayları ortaya koyan bir Excel çalışma sayfasındaki öğe.

     Grafik sayfası Tasarım zamanında yeni bir sayfa olarak Microsoft Office Excel belge düzeyi özelleştirmesi projenizde eklediğinizde, Visual Studio otomatik olarak oluşturur bir <xref:Microsoft.Office.Tools.Excel.ChartSheet> konak öğesi.

     Ancak bir <xref:Microsoft.Office.Tools.Excel.ChartSheet> konak öğesi bir Excel çalışma sayfasında, herhangi bir denetim için grafik sayfası eklenemiyor. Bir çalışma sayfası bir grafik ile diğer denetimler istiyorsanız, bir grafik sayfası kullanmayın. Bunun yerine, bir grafik çalışma sayfasındaki katıştırılmış nesne olarak kullanarak yerleştirebilirsiniz <xref:Microsoft.Office.Tools.Excel.Chart> konak kontrolü. Daha fazla bilgi için [grafik denetimi](../vsto/chart-control.md).

## <a name="excel-host-controls"></a>Excel konak denetimleri
 Yardımcı olan denetimler için Excel oluşturmak, düzenlemek ve otomatikleştirmek çalışma kitaplarını ve çalışma birden çok konak vardır. Bu konak denetimleri, olayları ve yerel Excel nesne modelinde karşılıkları olmayan veri bağlama özellikleri sağlar.

 Excel projelerinde kullanabileceğiniz konak denetimleri hakkında daha fazla bilgi için aşağıdaki konulara bakın:

- [Grafik denetimi](../vsto/chart-control.md)

- [ListObject denetimi](../vsto/listobject-control.md)

- [NamedRange denetimi](../vsto/namedrange-control.md)

- [XmlMappedRange denetimi](../vsto/xmlmappedrange-control.md)

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: ListObject denetimlerini veri ile doldurabilirsiniz.](../vsto/how-to-fill-listobject-controls-with-data.md)
- [Nasıl yapılır: Çalışma sayfalarına Grafik denetimleri ekleme](../vsto/how-to-add-chart-controls-to-worksheets.md)
- [Nasıl yapılır: Çalışma sayfalarına ListObject denetimleri ekleme](../vsto/how-to-add-listobject-controls-to-worksheets.md)
- [Nasıl yapılır: Çalışma sayfalarına NamedRange denetimleri ekleme](../vsto/how-to-add-namedrange-controls-to-worksheets.md)
- [Nasıl yapılır: Çalışma sayfalarına XMLMappedRange denetimleri ekleme](../vsto/how-to-add-xmlmappedrange-controls-to-worksheets.md)
- [Nasıl yapılır: NamedRange denetimlerinin boyutunu değiştirme](../vsto/how-to-resize-namedrange-controls.md)
- [Nasıl yapılır: ListObject denetimlerinin boyutunu değiştirme](../vsto/how-to-resize-listobject-controls.md)
- [Nasıl yapılır: ListObject denetimine yeni bir satır eklendiğinde verileri doğrulama](../vsto/how-to-validate-data-when-a-new-row-is-added-to-a-listobject-control.md)
- [Nasıl yapılır: ListObject sütunlarıyla verileri eşleme](../vsto/how-to-map-listobject-columns-to-data.md)
- [İzlenecek yol: NamedRange denetimi olaylarına karşı programlama](../vsto/walkthrough-programming-against-events-of-a-namedrange-control.md)
- [Word belgelerini ve Excel çalışma kitaplarını VSTO eklentileri çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
