---
title: 'Nasıl yapılır: Program aracılığıyla belgeleri yazdırma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Word [Office development in Visual Studio], printing documents
- documents [Office development in Visual Studio], printing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 252891f603f974b43fa9a609bd9bbde9dde2f7f3
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56654080"
---
# <a name="how-to-programmatically-print-documents"></a>Nasıl yapılır: Program aracılığıyla belgeleri yazdırma
  Tüm yazdırabilir Microsoft Office Word belgesi veya varsayılan yazıcı için bir belge bir parçası.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="print-a-document-that-is-part-of-a-document-level-customization"></a>Belge düzeyi özelleştirmesi parçası olan bir belgeyi yazdır

### <a name="to-print-the-entire-document"></a>Tüm belgeyi yazdırma

1.  Çağrı <xref:Microsoft.Office.Tools.Word.Document.PrintOut%2A> yöntemi `ThisDocument` , projenizdeki tüm belgeyi yazdırma sınıfı. Bu örneği kullanmak için kodu çalıştırın `ThisDocument` sınıfı.

     [!code-vb[Trin_VstcoreWordAutomation#11](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#11)]
     [!code-csharp[Trin_VstcoreWordAutomation#11](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#11)]

### <a name="to-print-the-current-page-of-the-document"></a>Geçerli belge sayfasını yazdırmak için

1.  Çağrı <xref:Microsoft.Office.Tools.Word.Document.PrintOut%2A> yöntemi `ThisDocument` projenizde sınıf ve geçerli sayfayı bir kopyasını yazdırılması gerektiğini belirtin. Bu örneği kullanmak için kodu çalıştırın `ThisDocument` sınıfı.

     [!code-vb[Trin_VstcoreWordAutomation#12](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#12)]
     [!code-csharp[Trin_VstcoreWordAutomation#12](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#12)]

## <a name="print-a-document-by-using-a-vsto-add-in"></a>Bir VSTO eklentisi kullanarak bir belgeyi yazdır

### <a name="to-print-an-entire-document"></a>Tüm belgeyi yazdırma

1.  Çağrı <xref:Microsoft.Office.Interop.Word._Document.PrintOut%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Document> yazdırmak istediğiniz nesne. Aşağıdaki kod örneği, etkin belgeyi yazdırır. Bu örneği kullanmak için kodu çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#11](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#11)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#11](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#11)]

### <a name="to-print-the-current-page-of-a-document"></a>Geçerli bir belge sayfasını yazdırmak için

1.  Çağrı <xref:Microsoft.Office.Interop.Word._Document.PrintOut%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Document> , yazdırma ve geçerli sayfasının bir kopya yazdırılır belirtmek istediğiniz nesne. Aşağıdaki kod örneği, etkin belgeyi yazdırır. Bu örneği kullanmak için kodu çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#12](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#12)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#12](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#12)]

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
