---
title: 'Nasıl yapılır: Belgelerde metni program aracılığıyla açıklama ekleme'
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
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5aba4c6446b2dbcfcb31c423a28eedd552799b4e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62967676"
---
# <a name="how-to-programmatically-add-comments-to-text-in-documents"></a>Nasıl yapılır: Belgelerde metni program aracılığıyla açıklama ekleme
  Belge sınıfının açıklamalar özelliği bir Microsoft Office Word belgesindeki bir metin aralığı için bir açıklama ekler.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

 Aşağıdaki örnek, ilk paragrafa belgedeki bir açıklama ekler.

## <a name="to-add-a-new-comment-to-text-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesinde metin için yeni bir açıklama eklemek için

1. Çağrı <xref:Microsoft.Office.Interop.Word.Comments.Add%2A> yöntemi <xref:Microsoft.Office.Tools.Word.Document.Comments%2A> özelliği ve aralığı ve açıklama metni girin. Aşağıdaki kod örneği kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomation#118](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#118)]
     [!code-csharp[Trin_VstcoreWordAutomation#118](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#118)]

## <a name="to-add-a-new-comment-to-text-in-a-vsto-add-in"></a>Bir VSTO eklentisi metinde yeni bir açıklama eklemek için

1. Çağrı <xref:Microsoft.Office.Interop.Word.Comments.Add%2A> yöntemi <xref:Microsoft.Office.Interop.Word._Document.Comments%2A> özelliği ve aralığı ve açıklama metni girin.

     Aşağıdaki kod örneği, etkin belgeye bir yorum ekler. Bu örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#118](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#118)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#118](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#118)]

## <a name="robust-programming"></a>Güçlü programlama
 Word yorum ekleyen kullanıcının baş değiştirmek için kullanın <xref:Microsoft.Office.Interop.Word._Application.UserInitials%2A> özelliği.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Belgelerden tüm açıklamaları program aracılığıyla kaldırma](../vsto/how-to-programmatically-remove-all-comments-from-documents.md)
- [Belge konak öğesi](../vsto/document-host-item.md)
