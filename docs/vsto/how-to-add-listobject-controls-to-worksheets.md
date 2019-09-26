---
title: 'Nasıl yapılır: Çalışma sayfalarına ListObject denetimleri ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ListObject control, adding to worksheets
- controls [Office development in Visual Studio], adding to worksheets
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: d4f6ca2544f64433746f6aa57c9456fee11459db
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71254685"
---
# <a name="how-to-add-listobject-controls-to-worksheets"></a>Nasıl yapılır: Çalışma sayfalarına ListObject denetimleri ekleme
  Tasarım zamanında bir <xref:Microsoft.Office.Tools.Excel.ListObject> Microsoft Office Excel çalışma sayfasına ve belge düzeyi projelerinde çalışma zamanında denetim ekleyebilirsiniz.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Ayrıca, VSTO eklenti <xref:Microsoft.Office.Tools.Excel.ListObject> projelerinde çalışma zamanında denetim ekleyebilirsiniz.

 Bu konuda aşağıdaki görevler açıklanmaktadır:

- [Tasarım zamanında ListObject denetimleri ekleme](#designtime)

- [Belge düzeyindeki bir projede çalışma zamanında ListObject denetimleri ekleme](#runtimedoclevel)

- [VSTO eklenti projesindeki ListObject denetimlerini çalışma zamanında ekleme](#runtimeaddin)

  Denetimler hakkında <xref:Microsoft.Office.Tools.Excel.ListObject> daha fazla bilgi için bkz. [ListObject denetimi](../vsto/listobject-control.md).

## <a name="designtime"></a>Tasarım zamanında ListObject denetimleri ekleme
 Tasarım zamanında belge düzeyindeki bir projedeki <xref:Microsoft.Office.Tools.Excel.ListObject> çalışma sayfasına denetim eklemenin birkaç yolu vardır: Excel içinden, Visual Studio **araç kutusundan**ve **veri kaynakları** penceresinden.

 [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

### <a name="to-use-the-ribbon-in-excel"></a>Şeriti Excel 'de kullanmak için

1. **Ekle** sekmesinde, **Tablolar** grubunda, **tablo**' ya tıklayın.

2. Listeye eklemek istediğiniz hücreyi veya hücreleri seçin ve **Tamam**' a tıklayın.

#### <a name="to-use-the-toolbox"></a>Araç kutusunu kullanmak için

1. **Araç kutusunun** <xref:Microsoft.Office.Tools.Excel.ListObject> **Excel denetimleri** sekmesinden, çalışma sayfasına sürükleyin.

     **ListObject denetimi Ekle** iletişim kutusu görüntülenir.

2. Listeye eklemek istediğiniz hücreyi veya hücreleri seçin ve **Tamam**' a tıklayın.

     Varsayılan adı korumak istemiyorsanız, adı **Özellikler** penceresinde değiştirebilirsiniz.

#### <a name="to-use-the-data-sources-window"></a>Veri Kaynakları penceresini kullanmak için

1. **Veri kaynakları** penceresini açın ve projeniz için bir veri kaynağı oluşturun. Daha fazla bilgi için bkz. [yeni bağlantılar ekleme](../data-tools/add-new-connections.md).

2. **Veri kaynakları** penceresinden bir tabloyu çalışma sayfanıza sürükleyin.

     Çalışma sayfasına veriye dayalı <xref:Microsoft.Office.Tools.Excel.ListObject> bir denetim eklenir. Daha fazla bilgi için bkz. [veri bağlama ve Windows Forms](/dotnet/framework/winforms/data-binding-and-windows-forms).

## <a name="runtimedoclevel"></a>Belge düzeyindeki bir projede çalışma zamanında ListObject denetimleri ekleme
 <xref:Microsoft.Office.Tools.Excel.ListObject> Denetimi çalışma zamanında dinamik olarak ekleyebilirsiniz. Bu, olaylara yanıt olarak konak denetimleri oluşturmanızı sağlar. Çalışma sayfası kapatıldığında dinamik olarak oluşturulan liste nesneleri çalışma sayfasında konak denetimleri olarak kalıcı olmaz. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

#### <a name="to-add-a-listobject-control-to-a-worksheet-programmatically"></a>Bir çalışma sayfasına programlı bir ListObject denetimi eklemek için

1. <xref:Microsoft.Office.Tools.Excel.ListObject> ' In <xref:Microsoft.Office.Tools.Excel.Worksheet.Startup> `Sheet1`olay işleyicisinde, a1 ile a4 arası hücrelere bir denetim eklemek için aşağıdaki kodu ekleyin.

     [!code-csharp[Trin_VstcoreHostControlsExcel#2](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#2)]
     [!code-vb[Trin_VstcoreHostControlsExcel#2](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#2)]

## <a name="runtimeaddin"></a>VSTO eklenti projesindeki ListObject denetimlerini çalışma zamanında ekleme
 VSTO eklenti projesindeki herhangi <xref:Microsoft.Office.Tools.Excel.ListObject> bir açık çalışma sayfasına programlı olarak bir denetim ekleyebilirsiniz. Dinamik olarak oluşturulan liste nesneleri, çalışma sayfası kaydedilip kapatıldığında konak denetimleri olarak çalışma sayfasında kalıcı olmaz. Daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

#### <a name="to-add-a-listobject-control-to-a-worksheet-programmatically"></a>Bir çalışma sayfasına programlı bir ListObject denetimi eklemek için

1. Aşağıdaki kod, açık çalışma sayfasına dayalı bir çalışma sayfası konak öğesi oluşturur ve sonra **a1** ile **a4**arası hücrelere <xref:Microsoft.Office.Tools.Excel.ListObject> bir denetim ekler.

     [!code-csharp[Trin_Excel_Dynamic_Controls#8](../vsto/codesnippet/CSharp/Trin_Excel_Dynamic_Controls/ThisAddIn.cs#8)]
     [!code-vb[Trin_Excel_Dynamic_Controls#8](../vsto/codesnippet/VisualBasic/Trin_Excel_Dynamic_Controls/ThisAddIn.vb#8)]

## <a name="see-also"></a>Ayrıca bkz.
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [ListObject denetimi](../vsto/listobject-control.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Nasıl yapılır: ListObject denetimlerini yeniden boyutlandır](../vsto/how-to-resize-listobject-controls.md)
- [Office çözümlerinde verileri denetimlere bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
