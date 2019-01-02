---
title: 'Nasıl Yapılır: Excel aralıklarına program aracılığıyla renk uygulama'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- formatting [Office development in Visual Studio]
- color, Excel ranges
- ranges, applying color
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 4cd8a9528b0bcd360fd00f700172899f1480d0ed
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53868030"
---
# <a name="how-to-programmatically-apply-color-to-excel-ranges"></a>Nasıl Yapılır: Excel aralıklarına program aracılığıyla renk uygulama
  Metin bir hücre aralığı içinde bir renk uygulamak için kullanmak bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi veya yerel Excel range nesnesi.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="use-a-namedrange-control"></a>NamedRange denetimi kullanma  
 Bu örnek için belge düzeyi özelleştirmeleri içindir.  
  
### <a name="to-apply-color-to-a-namedrange-control"></a>Renk NamedRange denetimine uygulamak için  
  
1.  Oluşturma bir <xref:Microsoft.Office.Tools.Excel.NamedRange> hücre A1 denetimi.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#65](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#65)]
     [!code-vb[Trin_VstcoreExcelAutomation#65](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#65)]  
  
2.  Metin rengini ayarlama <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#66](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#66)]
     [!code-vb[Trin_VstcoreExcelAutomation#66](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#66)]  
  
## <a name="use-native-excel-ranges"></a>Yerel Excel aralıkları kullanın  
  
### <a name="to-apply-color-to-a-native-excel-range-object"></a>Yerel bir Excel aralık nesnesi için renk uygulamak için  
  
1.  Hücre A1, bir aralık oluşturun ve sonra metnin rengini ayarlayın.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#67](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#67)]
     [!code-vb[Trin_VstcoreExcelAutomation#67](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#67)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Aralıklarla çalışma](../vsto/working-with-ranges.md)   
 [NamedRange denetimi](../vsto/namedrange-control.md)   
 [Nasıl yapılır: Program aracılığıyla çalışma kitaplarındaki aralıklara biçimler uygulama](../vsto/how-to-programmatically-apply-styles-to-ranges-in-workbooks.md)   
 [Nasıl yapılır: Koddaki çalışma sayfası aralıklarına program aracılığıyla bakma](../vsto/how-to-programmatically-refer-to-worksheet-ranges-in-code.md)   
 [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)  
