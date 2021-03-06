---
title: 'Nasıl yapılır: Program aracılığıyla Word belgelerine metin ekleme'
ms.date: 08/14/2019
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, inserting text in documents
- text [Office development in Visual Studio], inserting in documents
- ranges, replacing text in documents
- documents [Office development in Visual Studio], inserting text
- text [Office development in Visual Studio], replacing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 8ff5e0314e9834bd3d0f048bc82780d7e4af073d
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69551809"
---
# <a name="how-to-programmatically-insert-text-into-word-documents"></a>Nasıl yapılır: Program aracılığıyla Word belgelerine metin ekleme
  Microsoft Office Word belgelerine metin eklemenin üç temel yolu vardır:

- Bir aralığa metin ekleyin.

- Bir aralıktaki metni yeni metinle değiştirin.

- İmleç veya seçime metin eklemek <xref:Microsoft.Office.Interop.Word.Selection> için bir nesnenin yönteminikullanın.<xref:Microsoft.Office.Interop.Word.Selection.TypeText%2A>

> [!NOTE]
> Ayrıca içerik denetimlerine ve yer işaretlerine metin ekleyebilirsiniz. Daha fazla bilgi için bkz. [içerik denetimleri](../vsto/content-controls.md) ve [yer işareti denetimi](../vsto/bookmark-control.md).

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

[!include[Add-ins note](includes/addinsnote.md)]

## <a name="insert-text-in-a-range"></a>Bir aralığa metin ekleme
 Bir belgeye metin eklemek için <xref:Microsoft.Office.Interop.Word.Range> nesnesinin özelliğinikullanın.<xref:Microsoft.Office.Interop.Word.Range.Text%2A>

### <a name="to-insert-text-in-a-range"></a>Bir aralığa metin eklemek için

1. Belgenin başlangıcında bir Aralık belirtin ve metin **Yeni metin**ekleyin.

     Aşağıdaki kod örneği, belge düzeyi özelleştirmesinde kullanılabilir.

     [!code-vb[Trin_VstcoreWordAutomation#51](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#51)]
     [!code-csharp[Trin_VstcoreWordAutomation#51](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#51)]

     Aşağıdaki kod örneği bir VSTO eklentisi içinde kullanılabilir. Bu kod etkin belgeyi kullanır.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#51](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#51)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#51](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#51)]

2. Bir karakterden, ekli metnin uzunluğuna kadar genişletilen nesneyiseçin.<xref:Microsoft.Office.Interop.Word.Range>

     [!code-vb[Trin_VstcoreWordAutomation#52](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#52)]
     [!code-csharp[Trin_VstcoreWordAutomation#52](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#52)]

## <a name="replace-text-in-a-range"></a>Bir aralıktaki metni değiştirme
 Belirtilen Aralık metin içeriyorsa, aralıktaki tüm metin, girilen metinle birlikte değişir.

### <a name="to-replace-text-in-a-range"></a>Bir aralıktaki metni değiştirmek için

1. Belgedeki ilk <xref:Microsoft.Office.Interop.Word.Range> 12 karakterden oluşan bir nesne oluşturun.

     Aşağıdaki kod örneği, belge düzeyi özelleştirmesinde kullanılabilir.

     [!code-vb[Trin_VstcoreWordAutomation#53](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#53)]
     [!code-csharp[Trin_VstcoreWordAutomation#53](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#53)]

     Aşağıdaki kod örneği bir VSTO eklentisi içinde kullanılabilir. Bu kod etkin belgeyi kullanır.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#53](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#53)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#53](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#53)]

2. Bu karakterleri dize **yeni metinle**değiştirin.

     [!code-vb[Trin_VstcoreWordAutomation#54](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#54)]
     [!code-csharp[Trin_VstcoreWordAutomation#54](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#54)]

3. Aralığı seçin.

     [!code-vb[Trin_VstcoreWordAutomation#55](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#55)]
     [!code-csharp[Trin_VstcoreWordAutomation#55](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#55)]

## <a name="insert-text-using-typetext"></a>TypeText kullanarak metin ekleme
 <xref:Microsoft.Office.Interop.Word.Selection.TypeText%2A> Yöntemi, Seçime metin ekler. <xref:Microsoft.Office.Interop.Word.Selection.TypeText%2A>kullanıcının bilgisayarında ayarlanan seçeneklere bağlı olarak farklı davranır. Aşağıdaki yordamdaki kod bir <xref:Microsoft.Office.Interop.Word.Selection> nesne değişkeni bildirir ve açıksa **üzerine yazma** seçeneğini kapatır. **Üzerine yazma** seçeneği etkinleştirilirse, imlecin yanındaki tüm metinlerin üzerine yazılır.

### <a name="to-insert-text-using-the-typetext-method"></a>TypeText yöntemini kullanarak metin eklemek için

1. Bir <xref:Microsoft.Office.Interop.Word.Selection> nesne değişkeni bildirin.

    [!code-vb[Trin_VstcoreWordAutomation#57](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#57)]
    [!code-csharp[Trin_VstcoreWordAutomation#57](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#57)]

2. Açıksa **üzerine yazma** seçeneğini kapatın.

    [!code-vb[Trin_VstcoreWordAutomation#58](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#58)]
    [!code-csharp[Trin_VstcoreWordAutomation#58](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#58)]

3. Geçerli seçimin bir ekleme noktası olup olmadığını görmek için test edin.

    Eğer ise, kod kullanarak <xref:Microsoft.Office.Interop.Word.Selection.TypeText%2A>bir tümce ve sonra <xref:Microsoft.Office.Interop.Word.Selection.TypeParagraph%2A> yöntemi kullanılarak bir paragraf işareti eklenir.

    [!code-vb[Trin_VstcoreWordAutomation#59](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#59)]
    [!code-csharp[Trin_VstcoreWordAutomation#59](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#59)]

4. Seçimin normal bir seçim olup olmadığını görmek için **ElseIf** blok içindeki kod. Eğer ise, **ReplaceSelection** seçeneğinin açık olup olmadığını görmek için engelle ' yi **seçerseniz** , başka bir durumda. Eğer ise, kod seçili metin bloğunun başlangıcında <xref:Microsoft.Office.Interop.Word.Selection.Collapse%2A> seçimi bir ekleme noktasına daraltmak için seçimin yöntemini kullanır. Metni ve paragraf işaretini ekleyin.

    [!code-vb[Trin_VstcoreWordAutomation#60](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#60)]
    [!code-csharp[Trin_VstcoreWordAutomation#60](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#60)]

5. Seçim bir ekleme noktası veya seçili metin bloğu değilse, **Else** bloğundaki kod hiçbir şey yapmaz.

    [!code-vb[Trin_VstcoreWordAutomation#61](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#61)]
    [!code-csharp[Trin_VstcoreWordAutomation#61](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#61)]

   Ayrıca, klavyenizde <xref:Microsoft.Office.Interop.Word.Selection.TypeBackspace%2A> **geri al** tuşunun işlevlerini taklit <xref:Microsoft.Office.Interop.Word.Selection> eden nesnenin yöntemini de kullanabilirsiniz. Ancak, metin <xref:Microsoft.Office.Interop.Word.Range> ekleme ve düzenleme için olduğunda nesnesi size daha fazla denetim sağlar.

   Aşağıdaki örnek, tüm kodu gösterir. Bu örneği kullanmak için, projenizdeki `ThisDocument` veya `ThisAddIn` sınıfından kodu çalıştırın.

   [!code-vb[Trin_VstcoreWordAutomation#56](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#56)]
   [!code-csharp[Trin_VstcoreWordAutomation#56](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#56)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Belgelerde programlı olarak metin biçimlendirme](../vsto/how-to-programmatically-format-text-in-documents.md)
- [Nasıl yapılır: Belgelerde aralıkları program aracılığıyla tanımlama ve seçme](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)
- [Nasıl yapılır: Belgelerde aralıkları program aracılığıyla genişletme](../vsto/how-to-programmatically-extend-ranges-in-documents.md)
