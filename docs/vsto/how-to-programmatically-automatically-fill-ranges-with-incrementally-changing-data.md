---
title: 'Nasıl yapılır: Program aracılığıyla otomatik biçimde aralıkları artımlı şekilde değişen verilerle ile doldurun.'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Autofill method [Excel]
- filling ranges automatically
- ranges, automatically filling
- workbooks, filling ranges
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 867f59c04e9d0f99b36e6a067ad9a5cbc1041f46
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54088328"
---
# <a name="how-to-programmatically-automatically-fill-ranges-with-incrementally-changing-data"></a>Nasıl yapılır: Program aracılığıyla otomatik biçimde aralıkları artımlı şekilde değişen verilerle ile doldurun.
  <xref:Microsoft.Office.Interop.Excel.Range.AutoFill%2A> Yöntemi <xref:Microsoft.Office.Interop.Excel.Range> nesne değerlerle otomatik olarak çalışma sayfasındaki bir aralığı doldurmanıza olanak sağlar. Çoğu zaman <xref:Microsoft.Office.Interop.Excel.Range.AutoFill%2A> yöntemi artımlı olarak artan veya azalan bir aralıktaki değerleri depolamak için kullanılır. Gelen isteğe bağlı bir sabit sağlanarak davranış belirtebilirsiniz <xref:Microsoft.Office.Interop.Excel.XlAutoFillType> sabit listesi.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
 İki aralık kullanırken belirtmelisiniz <xref:Microsoft.Office.Interop.Excel.Range.AutoFill%2A>:  
  
-   Çağıran aralık <xref:Microsoft.Office.Interop.Excel.Range.AutoFill%2A> dolgu başlangıç noktasını belirtir ve bir başlangıç değeri içeren yöntemi.  
  
-   Bir parametre olarak geçirilen doldurmak istediğiniz aralık <xref:Microsoft.Office.Interop.Excel.Range.AutoFill%2A> yöntemi. Hedef aralığın başlangıç değeri içeren aralığını içermelidir.  
  
    > [!NOTE]  
    >  Geçiremezsiniz bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi <xref:Microsoft.Office.Interop.Excel.Range>. Daha fazla bilgi için [konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md).  
  
## <a name="example"></a>Örnek  
 [!code-csharp[Trin_VstcoreExcelAutomation#49](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#49)]
 [!code-vb[Trin_VstcoreExcelAutomation#49](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#49)]  
  
## <a name="compile-the-code"></a>Kod derleme  
 İlk hücrenin doldurmak istediğiniz aralığın başlangıç değeri içermelidir.  
  
 Örnek, üç bölgeleri dolgu gerektirir:  
  
-   Sütun B beş iş günü eklemektir. Başlangıç değeri için tür **Pazartesi** B1 hücresine.  
  
-   Sütun C'yi, beşinci aya dahil etmektir. Başlangıç değeri için tür **Ocak** hücresinde C1.  
  
-   Sütun D numaraları, iki her satır için artan bir dizi eklemektir. Başlangıç değerleri için tür **4** D1 hücresinde ve **6** D2 hücresine.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Aralıklarla çalışma](../vsto/working-with-ranges.md)   
 [Nasıl yapılır: Koddaki çalışma sayfası aralıklarına program aracılığıyla bakma](../vsto/how-to-programmatically-refer-to-worksheet-ranges-in-code.md)   
 [Nasıl yapılır: Program aracılığıyla çalışma kitaplarındaki aralıklara biçimler uygulama](../vsto/how-to-programmatically-apply-styles-to-ranges-in-workbooks.md)   
 [Nasıl yapılır: Program aracılığıyla Excel hesapları çalıştırma](../vsto/how-to-programmatically-run-excel-calculations-programmatically.md)   
 [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)  
