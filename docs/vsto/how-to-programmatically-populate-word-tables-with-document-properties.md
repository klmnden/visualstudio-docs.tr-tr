---
title: Belge özellikleriyle Word tablolarını program aracılığıyla doldurma
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- document properties, inserting in Word tables
- documents [Office development in Visual Studio], document properties
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e296a63c208bc1c3316f89b7b4003f16daf3c93e
ms.sourcegitcommit: 13ab9a5ab039b070b9cd9251d0b83dd216477203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2019
ms.locfileid: "66177789"
---
# <a name="how-to-programmatically-populate-word-tables-with-document-properties"></a>Nasıl yapılır: Belge özellikleriyle Word tablolarını program aracılığıyla doldurma
  Aşağıdaki örnek, belgenin üst kısmında bir Microsoft Office Word tablo oluşturur ve ana belgenin özellikleri ile doldurur.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="populate-tables-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesinde tablolarını doldurma

### <a name="to-create-a-table-and-populate-it-with-document-properties"></a>Bir tablo oluşturun ve belge özellikleri ile doldurmak için

1. Belgenin üst kısmında için aralığı ayarlayın.

    [!code-vb[Trin_VstcoreWordAutomation#90](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#90)]
    [!code-csharp[Trin_VstcoreWordAutomation#90](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#90)]

2. Tablo için bir başlık ekleyin ve paragraf işaretleri ekleyin.

    [!code-vb[Trin_VstcoreWordAutomation#91](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#91)]
    [!code-csharp[Trin_VstcoreWordAutomation#91](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#91)]

3. Tablo aralığı belge ekleyin.

    [!code-vb[Trin_VstcoreWordAutomation#92](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#92)]
    [!code-csharp[Trin_VstcoreWordAutomation#92](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#92)]

4. Tabloyu biçimlendirme ve stil uygulayabilirsiniz.

    [!code-vb[Trin_VstcoreWordAutomation#93](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#93)]
    [!code-csharp[Trin_VstcoreWordAutomation#93](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#93)]

5. Belge özellikleri hücrelere ekleyin.

    [!code-vb[Trin_VstcoreWordAutomation#94](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#94)]
    [!code-csharp[Trin_VstcoreWordAutomation#94](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#94)]

   Aşağıdaki örnek, tam bir yordam gösterir. Bu kodu kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.

   [!code-vb[Trin_VstcoreWordAutomation#89](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#89)]
   [!code-csharp[Trin_VstcoreWordAutomation#89](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#89)]

## <a name="populate-tables-in-a-vsto-add-in"></a>Bir VSTO eklentisi tablolarında Doldur

### <a name="to-create-a-table-and-populate-it-with-document-properties"></a>Bir tablo oluşturun ve belge özellikleri ile doldurmak için

1. Belgenin üst kısmında için aralığı ayarlayın.

    [!code-vb[Trin_VstcoreWordAutomationAddIn#90](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#90)]
    [!code-csharp[Trin_VstcoreWordAutomationAddIn#90](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#90)]

2. Tablo için bir başlık ekleyin ve paragraf işaretleri ekleyin.

    [!code-vb[Trin_VstcoreWordAutomationAddIn#91](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#91)]
    [!code-csharp[Trin_VstcoreWordAutomationAddIn#91](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#91)]

3. Tablo aralığı belge ekleyin.

    [!code-vb[Trin_VstcoreWordAutomationAddIn#92](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#92)]
    [!code-csharp[Trin_VstcoreWordAutomationAddIn#92](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#92)]

4. Tabloyu biçimlendirme ve stil uygulayabilirsiniz.

    [!code-vb[Trin_VstcoreWordAutomationAddIn#93](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#93)]
    [!code-csharp[Trin_VstcoreWordAutomationAddIn#93](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#93)]

5. Belge özellikleri hücrelere ekleyin.

    [!code-vb[Trin_VstcoreWordAutomationAddIn#94](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#94)]
    [!code-csharp[Trin_VstcoreWordAutomationAddIn#94](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#94)]

   Aşağıdaki örnek, tam bir yordam gösterir. Bu kodu kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.

   [!code-vb[Trin_VstcoreWordAutomationAddIn#89](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#89)]
   [!code-csharp[Trin_VstcoreWordAutomationAddIn#89](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#89)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Program aracılığıyla Word tabloları oluşturma](../vsto/how-to-programmatically-create-word-tables.md)
- [Nasıl yapılır: Metin ve biçimlendirme Word tablolarında hücrelere program aracılığıyla ekleme](../vsto/how-to-programmatically-add-text-and-formatting-to-cells-in-word-tables.md)
- [Nasıl yapılır: Word tablolarına program aracılığıyla satır ve sütun ekleme](../vsto/how-to-programmatically-add-rows-and-columns-to-word-tables.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
