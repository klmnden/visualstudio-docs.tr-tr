---
title: 'Nasıl Yapılır: Belgelerde metni program aracılığıyla açıklama ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- comments, adding to documents
- documents [Office development in Visual Studio], adding comments
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 677f0ba2cf02f4dd62759ea5f125c91290dc0762
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53857033"
---
# <a name="how-to-programmatically-add-comments-to-text-in-documents"></a>Nasıl Yapılır: Belgelerde metni program aracılığıyla açıklama ekleme
  Belge sınıfının açıklamalar özelliği bir Microsoft Office Word belgesindeki bir metin aralığı için bir açıklama ekler.  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
 Aşağıdaki örnek, ilk paragrafa belgedeki bir açıklama ekler.  
  
## <a name="to-add-a-new-comment-to-text-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesinde metin için yeni bir açıklama eklemek için  
  
1.  Çağrı <xref:Microsoft.Office.Interop.Word.Comments.Add%2A> yöntemi <xref:Microsoft.Office.Tools.Word.Document.Comments%2A> özelliği ve aralığı ve açıklama metni girin. Aşağıdaki kod örneği kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomation#118](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#118)]
     [!code-csharp[Trin_VstcoreWordAutomation#118](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#118)]  
  
## <a name="to-add-a-new-comment-to-text-in-a-vsto-add-in"></a>Bir VSTO eklentisi metinde yeni bir açıklama eklemek için  
  
1.  Çağrı <xref:Microsoft.Office.Interop.Word.Comments.Add%2A> yöntemi <xref:Microsoft.Office.Interop.Word._Document.Comments%2A> özelliği ve aralığı ve açıklama metni girin.  
  
     Aşağıdaki kod örneği, etkin belgeye bir yorum ekler. Bu örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#118](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#118)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#118](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#118)]  
  
## <a name="robust-programming"></a>Güçlü programlama  
 Word yorum ekleyen kullanıcının baş değiştirmek için kullanın <xref:Microsoft.Office.Interop.Word._Application.UserInitials%2A> özelliği.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Belgelerden tüm açıklamaları program aracılığıyla kaldırma](../vsto/how-to-programmatically-remove-all-comments-from-documents.md)   
 [Belge konak öğesi](../vsto/document-host-item.md)  
