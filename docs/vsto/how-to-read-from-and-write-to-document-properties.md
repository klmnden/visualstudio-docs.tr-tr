---
title: 'Nasıl yapılır: Okuma ve yazma için belge özellikleri'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Word [Office development in Visual Studio], document properties
- documents [Office development in Visual Studio], properties
- document properties [Office development in Visual Studio]
- Excel [Office development in Visual Studio], document properties
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 51add739e6303a62eb3333c4a173fa0d2e58f2f1
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54862635"
---
# <a name="how-to-read-from-and-write-to-document-properties"></a>Nasıl yapılır: Okuma ve yazma için belge özellikleri
  Bir belge yanı sıra belge özellikleri depolayabilirsiniz. Office uygulamaları birkaç yazar, başlık ve konu gibi yerleşik özellikler sağlar. Bu konu, Microsoft Office Excel ve Microsoft Office Word belgesi özelliklerini ayarlamak gösterilmektedir.  
  
 ![video bağlantı](../vsto/media/playvideo.gif "video bağlantı") ilgili video gösterimi için bkz. [nasıl yaparım? Erişim ve Microsoft Word özel belge özelliklerini değiştirmek mi? ](http://go.microsoft.com/fwlink/?LinkId=136772).  
  
 [!INCLUDE[appliesto_docprops](../vsto/includes/appliesto-docprops-md.md)]  
  
## <a name="set-document-properties-in-excel"></a>Excel belge özelliklerini ayarlama  
 Yerleşik özellikler Excel'de çalışmak için aşağıdaki özellikleri kullanın:  
  
- Bir belge düzeyi projede kullanmak <xref:Microsoft.Office.Tools.Excel.Workbook.BuiltinDocumentProperties%2A> özelliği `ThisWorkbook` sınıfı.  
  
- Bir VSTO eklenti projesinde kullanmak <xref:Microsoft.Office.Interop.Excel._Workbook.BuiltinDocumentProperties%2A> özelliği bir <xref:Microsoft.Office.Interop.Excel.Workbook> nesne.  
  
  Bu özellikleri döndürür bir <xref:Microsoft.Office.Core.DocumentProperties> bir koleksiyon nesne, <xref:Microsoft.Office.Core.DocumentProperty> nesneleri. Kullanabileceğiniz `Item` adı veya dizin koleksiyonundaki belirli bir özelliği almak için koleksiyonun özelliği.  
  
  Aşağıdaki kod örneği, yerleşik değiştirileceği gösterilmektedir **düzeltme numarası** bir belge düzeyi projede özelliği.  
  
### <a name="to-change-the-revision-number-property-in-excel"></a>Özelliğindeki düzeltme numarasını değiştirmek için  
  
1.  Yerleşik belge özellikleri, bir değişkene atayın.  
  
     [!code-vb[Trin_VstcoreProgramming#7](../vsto/codesnippet/VisualBasic/Trin_VstcoreProgrammingExcelVB/ThisWorkbook.vb#7)]
     [!code-csharp[Trin_VstcoreProgramming#7](../vsto/codesnippet/CSharp/Trin_VstcoreProgrammingExcelCS/ThisWorkbook.cs#7)]  
  
2.  Artırma `Revision Number` bir özellik.  
  
     [!code-vb[Trin_VstcoreProgramming#8](../vsto/codesnippet/VisualBasic/Trin_VstcoreProgrammingExcelVB/ThisWorkbook.vb#8)]
     [!code-csharp[Trin_VstcoreProgramming#8](../vsto/codesnippet/CSharp/Trin_VstcoreProgrammingExcelCS/ThisWorkbook.cs#8)]  
  
## <a name="set-document-properties-in-word"></a>Word'de belge özelliklerini ayarlama  
 Word yerleşik özellikleri ile çalışmak için aşağıdaki özellikleri kullanın:  
  
- Bir belge düzeyi projede kullanmak <xref:Microsoft.Office.Tools.Word.Document.BuiltInDocumentProperties%2A> özelliği `ThisDocument` sınıfı.  
  
- Bir VSTO eklenti projesinde kullanmak <xref:Microsoft.Office.Interop.Word._Document.BuiltInDocumentProperties%2A> özelliği bir <xref:Microsoft.Office.Interop.Word.Document> nesne.  
  
  Bu özellikleri döndürür bir <xref:Microsoft.Office.Core.DocumentProperties> bir koleksiyon nesne, <xref:Microsoft.Office.Core.DocumentProperty> nesneleri. Kullanabileceğiniz `Item` adı veya dizin koleksiyonundaki belirli bir özelliği almak için koleksiyonun özelliği.  
  
  Aşağıdaki kod örneği, yerleşik değiştirileceği gösterilmektedir **konu** bir belge düzeyi projede özelliği.  
  
### <a name="to-change-the-subject-property"></a>Konu özelliğini değiştirmek için  
  
1.  Yerleşik belge özellikleri, bir değişkene atayın.  
  
     [!code-csharp[Trin_VstcoreProgrammingWord#1](../vsto/codesnippet/CSharp/Trin_VstcoreProgrammingWordCS/ThisDocument.cs#1)]
     [!code-vb[Trin_VstcoreProgrammingWord#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreProgrammingWordVB/ThisDocument.vb#1)]  
  
2.  Değişiklik `Subject` "Teknik" özelliği.  
  
     [!code-csharp[Trin_VstcoreProgrammingWord#2](../vsto/codesnippet/CSharp/Trin_VstcoreProgrammingWordCS/ThisDocument.cs#2)]
     [!code-vb[Trin_VstcoreProgrammingWord#2](../vsto/codesnippet/VisualBasic/Trin_VstcoreProgrammingWordVB/ThisDocument.vb#2)]  
  
## <a name="robust-programming"></a>Güçlü programlama  
 Örnekler kod yazmış olduğunuz varsayılır `ThisWorkbook` Excel için belge düzeyi projesinde sınıfı ve `ThisDocument` Word için belge düzeyi projesinde sınıfı.  
  
 Microsoft Office, Word ve Excel ve nesneleri ile çalışmanıza rağmen kullanılabilir yerleşik belge özelliklerinin listesini sağlar. Tanımlanmamış bir özelliğe erişmeye çalışırken bir özel durum oluşturur.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSTO eklentilerini programlama](../vsto/programming-vsto-add-ins.md)   
 [Belge düzeyi özelleştirmelerini programlama](../vsto/programming-document-level-customizations.md)   
 [Nasıl yapılır: Özel belge özelliklerini oluşturma ve değiştirme](../vsto/how-to-create-and-modify-custom-document-properties.md)  
