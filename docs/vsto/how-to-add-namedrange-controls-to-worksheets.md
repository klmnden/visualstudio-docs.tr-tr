---
title: 'Nasıl yapılır: Çalışma sayfalarına NamedRange denetimleri ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, adding to worksheets
- NamedRange control, adding to worksheets
- controls [Office development in Visual Studio], adding to worksheets
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 0bd5f9763150cf526acca2dfdc2762b3f202950a
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255618"
---
# <a name="how-to-add-namedrange-controls-to-worksheets"></a>Nasıl yapılır: Çalışma sayfalarına NamedRange denetimleri ekleme
  Tasarım zamanında bir <xref:Microsoft.Office.Tools.Excel.NamedRange> Microsoft Office Excel çalışma sayfasına ve belge düzeyi projelerinde çalışma zamanında denetim ekleyebilirsiniz.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Ayrıca, VSTO eklenti <xref:Microsoft.Office.Tools.Excel.NamedRange> projelerinde çalışma zamanında denetim ekleyebilirsiniz.

 Bu konuda aşağıdaki görevler açıklanmaktadır:

- [Tasarım zamanında NamedRange denetimleri ekleme](#designtime)

- [Belge düzeyindeki bir projede çalışma zamanında NamedRange denetimleri ekleme](#runtimedoclevel)

- [VSTO eklenti projesinde çalışma zamanında NamedRange denetimleri ekleme](#runtimeaddin)

  Denetimler hakkında <xref:Microsoft.Office.Tools.Excel.NamedRange> daha fazla bilgi için bkz. [NamedRange denetimi](../vsto/namedrange-control.md).

## <a name="designtime"></a>Tasarım zamanında NamedRange denetimleri ekleme
 Tasarım zamanında belge düzeyindeki bir projedeki <xref:Microsoft.Office.Tools.Excel.NamedRange> çalışma sayfasına denetim eklemenin birkaç yolu vardır: Excel içinden, Visual Studio **araç kutusundan**ve **veri kaynakları** penceresinden.

 [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

### <a name="to-add-a-namedrange-control-to-a-worksheet-using-the-name-box-in-excel"></a>Excel 'deki ad kutusunu kullanarak bir çalışma sayfasına NamedRange denetimi eklemek için

1. Adlandırılmış aralığa eklemek istediğiniz hücreyi veya hücreleri seçin.

2. **Ad kutusuna**, Aralık için bir ad yazın ve **ENTER**tuşuna basın.

     **Ad kutusu** , formül çubuğunun yanında, çalışma sayfasının **A** sütununun hemen üzerinde bulunur.

### <a name="to-add-a-namedrange-control-to-a-worksheet-using-the-toolbox"></a>Araç kutusunu kullanarak bir çalışma sayfasına NamedRange denetimi eklemek için

1. **Araç kutusunu** açın ve **Excel denetimleri** sekmesine tıklayın.

2. Tıklayın <xref:Microsoft.Office.Tools.Excel.NamedRange> ve bir çalışma sayfasına sürükleyin.

     **Adlandırılmış Aralık Ekle** iletişim kutusu görünür.

3. Adlandırılmış aralığa eklemek istediğiniz hücreyi veya hücreleri seçin.

4. **Tamam**'ı tıklatın.

     Denetim için verilen varsayılan adı istemiyorsanız, **Özellikler** penceresinde adı değiştirebilirsiniz.

### <a name="to-add-a-namedrange-control-to-a-worksheet-using-the-data-sources-window"></a>Veri Kaynakları penceresini kullanarak bir çalışma sayfasına NamedRange denetimi eklemek için

1. **Veri kaynakları** penceresini açın ve projeniz için bir veri kaynağı oluşturun. Daha fazla bilgi için bkz. [yeni bağlantılar ekleme](../data-tools/add-new-connections.md).

2. **Veri kaynakları** penceresinden çalışma sayfanıza tek bir alan sürükleyin.

     Çalışma sayfasına veriye dayalı <xref:Microsoft.Office.Tools.Excel.NamedRange> bir denetim eklenir. Daha fazla bilgi için bkz. [veri bağlama ve Windows Forms](/dotnet/framework/winforms/data-binding-and-windows-forms).

## <a name="runtimedoclevel"></a>Belge düzeyindeki bir projede çalışma zamanında NamedRange denetimleri ekleme
 Çalışma zamanında çalışma sayfanıza <xref:Microsoft.Office.Tools.Excel.NamedRange> programlı bir denetim ekleyebilirsiniz. Bu, olaylara yanıt olarak konak denetimleri oluşturmanızı sağlar. Dinamik olarak oluşturulan adlandırılmış aralıklar çalışma sayfası kapalıyken konak denetimleri olarak çalışma sayfasında kalıcı olmaz. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

### <a name="to-add-a-namedrange-control-to-a-worksheet-programmatically"></a>Bir çalışma sayfasına programlı olarak NamedRange denetimi eklemek için

1. <xref:Microsoft.Office.Tools.Excel.NamedRange.Value2%2A> Olay işleyicisinde, a1 hücresine <xref:Microsoft.Office.Tools.Excel.NamedRange> denetim eklemek ve özelliğini olarak ayarlamak için aşağıdaki kodu ekleyin. `Sheet1` <xref:Microsoft.Office.Tools.Excel.Worksheet.Startup>`Hello world!`

     [!code-csharp[Trin_VstcoreHostControlsExcel#3](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#3)]
     [!code-vb[Trin_VstcoreHostControlsExcel#3](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#3)]

## <a name="runtimeaddin"></a>VSTO eklenti projesinde çalışma zamanında NamedRange denetimleri ekleme
 VSTO eklenti projesindeki herhangi <xref:Microsoft.Office.Tools.Excel.NamedRange> bir açık çalışma sayfasına programlı olarak bir denetim ekleyebilirsiniz. Dinamik olarak oluşturulan adlandırılmış aralıklar çalışma sayfası kapalıyken konak denetimleri olarak çalışma sayfasında kalıcı olmaz. Daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

### <a name="to-add-a-namedrange-control-to-a-worksheet-programmatically"></a>Bir çalışma sayfasına programlı olarak NamedRange denetimi eklemek için

1. Aşağıdaki kod, açık çalışma sayfasına dayalı bir çalışma sayfası konak öğesi <xref:Microsoft.Office.Tools.Excel.NamedRange> oluşturur ve sonra **a1** hücresine bir denetim ekler ve <xref:Microsoft.Office.Tools.Excel.NamedRange.Value2%2A> özelliğini olarak `Hello world`ayarlar.

     [!code-csharp[Trin_Excel_Dynamic_Controls#7](../vsto/codesnippet/CSharp/Trin_Excel_Dynamic_Controls/ThisAddIn.cs#7)]
     [!code-vb[Trin_Excel_Dynamic_Controls#7](../vsto/codesnippet/VisualBasic/Trin_Excel_Dynamic_Controls/ThisAddIn.vb#7)]

## <a name="see-also"></a>Ayrıca bkz.
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [NamedRange denetimi](../vsto/namedrange-control.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Nasıl yapılır: NamedRange denetimlerini yeniden boyutlandır](../vsto/how-to-resize-namedrange-controls.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
