---
title: 'Nasıl yapılır: Office belgelerine Windows Forms denetimleri ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office documents [Office development in Visual Studio, Windows Forms controls
- Windows Forms controls [Office development in Visual Studio], adding
- controls [Office development in Visual Studio], Windows Forms controls
- documents [Office development in Visual Studio], Windows Forms controls
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a745794bb23902872f4b09c39eb8a3b3c1706137
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255879"
---
# <a name="how-to-add-windows-forms-controls-to-office-documents"></a>Nasıl yapılır: Office belgelerine Windows Forms denetimleri ekleme
  Belge düzeyi projelerinde, tasarım zamanında Excel Microsoft Office ve Microsoft Office Word belgelerine Windows Forms denetimleri ekleyebilirsiniz. Çalışma zamanında, belge düzeyi özelleştirmelerine ve VSTO eklentilerine denetim ekleyebilirsiniz. Örneğin, kullanıcıların bir seçenek listesinden seçim <xref:Microsoft.Office.Tools.Excel.Controls.ComboBox> yapabilmesi için çalışma sayfanıza bir denetim ekleyebilirsiniz.

 [!INCLUDE[appliesto_controls](../vsto/includes/appliesto-controls-md.md)]

 Bu konuda aşağıdaki görevler açıklanmaktadır:

- [Tasarım zamanında denetim ekleme](#designtime)

- [Belge düzeyi projelerde çalışma zamanında denetim ekleme](#runtimedoclevel)

- [VSTO eklentilerinde çalışma zamanında denetim ekleme](#runtimeaddin)

  ![video bağlantısı](../vsto/media/playvideo.gif "video bağlantısı") İlgili video gösterimi için bkz [. nasıl yaparım?: Çalışma zamanında bir belge yüzeyine denetimler eklensin mi? ](http://go.microsoft.com/fwlink/?LinkId=132782).

## <a name="designtime"></a>Tasarım zamanında denetim ekleme
 Belge düzeyindeki bir projede belgeye tasarım zamanında Windows Forms denetimleri eklemenin birkaç yolu vardır.

 [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

### <a name="to-drag-a-windows-forms-control-to-the-document"></a>Windows Forms denetimini belgeye sürüklemek için

1. Belge tasarımcıda görünür olması için Visual Studio 'da bir Excel çalışma kitabı projesi veya Word belgesi projesi oluşturun veya açın. Proje oluşturma hakkında daha fazla bilgi için [bkz. nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

2. **Araç kutusunun** **ortak denetimler** sekmesinde eklemek istediğiniz denetime tıklayın ve belgeyi belgeye sürükleyin.

    > [!NOTE]
    > Excel 'de bir denetim seçtiğinizde, **Formül çubuğuna** **= embed ("WinForms. Control. Host", "")** görürsünüz. Bu metin gereklidir ve silinmemelidir.

### <a name="to-draw-a-windows-forms-control-on-the-document"></a>Belgede Windows Forms denetimi çizmek için

1. Belge tasarımcıda görünür olması için Visual Studio 'da bir Excel çalışma kitabı projesi veya Word belgesi projesi oluşturun veya açın. Proje oluşturma hakkında daha fazla bilgi için [bkz. nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

2. **Araç kutusunun** **ortak denetimler** sekmesinde, eklemek istediğiniz denetime tıklayın.

3. Belge üzerinde, denetimin sol üst köşesinin bulunmasını istediğiniz yere tıklayın ve denetimin sağ alt köşesinin bulunmasını istediğiniz yere sürükleyin.

     Denetim belgeye belirtilen konum ve boyutla eklenir.

    > [!NOTE]
    > Excel 'de bir denetim seçtiğinizde, **Formül çubuğuna** **= embed ("WinForms. Control. Host", "")** görürsünüz. Bu metin gereklidir ve silinmemelidir.

### <a name="to-add-a-windows-forms-control-to-the-document-by-single-clicking-the-control"></a>Denetime tek tıklanarak belgeye Windows Forms denetimi eklemek için

1. Belge tasarımcıda görünür olması için Visual Studio 'da bir Excel çalışma kitabı projesi veya Word belgesi projesi oluşturun veya açın. Proje oluşturma hakkında daha fazla bilgi için [bkz. nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

2. **Araç kutusunun** **ortak denetimler** sekmesinde, eklemek istediğiniz denetime tıklayın

3. Bir belge, denetimin eklenmesini istediğiniz yere tıklayın.

     Denetim belgeye varsayılan boyutla eklenir.

    > [!NOTE]
    > Excel 'de bir denetim seçtiğinizde, **Formül çubuğuna** **= embed ("WinForms. Control. Host", "")** görürsünüz. Bu metin gereklidir ve silinmemelidir.

### <a name="to-add-a-windows-forms-control-to-the-document-by-double-clicking-the-control"></a>Denetime çift tıklayarak belgeye Windows Forms denetimi eklemek için

1. Belge tasarımcıda görünür olması için Visual Studio 'da bir Excel çalışma kitabı projesi veya Word belgesi projesi oluşturun veya açın. Proje oluşturma hakkında daha fazla bilgi için [bkz. nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

2. **Araç kutusunun** **ortak denetimler** sekmesinde, eklemek istediğiniz denetime çift tıklayın.

     Denetim belgeye belge veya etkin bölmesinin merkezinde eklenir.

    > [!NOTE]
    > Excel 'de bir denetim seçtiğinizde, **Formül çubuğuna** **= embed ("WinForms. Control. Host", "")** görürsünüz. Bu metin gereklidir ve silinmemelidir.

### <a name="to-add-a-windows-forms-control-to-the-document-by-pressing-the-enter-key"></a>ENTER tuşuna basarak belgeye Windows Forms denetimi eklemek için

1. Belge tasarımcıda görünür olması için Visual Studio 'da bir Excel çalışma kitabı projesi veya Word belgesi projesi oluşturun veya açın. Proje oluşturma hakkında daha fazla bilgi için [bkz. nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

2. **Araç kutusunun** **ortak denetimler** sekmesinde, eklemek Istediğiniz denetime tıklayın ve **ENTER** tuşuna basın.

     Denetim belgeye belge veya etkin bölmesinin merkezinde eklenir.

    > [!NOTE]
    > Excel 'de bir denetim seçtiğinizde, **Formül çubuğuna** **= embed ("WinForms. Control. Host", "")** görürsünüz. Bu metin gereklidir ve silinmemelidir.

## <a name="runtimedoclevel"></a>Belge düzeyi projelerde çalışma zamanında denetim ekleme
 Çalışma zamanında bir belgeye program aracılığıyla Windows Forms denetimleri ekleyebilirsiniz. Word 'de, <xref:Microsoft.Office.Tools.Word.DocumentBase.Controls%2A> `ThisDocument` sınıfının özelliğinin yöntemlerini kullanın. Excel 'de <xref:Microsoft.Office.Tools.Excel.WorksheetBase.Controls%2A> *n* sınıfının özelliğinin `Sheet`yöntemlerini kullanın. Her yöntemde, denetimin konumunu farklı şekillerde belirtmenize imkan tanıyan birkaç aşırı yükleme vardır.

 Çalışma zamanında bir belgeye Windows Forms denetimi eklediğinizde, belge kapatıldığında denetim belgede kalıcı olmaz. Belgeyi bir dahaki sefer açıldığında denetimi yeniden oluşturabilirsiniz. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

### <a name="to-add-a-windows-forms-control-at-run-time"></a>Çalışma zamanında bir Windows Forms denetimi eklemek için

1. Add\<*Control Class*adlı bir yöntemi kullanın > ( *Denetim sınıfı* , eklemek <xref:Microsoft.Office.Tools.Word.ControlExtensions.AddButton%2A>istediğiniz Windows Forms denetiminin sınıf adıdır).

     Aşağıdaki kod örneği, Excel için belge düzeyindeki bir <xref:Microsoft.Office.Tools.Excel.Controls.Button> projede **C5** öğesinin `Sheet1` bir hücresine nasıl ekleneceğini gösterir.

     [!code-vb[Trin_VstcoreProgrammingControlsExcel#4](../vsto/codesnippet/VisualBasic/my excel chart/Sheet1.vb#4)]
     [!code-csharp[Trin_VstcoreProgrammingControlsExcel#4](../vsto/codesnippet/CSharp/Trin_VstcoreProgrammingControlsExcelCS/Sheet1.cs#4)]

## <a name="runtimeaddin"></a>VSTO eklentilerinde çalışma zamanında denetim ekleme
 Çalışma zamanında herhangi bir açık belgeye program aracılığıyla Windows Forms denetimleri ekleyebilirsiniz. İlk olarak, açık bir belgeyi veya çalışma sayfasını temel alan bir konak öğesi oluşturun. Ardından, Word 'de yeni ana bilgisayar öğesinin <xref:Microsoft.Office.Tools.Word.Document.Controls%2A> özelliğinin yöntemlerini kullanın. Excel 'de yeni ana bilgisayar öğesinin <xref:Microsoft.Office.Tools.Excel.Worksheet.Controls%2A> özelliğinin yöntemlerini kullanın. Her yöntemde, denetimin konumunu farklı şekillerde belirtmenize imkan tanıyan birkaç aşırı yükleme vardır.

 Çalışma zamanında bir belgeye Windows Forms denetimi eklediğinizde, belge kapatıldığında denetim belgede kalıcı olmaz. Belgeyi bir dahaki sefer açıldığında denetimi yeniden oluşturabilirsiniz. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

 VSTO eklenti projelerinde konak öğeleri oluşturma hakkında daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

### <a name="to-add-a-windows-forms-control-at-run-time"></a>Çalışma zamanında bir Windows Forms denetimi eklemek için

1. Add\<*Control Class*adlı bir yöntemi kullanın > ( *Denetim sınıfı* , eklemek <xref:Microsoft.Office.Tools.Word.ControlExtensions.AddButton%2A>istediğiniz Windows Forms denetiminin sınıf adıdır).

    > [!NOTE]
    > [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya sonraki bir sürümü hedefleyen VSTO eklenti projelerinde, Add 'e erişebilmek için önce *Microsoft. Office. Tools. Excel. v 4.0. Utilities. dll* veya *Microsoft. Office. Tools. Word. v 4.0. Utilities. dll* derlemesine bir başvuru eklemeniz gerekir. Denetim sınıfı > yöntemleri. \<

     Aşağıdaki kod örneği, bir <xref:Microsoft.Office.Tools.Word.Controls.Button> Word VSTO eklentisi kullanarak etkin belgenin ilk paragrafına nasıl ekleneceğini gösterir.

     [!code-vb[Trin_WordAddInDynamicControls#7](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#7)]
     [!code-csharp[Trin_WordAddInDynamicControls#7](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#7)]

## <a name="see-also"></a>Ayrıca bkz.
- [Windows Forms denetimlerine Office belgeleri genel bakış](../vsto/windows-forms-controls-on-office-documents-overview.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Nasıl yapılır: Çalışma sayfası hücrelerinin içindeki denetimleri yeniden boyutlandırma](../vsto/how-to-resize-controls-within-worksheet-cells.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
