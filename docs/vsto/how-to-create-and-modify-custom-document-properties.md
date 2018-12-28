---
title: 'Nasıl Yapılır: Özel belge özelliklerini oluşturma ve değiştirme'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- custom document properties
- documents [Office development in Visual Studio], properties
- document properties [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 71ff5c37eee21092e186e50547cf9c0b72f1b20e
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53646515"
---
# <a name="how-to-create-and-modify-custom-document-properties"></a>Nasıl Yapılır: Özel belge özelliklerini oluşturma ve değiştirme
  Yukarıda listelenen Microsoft Office uygulamaları ile belgeleri depolanan yerleşik özellikler sağlar. Ayrıca, oluşturun ve belge ile depolamak istediğiniz ek bilgiler varsa, özel belge özelliklerini değiştirin.  
  
 [!INCLUDE[appliesto_docprops](../vsto/includes/appliesto-docprops-md.md)]  
  
 Özel özellikleri ile çalışmak için bir belge CustomDocumentProperties özelliğini kullanın. Örneğin, Microsoft Office Excel için belge düzeyi projede kullanın <xref:Microsoft.Office.Tools.Excel.Workbook.CustomDocumentProperties%2A> özelliği `ThisWorkbook` sınıfı. Bir VSTO eklenti projesinde Excel kullanmak <xref:Microsoft.Office.Interop.Excel._Workbook.CustomDocumentProperties%2A> özelliği bir <xref:Microsoft.Office.Interop.Excel.Workbook> nesne. Bu özellikleri döndürür bir <xref:Microsoft.Office.Core.DocumentProperties> bir koleksiyon nesne, <xref:Microsoft.Office.Core.DocumentProperty> nesneleri. Kullanabileceğiniz `Item` adı veya dizin koleksiyonundaki belirli bir özelliği almak için koleksiyonun özelliği.  
  
 Aşağıdaki örnek, bir özel özellik Excel için belge düzeyi özelleştirmesinde ekleyin ve bir değer atamak gösterilmiştir.  
  
 ![video bağlantı](../vsto/media/playvideo.gif "video bağlantı") ilgili video gösterimi için bkz. [nasıl yaparım? Erişim ve Microsoft Word özel belge özelliklerini değiştirmek mi? ](http://go.microsoft.com/fwlink/?LinkId=136772).  
  
## <a name="example"></a>Örnek  
 [!code-vb[Trin_VstcoreProgramming#6](../vsto/codesnippet/VisualBasic/Trin_VstcoreProgrammingExcelVB/ThisWorkbook.vb#6)]
 [!code-csharp[Trin_VstcoreProgramming#6](../vsto/codesnippet/CSharp/Trin_VstcoreProgrammingExcelCS/ThisWorkbook.cs#6)]  
  
## <a name="robust-programming"></a>Güçlü programlama  
 Erişmeye `Value` özelliği tanımsız özellikleri için bir özel durum oluşturur.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSTO eklentilerini programlama](../vsto/programming-vsto-add-ins.md)   
 [Belge düzeyi özelleştirmelerini programlama](../vsto/programming-document-level-customizations.md)   
 [Nasıl yapılır: Okuma ve yazma için belge özellikleri](../vsto/how-to-read-from-and-write-to-document-properties.md)  
  
  