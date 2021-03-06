---
title: 'Nasıl yapılır: Program aracılığıyla bulunan öğeler arasında döngü'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- loops, through found items in documents
- documents [Office development in Visual Studio], searching
- text [Office development in Visual Studio], searching in documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 22f8035cc7c1b09e7fd54f3c10842237ee6273b9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62812421"
---
# <a name="how-to-programmatically-loop-through-found-items-in-documents"></a>Nasıl yapılır: Program aracılığıyla bulunan öğeler arasında döngü
  <xref:Microsoft.Office.Interop.Word.Find> Sınıfında bir <xref:Microsoft.Office.Interop.Word.Find.Found%2A> döndüren özellik **true** olduğunda Aranan öğe bulundu. Bulunan tüm örnekleri arasında döngü bir <xref:Microsoft.Office.Interop.Word.Range> kullanarak <xref:Microsoft.Office.Interop.Word.Find.Execute%2A> yöntemi.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="to-loop-through-found-items"></a>Bulunan öğeler arasında döngü

1. Bildirme bir <xref:Microsoft.Office.Interop.Word.Range> nesne.

    Aşağıdaki kod örneği belge düzeyi özelleştirmesinde kullanılabilir.

    [!code-vb[Trin_VstcoreWordAutomation#79](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#79)]
    [!code-csharp[Trin_VstcoreWordAutomation#79](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#79)]

    Aşağıdaki kod örneği, VSTO eklentisi içinde kullanılabilir. Bu örnek etkin belgeyi kullanır.

    [!code-vb[Trin_VstcoreWordAutomationAddIn#79](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#79)]
    [!code-csharp[Trin_VstcoreWordAutomationAddIn#79](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#79)]

2. Kullanım <xref:Microsoft.Office.Interop.Word.Find.Found%2A> belge dizenin tüm oluşumlarını arayın ve bir tam sayı değişkeni her zaman 1 artırmak için bir döngü özelliğinde dize bulundu.

    [!code-vb[Trin_VstcoreWordAutomation#80](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#80)]
    [!code-csharp[Trin_VstcoreWordAutomation#80](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#80)]

3. Bir ileti kutusunda dizenin bulunup sayısını görüntüler.

    [!code-vb[Trin_VstcoreWordAutomation#81](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#81)]
    [!code-csharp[Trin_VstcoreWordAutomation#81](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#81)]

   Aşağıdaki örnekler, ayrıntılı bir yöntemi gösterir.

## <a name="document-level-customization-example"></a>Belge düzeyi özelleştirmesi örneği

### <a name="to-loop-through-items-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesinde öğeler arasında döngü için

1. Aşağıdaki örnek, bir belge düzeyi özelleştirmesi için tam kod gösterilir. Bu kodu kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomation#78](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#78)]
     [!code-csharp[Trin_VstcoreWordAutomation#78](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#78)]

## <a name="vsto-add-in-example"></a>VSTO eklenti örneği

### <a name="to-loop-through-items-in-a-vsto-add-in"></a>Bir VSTO eklentisi öğeler arasında döngü için

1. Aşağıdaki örnek, VSTO eklentisi için tam kod gösterilmektedir. Bu kodu kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#78](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#78)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#78](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#78)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Program aracılığıyla arama ve belgelerdeki rext değiştirin](../vsto/how-to-programmatically-search-for-and-replace-text-in-documents.md)
- [Nasıl yapılır: Program aracılığıyla Word arama seçeneklerini ayarlama](../vsto/how-to-programmatically-set-search-options-in-word.md)
- [Nasıl yapılır: Program aracılığıyla tanımlama ve belgelerde aralıkları seçin](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)
- [Nasıl yapılır: Program aracılığıyla aramalardan sonra seçimleri geri yükleme](../vsto/how-to-programmatically-restore-selections-after-searches.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
