---
title: 'Nasıl Yapılır: Program aracılığıyla çalışma sayfası hücresinde bir dizeyi görüntüleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- text [Office development in Visual Studio], adding to worksheets
- worksheets, displaying text in cells
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 021fe02e501fc5a8921ec8f2a50329653ca45401
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53849774"
---
# <a name="how-to-programmatically-display-a-string-in-a-worksheet-cell"></a>Nasıl Yapılır: Program aracılığıyla çalışma sayfası hücresinde bir dizeyi görüntüleme
  Bu örnek, bir hücresinde program aracılığıyla metin görüntüleme gösterilmiştir. Metni hücrede görüntülemek için kullanın bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi veya yerel Excel range nesnesi.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="use-a-namedrange-control"></a>NamedRange denetimi kullanma  
 Bu örnekte bir <xref:Microsoft.Office.Tools.Excel.NamedRange> adlı Denetim `message`. Tasarım zamanında bir belge düzeyi özelleştirmesi için bir denetim eklenmesi gerekir. Aşağıdaki kod, bir sayfa sınıfında değil yerleştirilmelidir `ThisWorkbook` sınıfı.  
  
### <a name="to-display-text-in-a-namedrange-control"></a>NamedRange denetimi metni görüntülemek için  
  
1.  Değerini <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimini **Hello World**.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#68](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#68)]
     [!code-vb[Trin_VstcoreExcelAutomation#68](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#68)]  
  
## <a name="use-a-native-excel-range"></a>Yerel bir Excel aralığı kullanın  
 Aşağıdaki kod, program aracılığıyla yeni bir aralık oluşturur ve bir değer atar.  
  
### <a name="to-display-text-in-an-excel-range"></a>Excel aralığında metni görüntülemek için  
  
1.  Hücre aralığı almak **A1** üzerinde `Sheet1` ve değerine **Hello World**.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#69](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#69)]
     [!code-vb[Trin_VstcoreExcelAutomation#69](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#69)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [İzlenecek yol: Bir Windows formu kullanarak veri toplama](../vsto/walkthrough-collecting-data-using-a-windows-form.md)   
 [Office çözümlerinde sorun giderme](../vsto/troubleshooting-office-solutions.md)   
 [NamedRange denetimi](../vsto/namedrange-control.md)   
 [Office projelerindeki nesnelere genel erişim](../vsto/global-access-to-objects-in-office-projects.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)  
