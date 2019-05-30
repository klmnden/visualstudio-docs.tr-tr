---
title: '& Program aracılığıyla Word Tablo hücrelerini biçimlendirme metin Ekle'
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
ms.openlocfilehash: cdab1877cf2114f7828dbd65786cf8758d77d0f3
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66402012"
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
