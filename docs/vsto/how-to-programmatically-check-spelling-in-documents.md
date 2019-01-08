---
title: 'Nasıl yapılır: Program aracılığıyla Yazımı denetleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], checking spelling
- spelling checker, documents
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 19dc596851ba8ca8b2ea3ef50e7d151220354e3b
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54087769"
---
# <a name="how-to-programmatically-check-spelling-in-documents"></a>Nasıl yapılır: Program aracılığıyla Yazımı denetleme
  Belgede yazım denetimi yapmak için kullanın <xref:Microsoft.Office.Interop.Word._Application.CheckSpelling%2A> yöntemi. Bu yöntem, sağlanan parametresi doğru yazıldığından emin olup olmadığını gösteren bir Boole değeri döndürür.  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
## <a name="to-check-spelling-and-display-results-in-a-message-box"></a>Yazım denetimi ve sonuçları bir ileti kutusu içinde görüntülemek için  
  
1.  Çağrı <xref:Microsoft.Office.Interop.Word._Application.CheckSpelling%2A> yöntemi ve yazım hataları denetlemek için metin aralığı geçirin. Bu kod örneği kullanmak için çalıştırın `ThisDocument` veya `ThisAddIn` projenizdeki sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomation#113](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#113)]
     [!code-csharp[Trin_VstcoreWordAutomation#113](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#113)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Program aracılığıyla tanımlama ve belgelerde aralıkları seçin](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)  
