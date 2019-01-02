---
title: 'Nasıl Yapılır: Visio belgelerini program aracılığıyla kapatma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], closing Visio documents
- Visio [Office development in Visual Studio], closing Visio documents
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 0516fcaf8f35e089752e645fbe22093ed8d87bf3
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53848541"
---
# <a name="how-to-programmatically-close-visio-documents"></a>Nasıl Yapılır: Visio belgelerini program aracılığıyla kapatma
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
