---
title: Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office documents [Office development in Visual Studio, host controls
- application development [Office development in Visual Studio], host items
- Office applications [Office development in Visual Studio], host items
- host items [Office development in Visual Studio], programmatic limitations
- Excel [Office development in Visual Studio], host items
- host controls [Office development in Visual Studio], creating
- document-level customizations [Office development in Visual Studio], host controls
- Office applications [Office development in Visual Studio], host controls
- documents [Office development in Visual Studio], host controls
- controls [Office development in Visual Studio], host controls
- host controls [Office development in Visual Studio], passing to methods and properties
- application development [Office development in Visual Studio], host controls
- Excel [Office development in Visual Studio], host controls
- host controls [Office development in Visual Studio], programmatic limitations
- documents [Office development in Visual Studio], host items
- Office documents [Office development in Visual Studio, host items
- Word [Office development in Visual Studio], host items
- document-level customizations [Office development in Visual Studio], host items
- Word [Office development in Visual Studio], host controls
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: facf78a9c737dbaa0d3a48e93d8424d5288f683a
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54865469"
---
# <a name="programmatic-limitations-of-host-items-and-host-controls"></a>Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları
  Her bir ana bilgisayar öğesi ve konak kontrolü ek işlevlere sahip karşılık gelen yerel Microsoft Office Word veya Microsoft Office Excel nesnesi gibi davranacak şekilde tasarlanmıştır. Ancak, konak denetimlerinin ve konak öğelerinin davranışını ve çalışma zamanında yerel Office nesneler arasındaki bazı temel farklar vardır.  
  
 Konak denetimlerinin ve konak öğeleri hakkında genel bilgi için bkz. [konak öğelerini ve denetimlerine genel bakış için ana bilgisayar](../vsto/host-items-and-host-controls-overview.md).  
  
 [!INCLUDE[appliesto_controls](../vsto/includes/appliesto-controls-md.md)]  
  
## <a name="programmatically-create-host-items"></a>Program aracılığıyla ana bilgisayar öğeleri oluşturma  
 Program aracılığıyla oluşturma veya Word veya Excel nesne modelini kullanarak bir belge, çalışma kitabı veya çalışma zamanında açın, öğe konak öğesi değil. Bunun yerine, yeni bir yerel Office nesne nesnedir. Örneğin kullanırsanız <xref:Microsoft.Office.Interop.Word.Documents.Add%2A> yöntemi, yeni bir Word belgesi oluşturmak için çalışma zamanında, yerel olacaktır <xref:Microsoft.Office.Interop.Word.Document> nesne yerine <xref:Microsoft.Office.Tools.Word.Document> konak öğesi. Benzer şekilde, oluşturduğunuzda, yeni bir çalışma zamanında kullanarak <xref:Microsoft.Office.Interop.Excel.Worksheets.Add%2A> yöntemi, bir yerel alma <xref:Microsoft.Office.Interop.Excel.Worksheet> nesne yerine <xref:Microsoft.Office.Tools.Excel.Worksheet> konak öğesi.  
  
 Belge düzeyinde projelerde, çalışma zamanında bir ana bilgisayar öğeleri oluşturamazsınız. Konak öğeleri yalnızca belge düzeyinde projeler tasarım zamanında oluşturulabilir. Daha fazla bilgi için [belge konak öğesi](../vsto/document-host-item.md), [çalışma kitabı konak öğesi](../vsto/workbook-host-item.md), ve [çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md).  
  
 VSTO eklenti projesinde oluşturduğunuz <xref:Microsoft.Office.Tools.Word.Document>, <xref:Microsoft.Office.Tools.Excel.Workbook>, veya <xref:Microsoft.Office.Tools.Excel.Worksheet> öğelerinin çalışma zamanında barındırın. Daha fazla bilgi için [genişletmek Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında VSTO Add-Ins](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).  
  
## <a name="programmatically-create-host-controls"></a>Konak denetimleri program aracılığıyla oluşturma  
 Konak denetimleri program aracılığıyla ekleyebilirsiniz bir <xref:Microsoft.Office.Tools.Word.Document> veya <xref:Microsoft.Office.Tools.Excel.Worksheet> çalışma zamanında konak öğesi. Daha fazla bilgi için [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).  
  
 Konak denetimleri yerel eklenemiyor <xref:Microsoft.Office.Interop.Word.Document> veya <xref:Microsoft.Office.Interop.Excel.Worksheet>.  
  
> [!NOTE]  
>  Aşağıdaki konak denetimleri, program aracılığıyla çalışma sayfaları veya belgeler için eklenemiyor: <xref:Microsoft.Office.Tools.Excel.XmlMappedRange>, <xref:Microsoft.Office.Tools.Word.XMLNode>, ve <xref:Microsoft.Office.Tools.Word.XMLNodes>.  
  
## <a name="understand-type-differences-between-host-items-host-controls-and-native-office-objects"></a>Konak öğeleri, konak denetimleri ve yerel Office nesneler arasındaki türü farkları  
 Her ana bilgisayar öğesi ve konak kontrolü için temel alınan yerel Microsoft Office Word veya Microsoft Office Excel nesne yok. Temel alınan nesnede konak öğesi ya da konak kontrolü InnerObject özelliğini kullanarak erişebilirsiniz. Ancak, yerel bir Office nesnesi kendi ilgili konak öğesi ya da konak kontrolü hiçbir yolu yoktur. Yerel bir Office nesne türüne bir ana bilgisayar öğesi ya da konak kontrolü dönüştürmeyi denerseniz bir <xref:System.InvalidCastException> oluşturulur.  
  
 Konak denetimlerinin ve konak öğelerinin türlerini ve temel alınan yerel Office nesneler arasındaki farklar kodunuzu nereye etkileyebilir birkaç senaryo mevcuttur.  
  
### <a name="pass-host-controls-to-methods-and-properties"></a>Konak denetimleri yöntemleri ve özellikleri geçirme  
 Word'de bir yöntem veya bir parametre olarak yerel bir Word nesne gerektiren bir özellik için bir konak kontrolü geçiremezsiniz. Temel alınan yerel Word nesneyi döndürmek için konak kontrolü InnerObject özelliğini kullanmanız gerekir. Örneğin, geçirebilirsiniz bir <xref:Microsoft.Office.Interop.Word.Bookmark> nesnesi geçirerek bir yönteme <xref:Microsoft.Office.Tools.Word.Bookmark.InnerObject%2A> özelliği <xref:Microsoft.Office.Tools.Word.Bookmark> konak kontrolü yöntemi.  
  
 Excel'de, yöntemi veya özelliği Excel nesnesini beklerken bir yöntem veya özellik için konak kontrolü geçirmek için konak kontrolü InnerObject özelliğini kullanmanız gerekir.  
  
 Aşağıdaki örnek, oluşturur bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetlemek ve buna ileten <xref:Microsoft.Office.Interop.Excel.Range.AutoFill%2A> yöntemi. Kod <xref:Microsoft.Office.Tools.Excel.NamedRange.InnerObject%2A> temel alınan Office döndürülecek adlandırılmış aralık özelliği <xref:Microsoft.Office.Interop.Excel.Range> tarafından gerekli <xref:Microsoft.Office.Interop.Excel.Range.AutoFill%2A> yöntemi.  
  
 [!code-csharp[Trin_VstcoreHostControlsExcel#28](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#28)]
 [!code-vb[Trin_VstcoreHostControlsExcel#28](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#28)]  
  
### <a name="return-types-of-native-office-methods-and-properties"></a>Dönüş türleri yerel Office yöntemleri ve özellikleri  
 Birçok yöntem ve konak öğelerinin özelliklerini temel aldığı konak öğesi üzerinde yerel Office nesnesini döndürür. Örneğin, <xref:Microsoft.Office.Tools.Excel.NamedRange.Parent%2A> özelliği bir <xref:Microsoft.Office.Tools.Excel.NamedRange> konak kontrolü Excel döndürür bir <xref:Microsoft.Office.Interop.Excel.Worksheet> nesne yerine <xref:Microsoft.Office.Tools.Excel.Worksheet> konak öğesi. Benzer şekilde, <xref:Microsoft.Office.Tools.Word.RichTextContentControl.Parent%2A> özelliği bir <xref:Microsoft.Office.Tools.Word.RichTextContentControl> konak kontrolü Word döndürür bir <xref:Microsoft.Office.Interop.Word.Document> nesne yerine <xref:Microsoft.Office.Tools.Word.Document> konak öğesi.  
  
### <a name="access-collections-of-host-controls"></a>Konak denetimleri erişim koleksiyonları  
 [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] Tek koleksiyonlar, her ana denetim türü için sağlamaz. Bunun yerine, tüm yönetilen denetimleri (konak denetimleri ve Windows Forms denetimleri) belge veya çalışma sayfası üzerinde yinelemek için konak öğesi denetimleri özelliğini kullanın ve ilginizi çeken ana denetim türü eşleşen öğeleri bulun. Aşağıdaki kod örneği bir Word belgesi her denetim incelenir ve denetimin olup olmadığını belirleyen bir <xref:Microsoft.Office.Tools.Word.Bookmark>.  
  
 [!code-csharp[Trin_VstcoreHostControlsWord#10](../vsto/codesnippet/CSharp/trin_vstcorehostcontrolsword/ThisDocument.cs#10)]
 [!code-vb[Trin_VstcoreHostControlsWord#10](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsWordVB/ThisDocument.vb#10)]  
  
 Ana bilgisayar öğesi denetimleri özelliği hakkında daha fazla bilgi için bkz. [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).  
  
 Word ve Excel nesne modelleri, belge ve çalışma yerel denetimlerin koleksiyonlarını açığa çıkarır özellikleri içerir. Bu özellikleri kullanarak yönetilen denetimleri erişemez. Örneğin, her numaralandırmak mümkün değildir <xref:Microsoft.Office.Tools.Word.Bookmark> kullanarak ana bilgisayar denetimi belgede <xref:Microsoft.Office.Interop.Word._Document.Bookmarks%2A> özelliği bir <xref:Microsoft.Office.Interop.Word.Document> veya <xref:Microsoft.Office.Tools.Word.Document.Bookmarks%2A> özelliği bir <xref:Microsoft.Office.Tools.Word.Document>. Bu özellikler yalnızca dahil <xref:Microsoft.Office.Interop.Word.Bookmark> denetimlerini belgede; bunlar içermeyen <xref:Microsoft.Office.Tools.Word.Bookmark> konak denetimlerini belgedeki.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)   
 [Genişletilmiş nesneleri kullanarak Word'ü otomatikleştirirken](../vsto/automating-word-by-using-extended-objects.md)   
 [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)   
 [Çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md)   
 [Çalışma kitabı konak öğesi](../vsto/workbook-host-item.md)   
 [Belge konak öğesi](../vsto/document-host-item.md)  
