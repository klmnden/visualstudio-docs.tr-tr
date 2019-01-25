---
title: 'Nasıl yapılır: Program aracılığıyla karakter sayma sayısı'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- characters, counting in documents
- counting characters in documents
- documents [Office development in Visual Studio], counting characters
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 57babe4379482c4718990bac936c8bc7f930e112
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54872631"
---
# <a name="how-to-programmatically-count-characters-in-documents"></a>Nasıl yapılır: Program aracılığıyla karakter sayma sayısı
  İlk karakter bir belge, ekleme noktasını temsil eden karakter 0. konumdadır. Son karakter konumundan belgede toplam karakter sayısı eşittir. Kullanarak bir belgedeki karakter sayısına göre belirleyebilirsiniz <xref:Microsoft.Office.Interop.Word.Characters.Count%2A> özelliği <xref:Microsoft.Office.Interop.Word.Characters> koleksiyonu.  
  
 Boşluk, paragraf işaretlerini ve normalde gizli diğer karakterler dahil olmak üzere belgedeki tüm karakterleri sayılır. Paragraf işaretlerini içerdiği için yeni, boş bir belge bile bir karakter sayısını döndürür.  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
## <a name="to-display-the-number-of-characters-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesinde karakter sayısını görüntülemek için  
  
1.  Belgenin tamamını seçin.  
  
     [!code-vb[Trin_VstcoreWordAutomation#98](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#98)]
     [!code-csharp[Trin_VstcoreWordAutomation#98](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#98)]  
  
2.  Bir ileti kutusunda belgedeki karakter sayısına göre görüntüler.  
  
     [!code-vb[Trin_VstcoreWordAutomation#99](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#99)]
     [!code-csharp[Trin_VstcoreWordAutomation#99](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#99)]  
  
## <a name="to-display-the-number-of-characters-in-a-vsto-add-in"></a>Bir VSTO eklenti karakter sayısını görüntülemek için  
  
1.  Belgenin tamamını seçin. Aşağıdaki örnek, etkin belgeyi seçer.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#98](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#98)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#98](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#98)]  
  
2.  Bir ileti kutusunda belgedeki karakter sayısına göre görüntüler.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#99](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#99)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#99](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#99)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Program aracılığıyla aralıkta başlangıç ve bitiş karakterlerini alma](../vsto/how-to-programmatically-retrieve-start-and-end-characters-in-ranges.md)   
 [Nasıl yapılır: Program aracılığıyla tanımlama ve belgelerde aralıkları seçin](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)  
