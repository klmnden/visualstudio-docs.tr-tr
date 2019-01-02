---
title: Excel çalışma sayfalarında Windows Forms denetimlerini kullanma
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Windows Forms controls [Office development in Visual Studio], Excel
- Excel [Office development in Visual Studio], Windows Forms controls
- controls [Office development in Visual Studio], Window Forms controls
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: abc3e08a867af9b04d7ce1da1449f108a099b238
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53823425"
---
# <a name="use-windows-forms-controls-on-excel-worksheets"></a>Excel çalışma sayfalarında Windows Forms denetimlerini kullanma
  Windows Forms'a denetimler ekleme aynı şekilde, Windows Forms denetimleri için Microsoft Office Excel çalışma kitaplarınızı ekleyebilirsiniz. Belgelerindeki denetimler ile çalışma hakkında genel bilgi için bkz. [Windows Forms denetimleri Office belgeleri genel bakış](../vsto/windows-forms-controls-on-office-documents-overview.md).  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="control-considerations-for-excel"></a>Excel için Denetim konuları  
 Excel'e özgü birkaç nokta vardır.  
  
### <a name="match-control-size-to-cell-size"></a>Hücreyi boyuta denetim boyutu  
 Denetimin üst hücre boyutu değiştiğinde otomatik olarak yeniden boyutlandırılıp ayarlayabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Çalışma sayfası hücreleri içinde denetimleri yeniden boyutlandırma](../vsto/how-to-resize-controls-within-worksheet-cells.md).  
  
### <a name="add-components-that-are-shared-by-all-worksheets"></a>Tüm çalışma sayfalarını tarafından paylaşılan bileşenleri ekleme  
 Tüm çalışma sayfaları arasında gibi paylaşmak istediğiniz bileşenleri ekleyebileceğiniz bir <xref:System.Data.DataSet>, çalışma kitabı tasarımcısına çalışma sayfaları. Bileşen bileşen alanında görünür.  
  
### <a name="formula-for-embedding-controls"></a>Formül için denetimler ekleme  
 Excel'de bir denetimi seçtiğinizde göreceğiniz **=EMBED("WinForms.Control.Host","")** içinde **formül çubuğu**. Bu metin, gereklidir ve silinmemelidir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Çalışma sayfası hücreleri içinde denetimleri yeniden boyutlandırma](../vsto/how-to-resize-controls-within-worksheet-cells.md)   
 [Nasıl yapılır: Yazdırırken çalışma sayfası denetimlerini gizleme](../vsto/how-to-hide-controls-on-worksheets-when-printing.md)   
 [İzlenecek yol: CheckBox denetimlerini kullanarak çalışma sayfası biçimlendirmesini değiştirme](../vsto/walkthrough-changing-worksheet-formatting-using-checkbox-controls.md)   
 [İzlenecek yol: Düğme kullanarak çalışma sayfasındaki metin kutusunda metin görüntüleme](../vsto/walkthrough-displaying-text-in-a-text-box-in-a-worksheet-using-a-button.md)   
 [İzlenecek yol: Bir radyo düğmelerini kullanarak çalışma sayfasında grafik güncelleştir](../vsto/walkthrough-updating-a-chart-in-a-worksheet-using-radio-buttons.md)  
