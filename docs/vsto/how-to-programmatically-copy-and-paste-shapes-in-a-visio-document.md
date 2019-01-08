---
title: 'Nasıl yapılır: Program aracılığıyla kopyalayın ve bir Visio belgesinde şekiller yapıştırın'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- shapes [Office development in Visual Studio], copying and pasting Visio shapes
- Visio [Office development in Visual Studio], copying and pasting Visio shapes
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: b9b4f756c1b553f41f79dbbaaaf8a4c27bdfbc64
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54093957"
---
# <a name="how-to-programmatically-copy-and-paste-shapes-in-a-visio-document"></a>Nasıl yapılır: Program aracılığıyla kopyalayın ve bir Visio belgesinde şekiller yapıştırın
  Program aracılığıyla şekiller bir belgenin tek bir sayfada kopyalayabilir ve aynı belgede yeni bir sayfaya yapıştırın. Özgün sayfa üzerinde sahip oldukları gibi varsayılan konuma (etkin pencere Merkezi) veya aynı koordinat konumlarını bunları yapıştırın seçebilirsiniz.  
  
## <a name="copy-and-paste-shapes"></a>Kopyalama ve yapıştırma şekiller  
 Nesne modeli hakkında daha fazla ayrıntı için VBA başvuru belgelerine bakın [Microsoft.Office.Interop.Visio.Shape.DrawRectangle](/office/vba/api/Visio.Shape.DrawRectangle), [Microsoft.Office.Interop.Visio.Shape.DrawOval](/office/vba/api/Visio.Shape.DrawOval), [ Microsoft.Office.Interop.Visio.Shape.Copy](/office/vba/api/Visio.Shape.Copy), ve [Microsoft.Office.Interop.Visio.Shape.Paste](/office/vba/api/Visio.Shape.Paste) yöntemleri ve [ Microsoft.Office.Interop.Visio.VisCutCopyPasteCodes.visCopyPasteNormal](/office/vba/api/Visio.viscutcopypastecodes) bayrağı.  
  
### <a name="to-copy-shapes-to-the-center-of-another-page"></a>Başka bir sayfa merkezine şekiller kopyalamak için  
  
-   Aşağıdaki örnek, şekilleri ilk sayfadan kopyalayın ve ikinci sayfasında merkezini yapıştırın gösterilmektedir.  
  
     [!code-csharp[Trin_VstcoreVisioAutomationAddIn#14](../vsto/codesnippet/CSharp/trin_vstcorevisioautomationaddin/ThisAddIn.cs#14)]
     [!code-vb[Trin_VstcoreVisioAutomationAddIn#14](../vsto/codesnippet/VisualBasic/trin_vstcorevisioautomationaddin/ThisAddIn.vb#14)]  
  
## <a name="copy-and-paste-shapes-with-the-same-positions"></a>Kopyalama ve yapıştırma aynı konumlarla şekiller  
 Nesne modeli hakkında daha fazla ayrıntı için VBA başvuru belgelerine bakın [Microsoft.Office.Interop.Visio.Shape.DrawRectangle](/office/vba/api/Visio.Shape.DrawRectangle), [Microsoft.Office.Interop.Visio.Shape.DrawOval](/office/vba/api/Visio.Shape.DrawOval), [ Microsoft.Office.Interop.Visio.Shape.Copy](/office/vba/api/Visio.Shape.Copy), ve [Microsoft.Office.Interop.Visio.Shape.Paste](/office/vba/api/Visio.Shape.Paste) yöntemleri ve [ Microsoft.Office.Interop.Visio.VisCutCopyPasteCodes.visCopyPasteNoTranslate](/office/vba/api/Visio.viscutcopypastecodes) bayrağı.  
  
 Yapıştırılan bilgi biçimini denetlemek ve (isteğe bağlı olarak) bir kaynak dosyaya (örneğin, bir Microsoft Office Word belgesi) bir bağlantı kurmak gerekiyorsa denetlemeye yöntemini kullanın.  
  
### <a name="to-copy-shapes-and-shape-locations-to-another-page"></a>Şekiller ve Şekil konumları başka bir sayfaya kopyalamak için  
  
-   Aşağıdaki örnek, şekilleri ilk sayfadan kopyalayın ve ikinci sayfa koordinat özgün konumlarına ile yapıştırın gösterilmektedir.  
  
     [!code-csharp[Trin_VstcoreVisioAutomationAddIn#15](../vsto/codesnippet/CSharp/trin_vstcorevisioautomationaddin/ThisAddIn.cs#15)]
     [!code-vb[Trin_VstcoreVisioAutomationAddIn#15](../vsto/codesnippet/VisualBasic/trin_vstcorevisioautomationaddin/ThisAddIn.vb#15)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visio çözümleri](../vsto/visio-solutions.md)   
 [Visio nesne modeline genel bakış](../vsto/visio-object-model-overview.md)   
 [Visio şekilleri ile çalışma](../vsto/working-with-visio-shapes.md)   
 [Nasıl yapılır: Visio belgesine program aracılığıyla şekiller ekleme](../vsto/how-to-programmatically-add-shapes-to-a-visio-document.md)  
