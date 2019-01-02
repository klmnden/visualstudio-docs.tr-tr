---
title: Office belgelerindeki Windows Forms denetimleri sınırlamaları
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office documents [Office development in Visual Studio, Windows Forms controls
- Windows Forms controls [Office development in Visual Studio], ActiveX legacy
- ActiveX controls [Office development in Visual Studio]
- Windows Forms controls [Office development in Visual Studio], limitations
- controls [Office development in Visual Studio], Windows Forms controls
- Windows Forms controls [Office development in Visual Studio], unsupported properties and methods
- Toolbox [Office development in Visual Studio], unsupported controls
- user controls [Office development in Visual Studio], grouping controls
- Windows Forms controls [Office development in Visual Studio], Toolbox
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 1e3ea01d83dcb40378e3ac3282d95620eacc5731
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53929678"
---
# <a name="limitations-of-windows-forms-controls-on-office-documents"></a>Office belgelerindeki Windows Forms denetimleri sınırlamaları

Microsoft Office Word belgelerine veya Microsoft Office Excel çalışma sayfalarına eklenmiş Windows Forms denetimleri ve Windows Forms için eklenen Windows Formları arasında bazı farklar vardır. Örneğin, eklediğinizde bir <xref:Microsoft.Office.Tools.Word.Controls.Button> gibi bir belge, özellikleri denetlemek <xref:System.Windows.Forms.Control.Dock>, <xref:System.Windows.Forms.Control.Anchor>, ve <xref:System.Windows.Forms.Control.TabIndex> bekleyebileceğiniz gibi davranmayabilir.

Bu gibi durumlarda bu farklılıkların birçoğu, Windows Forms denetimleri barındırılan şekilde belgelerde kaynaklanır. Bir Windows Forms denetimini bir belgeye eklendiğinde [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] belge Windows Forms denetiminde'ı barındıran bir ActiveX denetimi ekler. Windows Forms denetimi doğrudan belge içinde gömülü.

[!INCLUDE[appliesto_controls](../vsto/includes/appliesto-controls-md.md)]

## <a name="limitations-of-methods-and-properties-of-windows-forms-controls"></a>Yöntemleri ve özellikleri Windows Forms denetimleri sınırlamaları

Bir dizi yöntem ve aynı şekilde bir Windows formunda yaptıkları ve bu nedenle, bunlar kullanılmaması önerilir gibi bir belgeyi çalışmaz Windows Forms denetimlerindeki özellikler vardır. Örneğin, gibi özellikleri ayarlamak <xref:System.Windows.Forms.Control.Dock> ve <xref:System.Windows.Forms.Control.Anchor> yalnızca belge yerine kapsayıcı ActiveX denetimi ile ilgili denetimin konumunu etkiler. Desteklenmeyen yöntem ve özellikleri Word ve Excel için Windows Forms denetimlerinin listesi verilmiştir:

- Excel denetimleri desteklenmeyen özellikler:

    - <xref:System.Windows.Forms.Control.Anchor>
    - <xref:System.Windows.Forms.Control.Dock>
    - <xref:System.Windows.Forms.Control.Location>
    - <xref:System.Windows.Forms.Control.TabIndex>
    - <xref:System.Windows.Forms.Control.TabStop>
    - <xref:System.Windows.Forms.Control.TopLevelControl>

- Desteklenmeyen yöntem ve özellikleri Word denetimleri:

    - <xref:System.Windows.Forms.Control.Hide%2A>
    - <xref:System.Windows.Forms.Control.Show%2A>
    - <xref:System.Windows.Forms.Control.Anchor>
    - <xref:System.Windows.Forms.Control.Dock>
    - <xref:System.Windows.Forms.Control.Location>
    - <xref:System.Windows.Forms.Control.TabIndex>
    - <xref:System.Windows.Forms.Control.TabStop>
    - <xref:System.Windows.Forms.Control.TopLevelControl>
    - <xref:System.Windows.Forms.Control.Visible>

Ayarlayamazsınız <xref:System.Windows.Forms.Control.Left> veya <xref:System.Windows.Forms.Control.Top> bir Word belgesinde metinde olan Windows Forms denetimlerinin özelliği. Windows Forms denetimleri, metin aşağıdaki durumlarda uygun olarak eklenir:

- Program aracılığıyla bir Word belgesi için denetim ekleme ve konum için bir aralık belirten bir yöntem kullanın.

- Tasarım zamanında bir Word belgesi için bir Windows Forms denetimi ekleyin. Bu tasarımcıda bir denetime değiştirerek değiştirebilirsiniz.

## <a name="differences-in-windows-forms-controls-on-office-documents"></a>Office belgelerindeki Windows Forms denetimleri farklılıkları

Windows Forms denetimleri genellikle aynı davranışı bir Office belgesi üzerinde bir Windows formunda yaptıkları, ancak bazı farklılıklar da mevcut sahip. Aşağıdaki tabloda, Office belgelerindeki Windows Forms denetimleri için mevcut farklar açıklanmaktadır.

|İşlevi|Fark|
|-------------------|----------------|
|Sekme düzenini denetleme|Aracılığıyla bir Excel çalışma sayfası veya Word belgesi denetimlerin sekme olamaz.|
|Denetim gruplandırma|Kullanamazsınız bir <xref:System.Windows.Forms.GroupBox> diğer Office belgesinden denetimleri içermesi için denetimi. Belgeye birden çok radyo düğmeleri eklediğinizde, radyo düğmeleri birbirini dışlamaz. Radyo düğmeleri birbirini dışlayan yapmak için kod yazabilirsiniz; Ancak, tercih edilen bir kullanıcı denetimine radyo düğmeleri ekleme ve belgede kullanıcı denetimi eklemek için bir yaklaşımdır. Daha fazla bilgi için bkz: Word denetimleri örneği veya Excel denetimleri örneğini şurada [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md).|
|Denetim türü|Belgelerde kullanılan Windows Forms denetimleri tarafından sağlanan bir sınıftaki sarılır [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] Word belgesi ve Excel çalışma sayfası için ek işlevler belirli denetimler vermektedir. Örneğin, bir **düğmesi** türü olarak belirttiğinizden emin olun, denetim bir Excel çalışma sayfasında <xref:Microsoft.Office.Tools.Excel.Controls.Button> yerine <xref:System.Windows.Forms.Button> başvuru veya nesne atama.|
|Denetimin konumu ve boyutu|Denetim konumu ve boyutu ' % s'kapsayıcı ActiveX denetiminin bir parçası olan özellikleri tarafından belirlenir. ActiveX denetimi özelliklerini farklı değerler eşdeğer bir Windows Forms denetimi özelliklerinden yararlanın. Ayarladığınızda `Top`, `Left`, `Height`, veya `Width` denetimin özelliklerini, onu ölçülür, piksel yerine işaret eder.|
|Word belgesindeki denetimi konumu|Akış tabanlı bir düzene denetimleri eklerseniz, denetimler içeriğin bulunduğu içerik değiştikçe akar aklınızda bulundurun. Buradan sürüklediğinizde bir paragraf denetime bağlayamazsınız **araç kutusu** çünkü Word belgesine metinle denetim eklenir. Denetime çift gibi denetim eklemek için başka bir yöntem kullanırsanız, resim eklemek için ayarladığınız Word seçeneğe göre denetimi eklenir.<br /><br /> Ayarlayamazsınız `Left` veya `Top` satır içi metin ile denetimin özellik.<br /><br /> Üstbilgi ve altbilgisindeki veya bir alt denetimler yerleştiremezsiniz.|
|Denetim olayları|Bir Denetim seçildiğinde, olaylar aşağıdaki sırada oluşur:<br /><br /> 1.  `Enter`<br />2.  `GotFocus`<br /><br /> Denetim seçili olmadığında, olaylar aşağıdaki sırada oluşur:<br /><br /> 1.  `Leave`<br />2.  `Validating`<br />3.  `Validated`<br />4.  `LostFocus`|
|Denetimini ölçeklendirme|Bir belgenin yakınlaştırma ayarı % 100'den başka bir değere değiştirdiğinizde, bunlar görünmesine karşın denetimleri devre dışı bırakılır, belge ile ölçeklendirin. Örneğin, belgenizi %130 yakınlaştırma düzeyinde olduğunda bir düğmeye tıklarsanız, bir ileti gösterilir % 100 yakınlaştırma ayarlanana kadar denetim devre dışı olduğunu. % 100 yakınlaştırma değiştirdiğinizde denetimleri düzgün çalışmayacaktır.|
|Özellik değerlerini denetleme|Bir Windows formundaki denetimler özelliklerini tamsayı değerine ayarlanır olsa da, tek bir Word belgesi denetimleri için ayarlanır. Excel'de denetimleri özellik değerlerini bir çift olarak ayarlanır. Varsa `Height` ve `Width` özelliği çalışma sayfasındaki bir denetimin çalışma sayfası veya ekran boyutunu aşıyor, değer kesilir.|
|Denetimi yeniden boyutlandırma|Bir denetimde sekiz boyutlandırma tutamaçlarından birinin kullanarak belgeyi yeniden boyutlandırırsanız, yeni denetim boyutları yansıtılmaz **özellikleri** denetim yansıtımaz kadar penceresi.|
|Denetimin davranışı|Çalışma sayfası pencerenin ayrıldığında bir Excel çalışma sayfasındaki denetimleri beklenmedik şekilde davranabilir. Örneğin, erişimi bir <xref:Microsoft.Office.Tools.Excel.Controls.TextBox> çalışma sayfasında yalnızca windows biri mevcut olabilir.|
|Denetim adlandırma|Ayrılmış sözcükler adı denetimleri için kullanamazsınız. Örneğin eklerseniz, bir <xref:Microsoft.Office.Tools.Excel.Controls.Button> çalışma ve adla değiştirin **sistem**, projeyi oluşturduğunuzda hatalar oluşur.|
|Programlı olarak denetim ekleme|Denetimin Oluşturucusu belgenizi çalışma zamanında bir denetim eklemek için kullanmayın. Bunun yerine, tarafından sağlanan yardımcı yöntemler kullanın [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]. Örneğin, <xref:Microsoft.Office.Tools.Excel.ControlExtensions.AddButton%2A> çalışma sayfasına bir düğme eklemek için yöntemi. Bu yardımcı yöntemler tarafından desteklenmeyen bir denetim eklemek istiyorsanız, kullanabileceğiniz `AddControl` yöntemi. Daha fazla bilgi için [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).|
|Denetimleri kopyalama|Bir Windows Forms denetimini kopyalayın ve çalışma zamanında bir belgeye yapıştırın, boş bir kapsayıcı ActiveX denetimi belgeye yapıştırılır. Windows Forms denetimi yeni konuma görünmez ve özgün denetimin arka plan kod ActiveX denetimi kapsayıcısı için kopyalanmaz.|

## <a name="limitations-in-document-level-projects"></a>Belge düzeyi projelere sınırlamaları

Belgelerindeki Windows Forms denetimleri kullanarak bazı sınırlamaları için belge düzeyi projelerine özgüdür.

### <a name="control-support-at-design-time"></a>Tasarım zamanında denetimi desteği

Bazı Windows Forms denetimleri çıkarılır **araç kutusu** ne zaman bir Excel çalışma sayfası veya Word belgesi açıksa Visual Studio Tasarımcısı'nda. Bu teknik sınırlamaları nedeniyle, veya işlevi zaten Word veya Excel içinde kullanılabilir. Excel ve Word projelerini desteklemek tüm Windows Forms denetimleri ve görünen diğer bileşenleri **araç kutusu** zaman belge odağa sahip ve bir çalışma sayfası veya belge de üçüncü taraf denetimleri ekleyebilirsiniz.

> [!NOTE]
> Tüm denetimleri çıkarılır **araç kutusu** ne zaman bir belge korunur. Belge koruması hakkında daha fazla bilgi için bkz. [koruma belge düzeyi çözümlerde belge](../vsto/document-protection-in-document-level-solutions.md).

> [!NOTE]
> Üçüncü taraf denetimleri olmalıdır <xref:System.Runtime.InteropServices.ComVisibleAttribute> özniteliğini **true** Office çözümünü kullanılabilmesi için.

Aşağıdaki denetimleri ve bileşenleri kullanılabilir olmayan **araç kutusu**:

- <xref:System.Windows.Forms.BindingNavigator>

- <xref:System.Windows.Forms.ContextMenuStrip>

- <xref:System.Windows.Forms.DataGrid>

- <xref:System.DirectoryServices.DirectoryEntry>

- <xref:System.DirectoryServices.DirectorySearcher>

- <xref:System.Windows.Forms.ErrorProvider>

- <xref:System.Diagnostics.EventLog>

- <xref:System.IO.FileSystemWatcher>

- <xref:System.Windows.Forms.FlowLayoutPanel>

- <xref:System.Windows.Forms.GroupBox>

- <xref:System.Windows.Forms.MainMenu>

- <xref:System.Windows.Forms.MenuStrip>

- <xref:System.Messaging.MessageQueue>

- <xref:System.Windows.Forms.NotifyIcon>

- <xref:System.Windows.Forms.PageSetupDialog>

- <xref:System.Windows.Forms.Panel>

- <xref:System.Diagnostics.PerformanceCounter>

- <xref:System.Windows.Forms.PrintDialog>

- <xref:System.Drawing.Printing.PrintDocument>

- <xref:System.Windows.Forms.PrintPreviewControl>

- <xref:System.Diagnostics.Process>

- <xref:System.Windows.Forms.RichTextBox>

- <xref:System.IO.Ports.SerialPort>

- <xref:System.ServiceProcess.ServiceController>

- <xref:System.Windows.Forms.SplitContainer>

- <xref:System.Windows.Forms.Splitter>

- <xref:System.Windows.Forms.StatusBar>

- <xref:System.Windows.Forms.StatusStrip>

- <xref:System.Windows.Forms.TabControl>

- <xref:System.Windows.Forms.TableLayoutPanel>

- <xref:System.Timers.Timer>

- <xref:System.Windows.Forms.Timer>

- <xref:System.Windows.Forms.ToolBar>

- <xref:System.Windows.Forms.ToolStrip>

- <xref:System.Windows.Forms.ToolStripContainer>

- <xref:System.Windows.Forms.ToolStripDropDown>

- <xref:System.Windows.Forms.ToolStripDropDownMenu>

- <xref:System.Windows.Forms.ToolStripPanel>

### <a name="support-for-legacy-activex-controls"></a>Eski ActiveX denetimleri için desteği

ActiveX denetimlerini işlevselliğini kaybolmaz, mevcut bir Word belgesi veya ActiveX denetimlerini içeren Excel çalışma kitabı kullanan bir belge düzeyinde Office projesi oluşturursanız, Ancak, Visual Studio içinden belgelerinizi yeni ActiveX denetimleri ekleme desteği yoktur. Örneğin, Word belgesi bir düğmeyle varsa **denetimi** Visual Basic for Applications (VBA) makrosu araç kutusu, bu belge Office projeleri kullanıldıktan sonra makrosu çalışmaya devam edecek. Ancak, ActiveX denetimlerini ve VBA denetimlerini kaldırın ve bunları Windows Forms denetimleri ile değiştirin ve yönetilen kodla önerilir.

## <a name="see-also"></a>Ayrıca bkz.

- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Windows Forms denetimlerine Office belgeleri genel bakış](../vsto/windows-forms-controls-on-office-documents-overview.md)
- [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Nasıl yapılır: Office belgelerine Windows Forms denetimleri ekleme](../vsto/how-to-add-windows-forms-controls-to-office-documents.md)