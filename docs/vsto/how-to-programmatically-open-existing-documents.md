---
title: 'Nasıl yapılır: Varolan belgeleri program aracılığıyla açma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], opening
- Word [Office development in Visual Studio], opening documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 490dda6e5357cd0933c6a8b494cc4373038e5c1c
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60062171"
---
# <a name="how-to-programmatically-open-existing-documents"></a>Nasıl yapılır: Varolan belgeleri program aracılığıyla açma
  <xref:Microsoft.Office.Interop.Word.Documents.Open%2A> Yöntemi, bir tam yol ve dosya adıyla belirtilen mevcut Microsoft Office Word belgesi açar. Bu yöntem döndürür bir <xref:Microsoft.Office.Interop.Word.Document> , açılan Belge temsil eder.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="to-open-a-document"></a>Bir belgeyi açmak için

- Çağrı <xref:Microsoft.Office.Interop.Word.Documents.Open%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Documents> koleksiyon ve belge yolunu belirtin.

     [!code-vb[Trin_VstcoreWordAutomation#5](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#5)]
     [!code-csharp[Trin_VstcoreWordAutomation#5](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#5)]

## <a name="to-open-a-document-as-read-only"></a>Bir belgeyi salt okunur olarak açmak için

- Çağrı <xref:Microsoft.Office.Interop.Word.Documents.Open%2A> yöntemi, belge için bir yol girin ve ayarlama *salt okunur* bağımsız değişkeni **True** yöntemini çağırın.

     [!code-vb[Trin_VstcoreWordAutomation#6](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#6)]
     [!code-csharp[Trin_VstcoreWordAutomation#6](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#6)]

## <a name="compile-the-code"></a>Kod derleme
 Bu kod örneği için aşağıdakiler gereklidir:

- Adlı bir belge *NewDocument.doc* adlı bir dizinde bulunmalıdır *Test* c sürücüsünün

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Program aracılığıyla yeni belgeler oluşturma](../vsto/how-to-programmatically-create-new-documents.md)
- [Nasıl yapılır: Program aracılığıyla belgeleri kapatma](../vsto/how-to-programmatically-close-documents.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
