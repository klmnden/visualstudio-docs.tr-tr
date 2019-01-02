---
title: XmlMappedRange denetimi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- XMLMappedRange control, data binding
- XMLMappedRange control
- XMLMappedRange control, events
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: f19bf36b145a5f2c1b4e841a96cdd485a0fb6ac1
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53946710"
---
# <a name="xmlmappedrange-control"></a>XmlMappedRange denetimi
  <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> Yalnızca yinelenmeyen bir şema öğesine Microsoft Office Excel'de eşlendiğinde oluşturan bir aralık denetimidir. Örneğin, `maxOccurs` bir şema öğesinin özniteliği, 1 değerine eşittir. Visual Studio XML eşlenmiş aralığı oluşturduktan sonra Excel nesne modeline geçiş yapmak zorunda kalmadan doğrudan karşı programlama yapabilirsiniz. Yalnızca silebilirsiniz bir <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> öğe eşlemesi kaldırıldığında Excel'den denetimi.  
  
 [!INCLUDE[appliesto_xlalldoc](../vsto/includes/appliesto-xlalldoc-md.md)]  
  
 ![video bağlantı](../vsto/media/playvideo.gif "video bağlantı") ilgili video gösterimi için bkz. [nasıl yaparım? XML eşleme Excel'de kullanılsın mı? ](http://go.microsoft.com/fwlink/?LinkID=130288).  
  
## <a name="bind-data-to-the-control"></a>Veriyi denetime bağlama  
 Bir <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> denetimi bağlama için tek bir veri alanı (Basit veri bağlama) destekler. <xref:Microsoft.Office.Tools.Excel.ListObject> Denetimi karmaşık veri bağlamayı destekler ve yinelenen bir şema öğesine bir hücreye eşlendiğinde otomatik olarak oluşturulur. Daha fazla bilgi için [ListObject denetimine](../vsto/listobject-control.md).  
  
 <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> Denetimi kullanarak bir veri kaynağına bağlı <xref:System.Windows.Forms.Control.DataBindings%2A> özelliği. Olduğunda bir <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> eklenen bir çalışma sayfası hücresi, Visual Studio otomatik olarak eşlenen hücreleri verilerinden bir veri kümesi oluşturur ve denetimi bu veri kümesine bağlar. Varsayılan veri bağlama özelliğini <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> olduğu <xref:Microsoft.Office.Tools.Excel.XmlMappedRange.Value2%2A>.  
  
 Herhangi bir mekanizma aracılığıyla ilişkili veri kümesindeki veriler güncelleştirilirse <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> denetimi değişiklikleri yansıtır.  
  
## <a name="formatting"></a>Biçimlendirme  
 Aynı biçimlendirme için uygulayabileceğiniz bir <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> uygulayabileceğiniz denetimi bir <xref:Microsoft.Office.Interop.Excel.Range>. Bu, kenarlık, yazı tipleri, sayı biçimini ve stilleri içerir.  
  
## <a name="events"></a>Olaylar  
 İçin kullanılabilir olan olaylar <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> denetimi:  
  
-   <xref:Microsoft.Office.Tools.Excel.XmlMappedRange.BeforeDoubleClick>  
  
-   <xref:Microsoft.Office.Tools.Excel.XmlMappedRange.BeforeRightClick>  
  
-   <xref:Microsoft.Office.Tools.Excel.XmlMappedRange.BindingContextChanged>  
  
-   <xref:Microsoft.Office.Tools.Excel.XmlMappedRange.Change>  
  
-   <xref:Microsoft.Office.Tools.Excel.XmlMappedRange.Selected>  
  
-   <xref:Microsoft.Office.Tools.Excel.XmlMappedRange.Deselected>  
  
-   <xref:System.ComponentModel.Component.Disposed>  
  
-   <xref:Microsoft.Office.Tools.Excel.XmlMappedRange.SelectionChange>  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)   
 [Nasıl yapılır: Çalışma sayfalarına XMLMappedRange denetimleri ekleme](../vsto/how-to-add-xmlmappedrange-controls-to-worksheets.md)   
 [Office çözümlerinde denetimlere veri bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)   
 [Nasıl yapılır: Şemaları Visual Studio içindeki çalışma sayfalarıyla eşleştirme](../vsto/how-to-map-schemas-to-worksheets-inside-visual-studio.md)   
 [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)  
