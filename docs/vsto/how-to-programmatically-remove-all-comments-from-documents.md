---
title: 'Nasıl Yapılır: Belgelerden tüm açıklamaları program aracılığıyla kaldırma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], removing comments
- comments, removing from documents
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 368779aa5c0edbfcaba3aff2abdf3eba09375f9f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53833416"
---
# <a name="how-to-programmatically-remove-all-comments-from-documents"></a>Nasıl Yapılır: Belgelerden tüm açıklamaları program aracılığıyla kaldırma
  Kullanım `DeleteAllComments` tüm açıklamaları bir Microsoft Office Word belgesinden kaldırmak için yöntemi.  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
## <a name="to-remove-all-comments-from-a-document-that-is-part-of-a-document-level-customization"></a>Tüm açıklamaları belge düzeyinde özelleştirme parçası olan bir belgeyi kaldırmak için  
  
1.  Çağrı <xref:Microsoft.Office.Tools.Word.Document.DeleteAllComments%2A> yöntemi `ThisDocument` projenizdeki sınıfı. Bu kod örneği kullanmak için çalıştırın `ThisDocument` sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomation#119](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#119)]
     [!code-csharp[Trin_VstcoreWordAutomation#119](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#119)]  
  
## <a name="to-remove-all-comments-from-a-document-by-using-a-vsto-add-in"></a>Tüm açıklamaları bir belgeden bir VSTO eklentisi kullanarak kaldırmak için  
  
1.  Çağrı <xref:Microsoft.Office.Interop.Word._Document.DeleteAllComments%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Document> açıklamaları kaldırmak istediğiniz.  
  
     Aşağıdaki kod örneği, tüm yorumlar etkin belgeden kaldırır. Bu kod örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#119](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#119)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#119](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#119)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Belgelerde metni program aracılığıyla açıklama ekleme](../vsto/how-to-programmatically-add-comments-to-text-in-documents.md)   
 [Belge konak öğesi](../vsto/document-host-item.md)  
