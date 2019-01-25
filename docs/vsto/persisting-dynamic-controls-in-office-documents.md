---
title: Office belgelerinde Dinamik denetimleri kalıcı
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office documents [Office development in Visual Studio, Windows Forms controls
- Office documents [Office development in Visual Studio, host controls
- controls [Office development in Visual Studio], persisting in the document
- Windows Forms controls [Office development in Visual Studio], persisting in the document
- documents [Office development in Visual Studio], Windows Forms controls
- documents [Office development in Visual Studio], host controls
- host controls [Office development in Visual Studio], persisting in the document
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 48b2cc1402243bfedb7b22280b4a161235cb9957
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54863519"
---
# <a name="persist-dynamic-controls-in-office-documents"></a>Office belgelerinde Dinamik denetimleri kalıcı

Belge veya çalışma kitabının kaydedilmiş ve kapandığında çalışma zamanında eklenen denetimlerin kalıcı değildir. Tam davranış konak denetimleri ve Windows Forms denetimleri için farklıdır. Her iki durumda da, çözümünüze kullanıcı belgeyi yeniden açana denetimleri yeniden oluşturmak için kod ekleyebilirsiniz.

Çalışma zamanında belgelere ekleme denetimleri çağrılır *Dinamik denetimleri*. Dinamik denetimleri hakkında daha fazla bilgi için bkz: [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

[!INCLUDE[appliesto_controls](../vsto/includes/appliesto-controls-md.md)]

## <a name="persist-host-controls-in-the-document"></a>Konak denetimleri belgede kalıcı

Bir Belge kaydedildiğinde ve kapatılan tüm dinamik ana bilgisayar denetimleri belgeden kaldırılır. Geriye yalnızca temel alınan yerel Office nesneler kalır. Örneğin, bir <xref:Microsoft.Office.Tools.Excel.ListObject?displayProperty=fullName> konak kontrolü olur bir <xref:Microsoft.Office.Interop.Excel.ListObject?displayProperty=fullName>. Ana bilgisayar denetim olaylarına yerel Office nesneleri bağlı değil ve veri bağlama işlevselliğini konak kontrolü yoktur.

Aşağıdaki tabloda, her ana denetim türü için bir belgede geride yerel Office nesne listeler.

|Ana bilgisayar Denetim türü|Yerel Office nesne türü|
|-----------------------|-------------------------------|
|<xref:Microsoft.Office.Tools.Excel.Chart>|<xref:Microsoft.Office.Interop.Excel.Chart>|
|<xref:Microsoft.Office.Tools.Excel.ListObject>|<xref:Microsoft.Office.Interop.Excel.ListObject>|
|<xref:Microsoft.Office.Tools.Excel.NamedRange>|<xref:Microsoft.Office.Interop.Excel.Range>|
|<xref:Microsoft.Office.Tools.Word.Bookmark>|<xref:Microsoft.Office.Interop.Word.Bookmark>|
|<xref:Microsoft.Office.Tools.Word.BuildingBlockGalleryContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.ComboBoxContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.ContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.DatePickerContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.DropDownListContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.GroupContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.PictureContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.PlainTextContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.RichTextContentControl>|<xref:Microsoft.Office.Interop.Word.ContentControl>|

### <a name="re-create-dynamic-host-controls-when-documents-are-opened"></a>Belge açıldığında, dinamik ana bilgisayar denetimleri yeniden oluşturun

Bir kullanıcının belgeyi açtığında, mevcut yerel denetimleri yerine dinamik ana bilgisayar denetimleri yeniden oluşturabilirsiniz. Bir belge açık olduğunda bu şekilde konak denetimleri oluşturma, kullanıcıları beklenebilir deneyimi benzetimini yapar.

Konak denetim sözcüğü için yeniden oluşturmanız veya bir <xref:Microsoft.Office.Tools.Excel.NamedRange> veya <xref:Microsoft.Office.Tools.Excel.ListObject> konak kontrolü Excel, kullanım için bir `Add` \< *denetim sınıf*> yöntemi bir <xref:Microsoft.Office.Tools.Excel.ControlCollection?displayProperty=fullName> veya <xref:Microsoft.Office.Tools.Word.ControlCollection?displayProperty=fullName> nesne. Yerel Office nesne için bir parametre içeren bir yöntem kullanın.

Örneğin oluşturmak istiyorsanız, bir <xref:Microsoft.Office.Tools.Excel.ListObject?displayProperty=fullName> konak var olan bir yerel denetiminden <xref:Microsoft.Office.Interop.Excel.ListObject?displayProperty=fullName> belge açıldığında kullanın <xref:Microsoft.Office.Tools.Excel.ControlCollection.AddListObject%2A> yöntemi ve mevcut geçişi <xref:Microsoft.Office.Interop.Excel.ListObject>. Aşağıdaki kod örneği bu Excel için belge düzeyi projede gösterir. Dinamik kod oluşturur, yeniden <xref:Microsoft.Office.Tools.Excel.ListObject> var olan bir alan <xref:Microsoft.Office.Interop.Excel.ListObject> adlı `MyListObject` içinde `Sheet1` sınıfı.

[!code-csharp[Trin_ExcelWorkbookDynamicControls#6](../vsto/codesnippet/CSharp/trin_excelworkbookdynamiccontrols4/Sheet1.cs#6)]
[!code-vb[Trin_ExcelWorkbookDynamicControls#6](../vsto/codesnippet/VisualBasic/trin_excelworkbookdynamiccontrols4/Sheet1.vb#6)]

### <a name="re-create-chart"></a>Grafiği yeniden oluşturun

Yeniden oluşturmak için bir <xref:Microsoft.Office.Tools.Excel.Chart?displayProperty=fullName> konak kontrolü, yerel silmelisiniz <xref:Microsoft.Office.Interop.Excel.Chart?displayProperty=fullName>ve yeniden oluşturma <xref:Microsoft.Office.Tools.Excel.Chart?displayProperty=fullName> kullanarak <xref:Microsoft.Office.Tools.Excel.ControlCollection.AddChart%2A> yöntemi. Yok hiçbir `Add` \< *denetim sınıf*> Yeni bir oluşturmanızı sağlayan yöntemi <xref:Microsoft.Office.Tools.Excel.Chart?displayProperty=fullName> dayanan <xref:Microsoft.Office.Interop.Excel.Chart?displayProperty=fullName>.

Yerel ilk silmezseniz <xref:Microsoft.Office.Interop.Excel.Chart>, yeniden oluşturduğunuzda, ikinci ve yinelenen bir hesap oluşturmanız <xref:Microsoft.Office.Tools.Excel.Chart?displayProperty=fullName>.

## <a name="persist-windows-forms-controls-in-documents"></a>Kalıcı belgelerindeki Windows Forms denetimleri

Bir belge kaydedildi ve ardından kapatıldığında [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] otomatik olarak dinamik olarak oluşturulan tüm Windows Formları denetimlerini belgeden kaldırır. Ancak, davranış belge düzeyi ve VSTO eklentisi projeleri için farklıdır.

Belge düzeyi özelleştirmelerde denetimleri ve (Bu belgede denetimleri barındırmak için kullanılan), temel alınan ActiveX sarmalayıcısının belgeyi bir sonraki açılışında kaldırılır. Şimdiye kadar denetimleri olan bir gösterge yoktur vardır.

VSTO eklentileri denetimler kaldırılır, ancak ActiveX sarmalayıcısının belgede kalır. Kullanıcı, belgeyi bir sonraki açışında ActiveX sarmalayıcısının görülebilir. Belge kaydedildi son kez göründüğü gibi Excel'de ActiveX sarmalayıcısının denetimleri görüntüler. Word, bunlar üzerinde kullanıcı tıkladığında sürece ActiveX sarmalayıcısının görünmez, bu durumda bunlar kenarlık denetimleri temsil eden bir noktalı çizgi görüntüler. ActiveX sarmalayıcıları birkaç yolu vardır. Daha fazla bilgi için [kaldırmak ActiveX sarmalayıcısının içinde bir eklenti](#removingActiveX).

### <a name="re-create-windows-forms-controls-when-documents-are-opened"></a>Belge açıldığında Windows Forms denetimleri yeniden oluşturma

Kullanıcı belgeyi yeniden açana zaman silinen Windows Forms denetimleri yeniden oluşturabilirsiniz. Bunu yapmak için çözümünüzün aşağıdaki görevleri gerçekleştirmeniz gerekir:

1.  Belge kaydedildiğinde veya boyutunu, konumu ve durumu denetimleri hakkında bilgi Store. Belge düzeyi özelleştirmesinde, belge verileri önbelleğe veri kaydedebilirsiniz. Bir VSTO eklenti, verileri özel bir XML parçasına belgedeki kaydedebilirsiniz.

2.  Belge açıldığında bir olay denetimlerinde yeniden oluşturun. Belge düzeyinde projelerde bunu yapabilirsiniz `Sheet` *n* `_Startup` veya `ThisDocument_Startup` olay işleyicileri. Projelerinde, VSTO eklentisi, bu olay işleyicileri yapabileceğiniz <xref:Microsoft.Office.Interop.Excel.AppEvents_Event.WorkbookOpen> veya <xref:Microsoft.Office.Interop.Word.ApplicationEvents4_Event.DocumentOpen> olayları.

###  <a name="removingActiveX"></a> Bir eklenti ActiveX sarmalayıcısının Kaldır

Bir VSTO eklentisi kullanarak belgelerine dinamik bir Windows Forms denetimleri ekleme, denetimleri için ActiveX sarmalayıcısının belge içinde sonraki seferde aşağıdaki yollarla açıldığında görüntülenmesini engelleyebilirsiniz.

#### <a name="remove-activex-wrappers-when-the-document-is-opened"></a>Belge açıldığında ActiveX sarmalayıcısının Kaldır

Tüm ActiveX sarmalayıcısının kaldırmak için çağrı `GetVstoObject` konak öğesi oluşturmak için yöntem <xref:Microsoft.Office.Interop.Word.Document> veya <xref:Microsoft.Office.Interop.Excel.Workbook> temsil eden yeni açılan belge. Örneğin, bir Word belgesi tüm ActiveX sarmalayıcısının kaldırmak için çağırabilirsiniz `GetVstoObject` konak öğesi oluşturmak için yöntem <xref:Microsoft.Office.Interop.Word.Document> için olay işleyicisine geçirilen nesne <xref:Microsoft.Office.Interop.Word.ApplicationEvents4_Event.DocumentOpen> olay.

Bu yordam, belge VSTO eklentinin yüklü olan bilgisayarlarda açılacak bildiğinizde yararlıdır. VSTO yüklü eklenti olmayan diğer kullanıcılar için belge geçebilir, belge kapatılmadan denetimleri kaldırma göz önünde bulundurun.

Aşağıdaki kod örneğinde nasıl çağrılacağını gösterir `GetVstoObject` belge açıldığında yöntemi.

[!code-vb[Trin_WordAddInDynamicControls#11](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#11)]
[!code-csharp[Trin_WordAddInDynamicControls#11](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#11)]

Ancak `GetVstoObject` yöntemi, öncelikli olarak çalışma zamanında yeni bir ana bilgisayar öğesi oluşturmak için kullanılır, bu yöntem, aynı zamanda belgedeki tüm ActiveX sarmalayıcısının için belirli bir belge çağırıldığında ilk kez temizler. Nasıl kullanılacağı hakkında daha fazla bilgi için `GetVstoObject` yöntemi bkz [genişletmek Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında VSTO Add-Ins](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

Belge açıldığında VSTO eklenti denetimleri dinamik oluşturursa, VSTO eklenti zaten çağıracak `GetVstoObject` denetimleri oluşturma işleminin bir parçası olarak yöntemi. Ayrı bir çağrı ekleyin gerekmez `GetVstoObject` ActiveX sarmalayıcısının Bu senaryoda kaldırmak için yöntemi.

#### <a name="remove-the-dynamic-controls-before-the-document-is-closed"></a>Belge kapatılmadan önce dinamik denetimlerini kaldırma

Belge kapatılmadan önce VSTO eklenti açıkça her dinamik denetim belgeden kaldırabilirsiniz. Bu yordam, VSTO yüklü eklenti olmayan diğer kullanıcılar için geçirilen belgeler için kullanışlıdır.

Aşağıdaki kod örneği, belge kapatıldığında tüm Windows Formları denetimleri Word belgesinden nasıl kaldırılacağı gösterilmektedir.

[!code-vb[Trin_WordAddInDynamicControls#10](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#10)]
[!code-csharp[Trin_WordAddInDynamicControls#10](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#10)]

## <a name="see-also"></a>Ayrıca bkz.

- [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
