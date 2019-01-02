---
title: 'Nasıl Yapılır: Baskı önizlemede program aracılığıyla belgeleri görüntüleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Word [Office development in Visual Studio], displaying documents in print preview
- documents [Office development in Visual Studio], displaying in print preview
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 66a21f2def806dc7800caa01d26a989f9a4cf8e8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53891952"
---
# <a name="how-to-programmatically-display-documents-in-print-preview"></a>Nasıl Yapılır: Baskı önizlemede program aracılığıyla belgeleri görüntüleme
  Çözümünüze bir rapor oluşturur, kullanıcı yazdırma önizleme modunda raporu görüntülemek isteyebilirsiniz.  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
## <a name="procedures-for-document-level-customizations"></a>Belge düzeyi özelleştirmeleri için yordamlar  
  
### <a name="to-display-a-document-in-print-preview-by-calling-the-printpreview-method"></a>PrintPreview yöntemini çağırarak baskı önizlemede belgeyi görüntülemek için  
  
1.  Çağrı <xref:Microsoft.Office.Tools.Word.Document.PrintPreview%2A> yöntemi <xref:Microsoft.Office.Tools.Word.Document> sınıfı. Bu kod örneği kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomation#13](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#13)]
     [!code-csharp[Trin_VstcoreWordAutomation#13](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#13)]  
  
### <a name="to-display-a-document-in-print-preview-by-setting-the-printpreview-property"></a>PrintPreview özelliğini ayarlayarak baskı önizlemede belgeyi görüntülemek için  
  
1.  Ayarlama <xref:Microsoft.Office.Interop.Word._Application.PrintPreview%2A> özelliği <xref:Microsoft.Office.Interop.Word.Application> nesnesini **true**.  
  
     [!code-vb[Trin_VstcoreWordAutomation#14](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#14)]
     [!code-csharp[Trin_VstcoreWordAutomation#14](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#14)]  
  
## <a name="procedures-for-vsto-add-ins"></a>VSTO eklentileri için yordamlar  
  
### <a name="to-display-a-document-in-print-preview-by-calling-the-printpreview-method"></a>PrintPreview yöntemini çağırarak baskı önizlemede belgeyi görüntülemek için  
  
1.  Çağrı <xref:Microsoft.Office.Interop.Word._Document.PrintPreview%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Document> Önizleme istediğiniz. Bu kod örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#13](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#13)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#13](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#13)]  
  
### <a name="to-display-a-document-in-print-preview-by-setting-the-printpreview-property"></a>PrintPreview özelliğini ayarlayarak baskı önizlemede belgeyi görüntülemek için  
  
1.  Ayarlama <xref:Microsoft.Office.Interop.Word._Application.PrintPreview%2A> özelliği <xref:Microsoft.Office.Interop.Word.Application> nesnesini **true**.  
  
     [!code-vb[Trin_VstcoreWordAutomation#14](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#14)]
     [!code-csharp[Trin_VstcoreWordAutomation#14](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#14)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Program aracılığıyla belgeleri yazdırma](../vsto/how-to-programmatically-print-documents.md)   
 [Nasıl yapılır: Varolan belgeleri program aracılığıyla açma](../vsto/how-to-programmatically-open-existing-documents.md)   
 [Nasıl yapılır: Program aracılığıyla yeni belgeler oluşturma](../vsto/how-to-programmatically-create-new-documents.md)  
