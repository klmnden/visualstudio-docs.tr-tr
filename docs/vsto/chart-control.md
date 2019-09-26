---
title: Grafik denetimi
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VST.ProjectItem.ExcelChart
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Chart control [Office development in Visual Studio], events
- Chart control [Office development in Visual Studio]
- Chart control [Office development in Visual Studio], data binding
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 864422aac695fbf474e6ed6b8cf6d765247eabf9
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255300"
---
# <a name="chart-control"></a>Grafik denetimi
  Denetim <xref:Microsoft.Office.Tools.Excel.Chart> , olayları ortaya çıkaran bir grafik nesnesidir. Bir çalışma sayfasına bir grafik eklediğinizde, Visual Studio Microsoft Office Excel nesne modelinde <xref:Microsoft.Office.Tools.Excel.Chart> geçiş yapmak zorunda kalmadan doğrudan programlama yapabileceğiniz bir nesne oluşturur.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="create-the-control"></a>Denetim oluşturma
 Tasarım zamanında Microsoft Office <xref:Microsoft.Office.Tools.Excel.Chart> Excel çalışma sayfasına veya belge düzeyindeki bir projede çalışma zamanında denetimler ekleyebilirsiniz.

 Bir çalışma sayfasına <xref:Microsoft.Office.Tools.Excel.Chart> bir VSTO eklentisinin çalışma zamanında denetim ekleyebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Çalışma sayfalarına](../vsto/how-to-add-chart-controls-to-worksheets.md)grafik denetimleri ekleyin.

> [!NOTE]
> Çalışma sayfası kapatıldığında dinamik olarak oluşturulan grafik nesneleri çalışma sayfasında konak denetimleri olarak kalıcı olmaz. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

## <a name="formatting"></a>Biçimlendirme
 Bir <xref:Microsoft.Office.Interop.Excel.Chart> <xref:Microsoft.Office.Tools.Excel.Chart> denetimine uygulanabilecek tüm biçimlendirmeler de bir denetime uygulanabilir. Bu, kenarlıkları, yazı tiplerini, grafik türünü, kılavuz çizgilerini, göstergeyi ve veri etiketlerini içerir.

## <a name="events"></a>Olaylar
 <xref:Microsoft.Office.Tools.Excel.Chart> Denetim için aşağıdaki olaylar mevcuttur:

- <xref:Microsoft.Office.Tools.Excel.Chart.ActivateEvent>

- <xref:Microsoft.Office.Tools.Excel.Chart.BeforeDoubleClick>

- <xref:Microsoft.Office.Tools.Excel.Chart.BeforeRightClick>

- <xref:Microsoft.Office.Tools.Excel.Chart.BindingContextChanged>

- <xref:Microsoft.Office.Tools.Excel.Chart.Calculate>

- <xref:Microsoft.Office.Tools.Excel.Chart.Deactivate>

- <xref:System.ComponentModel.Component.Disposed>

- <xref:Microsoft.Office.Tools.Excel.Chart.DragOver>

- <xref:Microsoft.Office.Tools.Excel.Chart.DragPlot>

- <xref:Microsoft.Office.Tools.Excel.Chart.MouseDown>

- <xref:Microsoft.Office.Tools.Excel.Chart.MouseMove>

- <xref:Microsoft.Office.Tools.Excel.Chart.MouseUp>

- <xref:Microsoft.Office.Tools.Excel.Chart.Resize>

- <xref:Microsoft.Office.Tools.Excel.Chart.SelectEvent>

- <xref:Microsoft.Office.Tools.Excel.Chart.SeriesChange>

## <a name="see-also"></a>Ayrıca bkz.
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Nasıl yapılır: Çalışma sayfalarına Grafik denetimleri ekleme](../vsto/how-to-add-chart-controls-to-worksheets.md)
- [Office çözümlerinde verileri denetimlere bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
