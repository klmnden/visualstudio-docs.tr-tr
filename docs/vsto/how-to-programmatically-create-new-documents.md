---
title: 'Nasıl yapılır: Program aracılığıyla yeni belgeler oluşturma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- templates [Office development in Visual Studio], custom document
- Word [Office development in Visual Studio], creating documents
- documents [Office development in Visual Studio], creating
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 94f39c80fc2b9294afb172c58fa62ef17f06516d
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54874659"
---
# <a name="how-to-programmatically-create-new-documents"></a>Nasıl yapılır: Program aracılığıyla yeni belgeler oluşturma
  Bir belge programlı olarak oluşturduğunuzda, yerel bir yeni belge olduğu <xref:Microsoft.Office.Interop.Word.Document> nesne. Bu nesne ek olaylar ve veri bağlama yeteneklerine sahip değil bir <xref:Microsoft.Office.Tools.Word.Document> konak öğesi. Daha fazla bilgi için [konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md).  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
 Belge düzeyi projesi geliştirdiğinizde, program aracılığıyla ekleyemezsiniz <xref:Microsoft.Office.Tools.Word.Document> barındırmak, proje öğeleri. Bir VSTO eklenti projesinde herhangi dönüştürebilir <xref:Microsoft.Office.Interop.Word.Document> nesnesini bir <xref:Microsoft.Office.Tools.Word.Document> çalışma zamanında konak öğesi. Daha fazla bilgi için [genişletmek Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında VSTO Add-Ins](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).  
  
## <a name="to-create-a-new-document-based-on-the-normal-template"></a>Normal bir şablonu temel alan yeni bir belge oluşturmak için  
  
-   Kullanım <xref:Microsoft.Office.Interop.Word.Documents.Add%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Documents> koleksiyonu yeni bir belge oluşturmak için Normal şablonu temel alan. Bu kod örneği kullanmak için çalıştırın `ThisDocument` veya `ThisAddIn` projenizdeki sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomation#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#1)]
     [!code-csharp[Trin_VstcoreWordAutomation#1](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#1)]  
  
## <a name="use-custom-templates"></a>Özel şablonları kullanma  
 <xref:Microsoft.Office.Interop.Word.Documents.Add%2A> Yöntemi olan isteğe bağlı *şablon* Normal şablonu dışındaki bir şablonu temelinde yeni bir belge oluşturmak için bağımsız değişken. Şablonun tam yolunu ve dosya adını sağlamanız gerekir.  
  
### <a name="to-create-a-new-document-based-on-a-custom-template"></a>Özel bir şablonu temel alan yeni bir belge oluşturmak için  
  
-   Çağrı <xref:Microsoft.Office.Interop.Word.Documents.Add%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Documents> koleksiyonu ve şablonun yolunu belirtin. Bu kod örneği kullanmak için çalıştırın `ThisDocument` veya `ThisAddIn` projenizdeki sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomation#2](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#2)]
     [!code-csharp[Trin_VstcoreWordAutomation#2](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#2)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Varolan belgeleri program aracılığıyla açma](../vsto/how-to-programmatically-open-existing-documents.md)   
 [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)   
 [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)  
