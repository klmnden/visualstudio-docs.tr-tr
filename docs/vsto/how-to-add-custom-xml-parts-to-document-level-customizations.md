---
title: 'Nasıl yapılır: Belge düzeyi özelleştirmelerine özel XML bölümleri ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- document-level customizations [Office development in Visual Studio], custom XML parts
- Office documents [Office development in Visual Studio, custom XML parts
- Word [Office development in Visual Studio], custom XML parts
- Excel [Office development in Visual Studio], custom XML parts
- custom XML parts [Office development in Visual Studio], adding
- documents [Office development in Visual Studio], custom XML parts
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 4de0471dcc94a709156f5dc9fcce57dca8fb82bd
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63427599"
---
# <a name="how-to-add-custom-xml-parts-to-document-level-customizations"></a>Nasıl yapılır: Belge düzeyi özelleştirmelerine özel XML bölümleri ekleme
  Belge düzeyi özelleştirmesinde özel bir XML parçasına oluşturarak, bir Microsoft Office Excel çalışma kitabı veya Microsoft Office Word belgesi içinde XML verileri depolayabilirsiniz. Daha fazla bilgi için [özel XML bölümlerine genel bakış](../vsto/custom-xml-parts-overview.md).

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

> [!NOTE]
> Visual Studio, Microsoft Office PowerPoint için belge düzeyi projelere sağlamaz. Bir VSTO eklentisi kullanarak bir PowerPoint sunumu özel XML bölümleri ekleme hakkında daha fazla bilgi için bkz: [nasıl yapılır: VSTO eklentileri kullanarak belgelere özel XML bölümleri ekleme](../vsto/how-to-add-custom-xml-parts-to-documents-by-using-vsto-add-ins.md).

### <a name="to-add-a-custom-xml-part-to-an-excel-workbook"></a>Bir Excel çalışma kitabına özel XML bölümleri ekleme

1. Yeni bir <xref:Microsoft.Office.Core.CustomXMLPart> nesnesini <xref:Microsoft.Office.Core.CustomXMLParts> çalışma kitabında koleksiyonu. <xref:Microsoft.Office.Core.CustomXMLPart> Çalışma kitabında depolamak istediğiniz XML dizesi içerir.

     [!code-csharp[Trin_AddCustomXmlPartExcelDocLevel#1](../vsto/codesnippet/CSharp/Trin_AddCustomXmlPartExcelDocLevel/ThisWorkbook.cs#1)]
     [!code-vb[Trin_AddCustomXmlPartExcelDocLevel#1](../vsto/codesnippet/VisualBasic/Trin_AddCustomXmlPartExcelDocLevel/ThisWorkbook.vb#1)]

2. Ekleme `AddCustomXmlPartToWorkbook` yönteme `ThisWorkbook` Excel için belge düzeyi projesinde sınıfı.

3. Projenizdeki başka bir koddan yöntemi çağırın. Örneğin, kullanıcı çalışma kitabınızı açtığında özel XML parçaları oluşturmak için içinden yöntemi çağırın `ThisWorkbook_Startup` olay işleyicisi.

### <a name="to-add-a-custom-xml-part-to-a-word-document"></a>Bir Word belgesi için özel XML bölümleri ekleme

1. Yeni bir <xref:Microsoft.Office.Core.CustomXMLPart> nesnesini <xref:Microsoft.Office.Core.CustomXMLParts> belgedeki koleksiyonu. <xref:Microsoft.Office.Core.CustomXMLPart> Belge içinde depolamak istediğiniz XML dizesi içerir.

     [!code-vb[Trin_AddCustomXmlPartWordDocLevel#1](../vsto/codesnippet/VisualBasic/Trin_AddCustomXmlPartWordDocLevel/ThisDocument.vb#1)]
     [!code-csharp[Trin_AddCustomXmlPartWordDocLevel#1](../vsto/codesnippet/CSharp/Trin_AddCustomXmlPartWordDocLevel/ThisDocument.cs#1)]

2. Ekleme `AddCustomXmlPartToDocument` yönteme `ThisDocument` Word için belge düzeyi projesinde sınıfı.

3. Projenizdeki başka bir koddan yöntemi çağırın. Örneğin, kullanıcının belge açıldığında özel XML parçaları oluşturmak için içinden yöntemi çağırın `ThisDocument_Startup` olay işleyicisi.

## <a name="robust-programming"></a>Güçlü programlama
 Kolaylık olması için bu örnek, bir yerel değişken yöntemi olarak tanımlanan bir XML dizesi kullanır. Genellikle, bir dosya veya veritabanı gibi bir dış kaynaktan XML edinmeniz gerekir.

## <a name="see-also"></a>Ayrıca bkz.
- [Özel XML bölümlerine genel bakış](../vsto/custom-xml-parts-overview.md)
- [Nasıl yapılır: VSTO eklentileri kullanarak belgelere özel XML bölümleri ekleme](../vsto/how-to-add-custom-xml-parts-to-documents-by-using-vsto-add-ins.md)
