---
title: 'Nasıl yapılır: Visio belgelerini program aracılığıyla kapatma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], closing Visio documents
- Visio [Office development in Visual Studio], closing Visio documents
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 499cc399c1e23c6f045426e57f8e9a027b5c6537
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54091799"
---
# <a name="how-to-programmatically-close-visio-documents"></a>Nasıl yapılır: Visio belgelerini program aracılığıyla kapatma
  Etkin Microsoft Office Visio belgesini kullanarak kapatabilirsiniz `Microsoft.Office.Interop.Visio.Document.Close` yöntemi.  
  
 Bu yöntem hakkında daha fazla ayrıntı için VBA başvuru belgelerine bakın [Microsoft.Office.Interop.Visio.Document.Close](/office/vba/api/Visio.Document.Close) yöntemi.  
  
## <a name="close-the-active-document"></a>Etkin belgeyi Kapat  
  
### <a name="to-close-the-active-document"></a>Etkin belgeyi kapatmak için  
  
-   Çağrı `Microsoft.Office.Interop.Visio.Document.Close` etkin belgeyi Kapat için yöntemi.  
  
     Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `ThisAddIn` Visio için VSTO eklenti projesinde sınıfı.  
  
     [!code-csharp[Trin_VstcoreVisioAutomationAddIn#7](../vsto/codesnippet/CSharp/trin_vstcorevisioautomationaddin/ThisAddIn.cs#7)]
     [!code-vb[Trin_VstcoreVisioAutomationAddIn#7](../vsto/codesnippet/VisualBasic/trin_vstcorevisioautomationaddin/ThisAddIn.vb#7)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visio çözümleri](../vsto/visio-solutions.md)   
 [Visio nesne modeline genel bakış](../vsto/visio-object-model-overview.md)   
 [Nasıl yapılır: Program aracılığıyla yeni Visio belgeleri oluşturma](../vsto/how-to-programmatically-create-new-visio-documents.md)   
 [Nasıl yapılır: Program aracılığıyla Visio belgelerini açma](../vsto/how-to-programmatically-open-visio-documents.md)   
 [Nasıl yapılır: Program aracılığıyla Visio belgelerini kaydetme](../vsto/how-to-programmatically-save-visio-documents.md)   
 [Nasıl yapılır: Program aracılığıyla Visio belgelerini yazdırma](../vsto/how-to-programmatically-print-visio-documents.md)  
