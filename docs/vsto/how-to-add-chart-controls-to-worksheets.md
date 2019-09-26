---
title: 'Nasıl yapılır: Çalışma sayfalarına Grafik denetimleri ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Chart control [Office development in Visual Studio], adding to worksheets
- controls [Office development in Visual Studio], adding to worksheets
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 80cc011cb9c2387b86e244f501fd5746ebb67535
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71254662"
---
# <a name="how-to-add-chart-controls-to-worksheets"></a>Nasıl yapılır: Çalışma sayfalarına Grafik denetimleri ekleme
  Tasarım zamanında Microsoft Office <xref:Microsoft.Office.Tools.Excel.Chart> Excel çalışma sayfasına ve belge düzeyi özelleştirmelerde çalışma zamanında denetim ekleyebilirsiniz. Ayrıca, VSTO Eklentilerindeki çalışma zamanında denetim ekleyebilirsiniz <xref:Microsoft.Office.Tools.Excel.Chart> .

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Bu konuda aşağıdaki görevler açıklanmaktadır:

- [Tasarım zamanında grafik denetimleri ekleme](#designtime)

- [Belge düzeyindeki bir projede çalışma zamanında grafik denetimleri ekleme](#runtimedoclevel)

- [VSTO eklenti projesindeki çalışma zamanında grafik denetimleri ekleme](#runtimeaddin)

  Denetimler hakkında <xref:Microsoft.Office.Tools.Excel.Chart> daha fazla bilgi için bkz. [Chart Control](../vsto/chart-control.md).

## <a name="designtime"></a>Tasarım zamanında grafik denetimleri ekleme
 <xref:Microsoft.Office.Tools.Excel.Chart> Denetim sayfanıza, uygulamanın içinden bir grafik ekleyeceğiniz şekilde ekleyebilirsiniz.

> [!NOTE]
> Denetim, **araç kutusu** veya **veri kaynakları** penceresinde kullanılamaz. <xref:Microsoft.Office.Tools.Excel.Chart>

### <a name="to-add-a-chart-host-control-to-a-worksheet-in-excel"></a>Excel 'deki çalışma sayfasına bir grafik konak denetimi eklemek için

1. **Ekle** sekmesinde, **grafikler** grubunda, **sütun**' a tıklayın, bir grafik kategorisine tıklayın ve sonra istediğiniz grafik türüne tıklayın.

2. **Grafik Ekle** Iletişim kutusunda **Tamam**' a tıklayın.

3. **Tasarım** sekmesinde, **veri** grubunda, **veri Seç**' e tıklayın.

4. **Veri kaynağı seç** iletişim kutusunda, **grafik** **veri aralığı** kutusuna tıklayın ve varsayılan seçimi kaldırın.

5. **Grafik verileri** sayfasında, grafiğe ait verileri içeren hücre aralığını seçin ( **a5** - **D8**arası hücreler).

6. **Veri kaynağı seç** Iletişim kutusunda **Tamam**' a tıklayın.

## <a name="runtimedoclevel"></a>Belge düzeyindeki bir projede çalışma zamanında grafik denetimleri ekleme
 <xref:Microsoft.Office.Tools.Excel.Chart> Denetimi çalışma zamanında dinamik olarak ekleyebilirsiniz. Belge kapatıldığında dinamik olarak oluşturulan grafikler, belgede konak denetimleri olarak kalıcı olmaz. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

#### <a name="to-add-a-chart-control-to-a-worksheet-programmatically"></a>Bir çalışma sayfasına programlı bir şekilde grafik denetimi eklemek için

1. Olay işleyicisinde, denetimi <xref:Microsoft.Office.Tools.Excel.Chart> eklemek için aşağıdaki kodu ekleyin. `Sheet1` <xref:Microsoft.Office.Tools.Excel.Worksheet.Startup>

     [!code-csharp[Trin_VstcoreHostControlsExcel#1](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#1)]
     [!code-vb[Trin_VstcoreHostControlsExcel#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#1)]

## <a name="runtimeaddin"></a>VSTO eklenti projesindeki çalışma zamanında grafik denetimleri ekleme
 VSTO eklenti projesindeki herhangi <xref:Microsoft.Office.Tools.Excel.Chart> bir açık çalışma sayfasına programlı olarak bir denetim ekleyebilirsiniz. Daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

 Çalışma sayfası kapatıldığında dinamik olarak oluşturulan grafik denetimleri çalışma sayfasında konak denetimleri olarak kalıcı olmaz. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

#### <a name="to-add-a-chart-control-to-a-worksheet-programmatically"></a>Bir çalışma sayfasına programlı bir şekilde grafik denetimi eklemek için

1. Aşağıdaki kod, açık çalışma sayfasına dayalı bir çalışma sayfası konak öğesi oluşturur ve sonra bir <xref:Microsoft.Office.Tools.Excel.Chart> denetim ekler.

     [!code-csharp[Trin_Excel_Dynamic_Controls#9](../vsto/codesnippet/CSharp/Trin_Excel_Dynamic_Controls/ThisAddIn.cs#9)]
     [!code-vb[Trin_Excel_Dynamic_Controls#9](../vsto/codesnippet/VisualBasic/Trin_Excel_Dynamic_Controls/ThisAddIn.vb#9)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek aşağıdaki gereksinimlere sahiptir:

- Çalışma sayfasındaki a5 ile D8 arasında depolanan, grafiklenen veriler.

## <a name="see-also"></a>Ayrıca bkz.
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Grafik denetimi](../vsto/chart-control.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Office çözümlerinde verileri denetimlere bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
