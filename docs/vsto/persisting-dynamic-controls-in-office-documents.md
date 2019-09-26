---
title: Office belgelerinde dinamik denetimleri kalıcı hale getirme
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
ms.openlocfilehash: 5d48dfab18ec2165753ac19330f7fbe18c923da9
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255999"
---
# <a name="persist-dynamic-controls-in-office-documents"></a>Office belgelerinde dinamik denetimleri kalıcı hale getirme

Çalışma zamanında eklenen denetimler belge veya çalışma kitabı kaydedilip kapatıldığında kalıcı olmaz. Tam davranış konak denetimleri ve Windows Forms denetimleri için farklıdır. Her iki durumda da, Kullanıcı belgeyi yeniden açtığında denetimleri yeniden oluşturmak için çözümünüze kod ekleyebilirsiniz.

Çalışma zamanında belgelere eklediğiniz denetimlere *Dinamik denetimler*denir. Dinamik denetimler hakkında daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

[!INCLUDE[appliesto_controls](../vsto/includes/appliesto-controls-md.md)]

## <a name="persist-host-controls-in-the-document"></a>Belgedeki konak denetimlerini kalıcı yap

Bir belge kaydedilip kapatıldığında, tüm dinamik konak denetimleri belgeden kaldırılır. Yalnızca temeldeki yerel Office nesneleri geride kalır. Örneğin, <xref:Microsoft.Office.Tools.Excel.ListObject?displayProperty=fullName> bir konak denetimi bir <xref:Microsoft.Office.Interop.Excel.ListObject?displayProperty=fullName>olur. Yerel Office nesneleri konak denetim olaylarına bağlı değildir ve konak denetiminin veri bağlama işlevselliğine sahip değildir.

Aşağıdaki tabloda her bir konak denetimi türü için bir belgede kalan yerel Office nesnesi listelenmektedir.

|Konak denetim türü|Yerel ofis nesne türü|
|-----------------------|-------------------------------|
|<xref:Microsoft.Office.Tools.Excel.Chart>|<xref:Microsoft.Office.Interop.Excel.Chart>|
|<xref:Microsoft.Office.Tools.Excel.ListObject>|<xref:Microsoft.Office.Interop.Excel.ListObject>|
|<xref:Microsoft.Office.Tools.Excel.NamedRange>|<xref:Microsoft.Office.Interop.Excel.Range>|
|<xref:Microsoft.Office.Tools.Word.Bookmark>|<xref:Microsoft.Office.Interop.Word.Bookmark>|
|<xref:Microsoft.Office.Tools.Word.BuildingBlockGalleryContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.ComboBoxContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.ContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.DatePickerContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.DropDownListContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.GroupContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.PictureContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.PlainTextContentControl><br /><br /> <xref:Microsoft.Office.Tools.Word.RichTextContentControl>|<xref:Microsoft.Office.Interop.Word.ContentControl>|

### <a name="re-create-dynamic-host-controls-when-documents-are-opened"></a>Belgeler açıldığında dinamik ana bilgisayar denetimlerini yeniden oluştur

Bir Kullanıcı belgeyi her açtığında, var olan yerel denetimlerin yerine dinamik ana bilgisayar denetimlerini yeniden oluşturabilirsiniz. Bir belge açıldığında, kullanıcıların beklediği deneyime benzediğinde, bu şekilde konak denetimleri oluşturma.

Word için bir konak denetimini veya Excel <xref:Microsoft.Office.Tools.Excel.NamedRange> `Add` \<için bir veya <xref:Microsoft.Office.Tools.Excel.ListObject> konak denetimini yeniden oluşturmak için bir <xref:Microsoft.Office.Tools.Excel.ControlCollection?displayProperty=fullName> veya <xref:Microsoft.Office.Tools.Word.ControlCollection?displayProperty=fullName> nesnesinin *Denetim sınıfı*> yöntemini kullanın. Yerel Office nesnesi için parametresi olan bir yöntemi kullanın.

Örneğin, belge açıldığında <xref:Microsoft.Office.Tools.Excel.ListObject?displayProperty=fullName> var olan bir yerel <xref:Microsoft.Office.Interop.Excel.ListObject?displayProperty=fullName> kümeden bir konak denetimi oluşturmak istiyorsanız, <xref:Microsoft.Office.Tools.Excel.ControlCollection.AddListObject%2A> yöntemini kullanın ve mevcut <xref:Microsoft.Office.Interop.Excel.ListObject>' ı geçirin. Aşağıdaki kod örneği, Excel için belge düzeyindeki bir projede bunu gösterir. <xref:Microsoft.Office.Tools.Excel.ListObject> Kod, <xref:Microsoft.Office.Interop.Excel.ListObject> sınıfında varolan bir adı `MyListObject` temel alan dinamik bir dinamik oluşturur. `Sheet1`

[!code-csharp[Trin_ExcelWorkbookDynamicControls#6](../vsto/codesnippet/CSharp/trin_excelworkbookdynamiccontrols4/Sheet1.cs#6)]
[!code-vb[Trin_ExcelWorkbookDynamicControls#6](../vsto/codesnippet/VisualBasic/trin_excelworkbookdynamiccontrols4/Sheet1.vb#6)]

### <a name="re-create-chart"></a>Grafiği yeniden oluştur

Bir <xref:Microsoft.Office.Tools.Excel.Chart?displayProperty=fullName> konak denetimini yeniden oluşturmak için önce yerel <xref:Microsoft.Office.Interop.Excel.Chart?displayProperty=fullName>' i silmeniz ve <xref:Microsoft.Office.Tools.Excel.Chart?displayProperty=fullName> ardından <xref:Microsoft.Office.Tools.Excel.ControlCollection.AddChart%2A> yöntemini kullanarak yeniden oluşturmanız gerekir. `Add`Mevcut bir *Denetim sınıfı*yoktur, bu, \<var olan <xref:Microsoft.Office.Interop.Excel.Chart?displayProperty=fullName>bir temel oluşturmaya göre <xref:Microsoft.Office.Tools.Excel.Chart?displayProperty=fullName> yeni bir oluşturma yöntemi >.

Önce yerel <xref:Microsoft.Office.Interop.Excel.Chart>' i silmeyin, yeniden <xref:Microsoft.Office.Tools.Excel.Chart?displayProperty=fullName>oluşturduğunuzda ikinci ve yinelenen bir grafik oluşturacaksınız.

## <a name="persist-windows-forms-controls-in-documents"></a>Belgelerde Windows Forms denetimleri Sürdür

Bir belge kaydedilip sonra kapatıldığında [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] , dinamik olarak oluşturulan Windows Forms denetimleri belgeden otomatik olarak kaldırır. Ancak, davranış belge düzeyi ve VSTO eklenti projeleri için farklıdır.

Belge düzeyi özelleştirmelerde, denetimler ve temel alınan ActiveX sarmalayıcıları (belge üzerinde denetimleri barındırmak için kullanılır) belge bir dahaki sefer açıldığında kaldırılır. Denetimlerin orada olduğunu belirten bir belirti yoktur.

VSTO eklentilerde denetimler kaldırılır, ancak ActiveX sarmalayıcıları belgede kalır. Kullanıcının belgeyi bir sonraki açışında, ActiveX sarmalayıcıları görünür. Excel 'de, ActiveX sarmalayıcıları denetimlerin görüntülerini belgenin kaydedildiği son zamanda göründüğü şekilde görüntüler. Word 'de, Kullanıcı onlara tıklamadığı müddetçe ActiveX sarmalayıcıları görünmez, bu durumda denetimlerin kenarlığını temsil eden noktalı bir çizgi görüntülenir. ActiveX sarmalayıcıları kaldırmak için çeşitli yollar vardır. Daha fazla bilgi için bkz. [eklentideki ActiveX sarmalayıcıları kaldırma](#removingActiveX).

### <a name="re-create-windows-forms-controls-when-documents-are-opened"></a>Belgeler açıldığında Windows Forms denetimleri yeniden oluştur

Kullanıcı belgeyi yeniden açtığında silinen Windows Forms denetimlerini yeniden oluşturabilirsiniz. Bunu yapmak için çözümünüzün aşağıdaki görevleri gerçekleştirmesi gerekir:

1. Belge kaydedildiğinde veya kapatıldığında denetimlerin boyut, konum ve durumuyla ilgili bilgileri depolayın. Belge düzeyi özelleştirmesinde verileri belgedeki veri önbelleğine kaydedebilirsiniz. Bir VSTO eklentisi içinde, verileri belgedeki özel bir XML bölümüne kaydedebilirsiniz.

2. Belge açıldığında oluşturulan bir olayda denetimleri yeniden oluşturun. Belge düzeyi projelerinde `Sheet`bunu *n* `_Startup` veya `ThisDocument_Startup` olay işleyicilerinde yapabilirsiniz. VSTO eklenti projelerinde, <xref:Microsoft.Office.Interop.Excel.AppEvents_Event.WorkbookOpen> veya <xref:Microsoft.Office.Interop.Word.ApplicationEvents4_Event.DocumentOpen> olayları için olay işleyicilerinde bunu yapabilirsiniz.

### <a name="removingActiveX"></a>Bir eklentideki ActiveX sarmalayıcılarını kaldırma

Bir VSTO eklentisini kullanarak belgelere dinamik Windows Forms denetimleri eklediğinizde, denetimlerin ActiveX sarmalayıcılarını bir sonraki sefer açıldığında belgede görünmesini engelleyebilirsiniz.

#### <a name="remove-activex-wrappers-when-the-document-is-opened"></a>Belge açıldığında ActiveX sarmalayıcıları 'nı kaldır

Tüm ActiveX sarmalayıcılarını kaldırmak için, `GetVstoObject` yeni açılan belgeyi temsil eden <xref:Microsoft.Office.Interop.Word.Document> veya <xref:Microsoft.Office.Interop.Excel.Workbook> için bir konak öğesi oluşturmak üzere yöntemini çağırın. Örneğin, bir Word belgesinden tüm ActiveX sarmalayıcılarını kaldırmak için, `GetVstoObject` <xref:Microsoft.Office.Interop.Word.ApplicationEvents4_Event.DocumentOpen> olayı için olay işleyicisine geçirilen <xref:Microsoft.Office.Interop.Word.Document> nesne için bir konak öğesi oluşturmak üzere yöntemini çağırabilirsiniz.

Bu yordam, belgenin yalnızca VSTO eklentisinin yüklü olduğu bilgisayarlarda açılacağını bildiğiniz durumlarda faydalıdır. Belge, VSTO eklentisinin yüklü olmadığı diğer kullanıcılara geçirilmemişse, bunun yerine Belgeyi kapatmadan önce denetimleri kaldırmayı göz önünde bulundurun.

Aşağıdaki kod örneği, belge açıldığında `GetVstoObject` yönteminin nasıl çağrılacağını gösterir.

[!code-vb[Trin_WordAddInDynamicControls#11](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#11)]
[!code-csharp[Trin_WordAddInDynamicControls#11](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#11)]

`GetVstoObject` Yöntemi, birincil olarak çalışma zamanında yeni bir konak öğesi oluşturmak için kullanılsa da bu yöntem, belirli bir belge için ilk çağrılışında belgedeki tüm ActiveX sarmalayıcılarını da temizler. `GetVstoObject` Yönteminin nasıl kullanılacağı hakkında daha fazla bilgi için bkz. [çalışma zamanında VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

VSTO eklentisi belge açıldığında dinamik denetimler oluşturursa, VSTO eklentisi, denetimleri oluşturma işleminin bir parçası olarak `GetVstoObject` yöntemi zaten çağıracaktır. Bu senaryodaki ActiveX sarmalayıcıları kaldırmak için `GetVstoObject` yöntemine ayrı bir çağrı eklemeniz gerekmez.

#### <a name="remove-the-dynamic-controls-before-the-document-is-closed"></a>Belge kapatılmadan önce dinamik denetimleri kaldırın

Belge kapatılmadan önce, VSTO eklentisi her dinamik denetimi belgeden açıkça kaldırabilir. Bu yordam, VSTO eklentisi yüklü olmayan diğer kullanıcılara geçirilebilecek belgeler için yararlıdır.

Aşağıdaki kod örneği, belge kapatıldığında bir Word belgesinden tüm Windows Forms denetimlerinin nasıl kaldırılacağını gösterir.

[!code-vb[Trin_WordAddInDynamicControls#10](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#10)]
[!code-csharp[Trin_WordAddInDynamicControls#10](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#10)]

## <a name="see-also"></a>Ayrıca bkz.

- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
