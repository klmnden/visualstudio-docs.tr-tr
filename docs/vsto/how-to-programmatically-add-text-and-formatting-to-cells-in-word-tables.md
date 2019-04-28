---
title: 'Nasıl yapılır: Metin ve biçimlendirme Word tablolarında hücrelere program aracılığıyla ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- cells, adding text and formatting
- text [Office development in Visual Studio], adding to Word tables
- formatting [Office development in Visual Studio]
- tables [Office development in Visual Studio], adding text and formatting
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a415e55c263534ee4b29e5b45e24ad471d68fe0e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62817482"
---
# <a name="how-to-programmatically-add-text-and-formatting-to-cells-in-word-tables"></a>Nasıl yapılır: Metin ve biçimlendirme Word tablolarında hücrelere program aracılığıyla ekleme
  Her tablo hücrelerinin koleksiyonu oluşur. Her <xref:Microsoft.Office.Interop.Word.Cell> nesne tablodaki bir hücreyi temsil eder. Konumuyla tablodaki her bir hücre bakın. Bu örnekte, ilk satırın ve tablonun ilk sütunu bulunan hücrenin başvurduğu; metin hücreye ekler; ve biçimlendirme uygular.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="to-add-text-and-formatting-to-cells"></a>Metin ve biçimlendirme hücrelere eklemek için

1. Konumuyla tablodaki hücre bakın, metin hücresine ekleyin ve biçimlendirme uygulayın.

     Aşağıdaki kod örneği belge düzeyi özelleştirmesinde kullanılabilir. Bu örneği kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomation#97](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#97)]
     [!code-csharp[Trin_VstcoreWordAutomation#97](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#97)]

     Aşağıdaki kod örneği, VSTO eklentisi içinde kullanılabilir. Bu örnek etkin belgeyi kullanır. Örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#97](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#97)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#97](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#97)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Program aracılığıyla Word tabloları oluşturma](../vsto/how-to-programmatically-create-word-tables.md)
- [Nasıl yapılır: Word tablolarına program aracılığıyla satır ve sütun ekleme](../vsto/how-to-programmatically-add-rows-and-columns-to-word-tables.md)
- [Nasıl yapılır: Belge özellikleriyle Word tablolarını program aracılığıyla doldurma](../vsto/how-to-programmatically-populate-word-tables-with-document-properties.md)
