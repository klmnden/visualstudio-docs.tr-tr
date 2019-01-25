---
title: 'Nasıl yapılır: Program aracılığıyla Word tabloları oluşturma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], adding tables
- tables [Office development in Visual Studio], adding to documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 1e0b75230ccce5004d1f764db7c7ea39775f3a4f
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54869937"
---
# <a name="how-to-programmatically-create-word-tables"></a>Nasıl yapılır: Program aracılığıyla Word tabloları oluşturma
  <xref:Microsoft.Office.Interop.Word.Tables> Koleksiyon üyesi olduğu <xref:Microsoft.Office.Interop.Word.Document>, <xref:Microsoft.Office.Tools.Word.Document>, <xref:Microsoft.Office.Interop.Word.Selection>, ve <xref:Microsoft.Office.Interop.Word.Range> sınıflarıyla bu içeriklerden herhangi birinde bir tablo oluşturabileceğiniz anlamına gelir. Kullandığınız <xref:Microsoft.Office.Interop.Word.Tables.Add%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Tables> belirli bir aralıkta bir tablo eklemek için koleksiyonu.  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
## <a name="create-tables-in-document-level-customizations"></a>Belge düzeyi özelleştirmelerde tabloları oluşturma  
  
### <a name="to-add-a-table-to-a-document"></a>Bir belge için bir tablo eklemek için  
  
- Kullanım <xref:Microsoft.Office.Interop.Word.Tables.Add%2A> üç satır ve belgenin başına dört sütun içeren bir tablo eklemek için yöntemi.  
  
   Aşağıdaki kod örneği kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.  
  
   [!code-vb[Trin_VstcoreWordAutomation#86](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#86)]
   [!code-csharp[Trin_VstcoreWordAutomation#86](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#86)]  
  
  Bir tablo oluşturduğunuzda, otomatik olarak eklenir <xref:Microsoft.Office.Interop.Word.Tables> koleksiyonunu <xref:Microsoft.Office.Tools.Word.Document> konak öğesi. Ardından tabloda öğe numarası kullanarak başvurabilirsiniz <xref:Microsoft.Office.Interop.Word.Tables.Item%2A> özelliği, aşağıdaki kodda gösterildiği gibi.  
  
### <a name="to-refer-to-a-table-by-item-number"></a>Öğe numarasına göre bir tabloya başvurmak için  
  
1. Kullanım <xref:Microsoft.Office.Interop.Word.Tables.Item%2A> özelliği ve tedarik başvurmak istediğiniz tabloyu öğe sayısı.  
  
    Aşağıdaki kod örneği kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.  
  
    [!code-vb[Trin_VstcoreWordAutomation#87](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#87)]
    [!code-csharp[Trin_VstcoreWordAutomation#87](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#87)]  
  
   Her <xref:Microsoft.Office.Interop.Word.Table> nesne de sahip bir <xref:Microsoft.Office.Interop.Word.Table.Range%2A> biçimlendirme ayarlamanıza olanak sağlayan özellik öznitelikleri.  
  
### <a name="to-apply-a-style-to-a-table"></a>Bir tabloya bir stil uygulamak için  
  
1.  Kullanım <xref:Microsoft.Office.Interop.Word.Table.Style%2A> tabloya Word yerleşik stil uygulamak için özellik.  
  
     Aşağıdaki kod örneği kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomation#88](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#88)]
     [!code-csharp[Trin_VstcoreWordAutomation#88](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#88)]  
  
## <a name="create-tables-in-vsto-add-ins"></a>VSTO eklentileri tablo oluşturma  
  
### <a name="to-add-a-table-to-a-document"></a>Bir belge için bir tablo eklemek için  
  
- Kullanım <xref:Microsoft.Office.Interop.Word.Tables.Add%2A> üç satır ve belgenin başına dört sütun içeren bir tablo eklemek için yöntemi.  
  
   Aşağıdaki kod örneği, etkin belgeye bir tablo ekler. Bu örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.  
  
   [!code-vb[Trin_VstcoreWordAutomationAddIn#86](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#86)]
   [!code-csharp[Trin_VstcoreWordAutomationAddIn#86](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#86)]  
  
  Bir tablo oluşturduğunuzda, otomatik olarak eklenir <xref:Microsoft.Office.Interop.Word.Tables> koleksiyonunu <xref:Microsoft.Office.Interop.Word.Document>. Ardından tabloda öğe numarası kullanarak başvurabilirsiniz <xref:Microsoft.Office.Interop.Word.Tables.Item%2A> özelliği, aşağıdaki kodda gösterildiği gibi.  
  
### <a name="to-refer-to-a-table-by-item-number"></a>Öğe numarasına göre bir tabloya başvurmak için  
  
1. Kullanım <xref:Microsoft.Office.Interop.Word.Tables.Item%2A> özelliği ve tedarik başvurmak istediğiniz tabloyu öğe sayısı.  
  
    Aşağıdaki kod örneği, etkin belgeyi kullanır. Bu örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.  
  
    [!code-vb[Trin_VstcoreWordAutomationAddIn#87](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#87)]
    [!code-csharp[Trin_VstcoreWordAutomationAddIn#87](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#87)]  
  
   Her <xref:Microsoft.Office.Interop.Word.Table> nesne de sahip bir <xref:Microsoft.Office.Interop.Word.Table.Range%2A> biçimlendirme ayarlamanıza olanak sağlayan özellik öznitelikleri.  
  
### <a name="to-apply-a-style-to-a-table"></a>Bir tabloya bir stil uygulamak için  
  
1.  Kullanım <xref:Microsoft.Office.Interop.Word.Table.Style%2A> tabloya Word yerleşik stil uygulamak için özellik.  
  
     Aşağıdaki kod örneği, etkin belgeyi kullanır. Bu örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#88](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#88)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#88](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#88)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Metin ve biçimlendirme Word tablolarında hücrelere program aracılığıyla ekleme](../vsto/how-to-programmatically-add-text-and-formatting-to-cells-in-word-tables.md)   
 [Nasıl yapılır: Word tablolarına program aracılığıyla satır ve sütun ekleme](../vsto/how-to-programmatically-add-rows-and-columns-to-word-tables.md)   
 [Nasıl yapılır: Belge özellikleriyle Word tablolarını program aracılığıyla doldurma](../vsto/how-to-programmatically-populate-word-tables-with-document-properties.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)  
