---
title: Aralıkları program aracılığıyla oluştururken paragraf işaretlerini hariç tutma
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], excluding paragraphs
- ranges, excluding paragraph marks in Word
- documents [Office development in Visual Studio], paragraph marks
- paragraphs, controlling structure
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 852dc6c51215e00c1fdc1571f51940a44f727794
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66402149"
---
# <a name="how-to-programmatically-exclude-paragraph-marks-when-creating-ranges"></a>Nasıl yapılır: Aralık oluştururken program aracılığıyla dışlama paragraf işaretleri
  Oluşturduğunuz her bir <xref:Microsoft.Office.Interop.Word.Range> bir paragraf paragraf işaretlerini gibi tüm yazdırılamayan karakterler temel nesne aralığında dahil edilir. Kaynak paragrafı hedef paragrafa metin eklemek isteyebilirsiniz. Hedef paragraf farklı paragraflara ayırmak istemiyorsanız, ilk paragraf işaretlerini kaynak paragrafın kaldırmalısınız. Ayrıca, paragraf işaretleri içinde paragraf biçimlendirme bilgilerini depolandığından, varolan paragrafa aralığı eklediğinizde bu içerecek şekilde istemeyebilirsiniz.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

 Aşağıdaki örnek yordamı iki dize değişkeni bildirir, etkin belgedeki ilk ve ikinci paragraf içeriğini alır ve ardından içeriklerini birbiriyle değiştirir. Örnek, ardından paragraf işaretçisini kullanarak aralıktan kaldırma gösterir <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> yöntemi ve paragraf içinde metin ekleme.

## <a name="to-control-paragraph-structure-when-inserting-text"></a>Paragraf yapısını metin eklerken denetlemek için

1. Birinci ve ikinci paragrafları için iki aralık değişkeni oluşturun ve kullanarak içerikleri almak <xref:Microsoft.Office.Interop.Word.Range.Text%2A> özelliği.

     Aşağıdaki kod örneği belge düzeyi özelleştirmesinde kullanılabilir.

     [!code-vb[Trin_VstcoreWordAutomation#27](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#27)]
     [!code-csharp[Trin_VstcoreWordAutomation#27](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#27)]

     Aşağıdaki kod örneği, bir uygulama düzeyinde VSTO eklenti kullanılabilir. Bu kod, etkin belgeyi kullanır.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#27](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#27)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#27](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#27)]

2. Ata <xref:Microsoft.Office.Interop.Word.Range.Text%2A> iki paragraflar arasındaki metni değiştirme özelliği.

     [!code-vb[Trin_VstcoreWordAutomation#28](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#28)]
     [!code-csharp[Trin_VstcoreWordAutomation#28](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#28)]

3. Sırayla her bir aralığı seçin ve sonuçları bir ileti kutusunda görüntülenecek duraklatabilirsiniz.

     [!code-vb[Trin_VstcoreWordAutomation#29](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#29)]
     [!code-csharp[Trin_VstcoreWordAutomation#29](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#29)]

4. Ayarlama `firstRange` kullanarak <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> yöntemi paragraf işaret artık bir parçası olması `firstRange`.

     [!code-vb[Trin_VstcoreWordAutomation#30](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#30)]
     [!code-csharp[Trin_VstcoreWordAutomation#30](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#30)]

5. Yeni bir dize atama ilk paragrafa metin rest değiştirin <xref:Microsoft.Office.Interop.Word.Range.Text%2A> aralık özelliği.

     [!code-vb[Trin_VstcoreWordAutomation#31](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#31)]
     [!code-csharp[Trin_VstcoreWordAutomation#31](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#31)]

6. Metni Değiştir `secondRange`, paragraf işaretlerini de dahil olmak üzere.

     [!code-vb[Trin_VstcoreWordAutomation#32](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#32)]
     [!code-csharp[Trin_VstcoreWordAutomation#32](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#32)]

7. Seçin `firstRange` ve sonuçları bir ileti kutusu içinde görüntülemek için Duraklat ve ile aynı yapmak `secondRange`.

     Bu yana `firstRange` tanımlandığından paragraf işaretlerini hariç tutmak için özgün paragraf biçimlendirmesini korunur. Bir cümle paragraf işaretlerini ancak eklenir `secondRange`, ayrı paragraf kaldırılıyor.

     [!code-vb[Trin_VstcoreWordAutomation#33](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#33)]
     [!code-csharp[Trin_VstcoreWordAutomation#33](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#33)]

     Belge orijinal durumuna geri yükleyebilmeniz için hem de aralık özgün içeriğini dize olarak kaydedildi.

8. Yeniden ayarlayın `firstRange` paragraf işaretlerini kullanarak içerecek şekilde <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> yöntemi için bir karakter konumu.

     [!code-vb[Trin_VstcoreWordAutomation#34](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#34)]
     [!code-csharp[Trin_VstcoreWordAutomation#34](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#34)]

9. `secondRange` klasörünü silin. Bu üç paragraf özgün konumuna geri yükler.

     [!code-vb[Trin_VstcoreWordAutomation#35](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#35)]
     [!code-csharp[Trin_VstcoreWordAutomation#35](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#35)]

10. Özgün paragraf metnini geri `firstRange`.

     [!code-vb[Trin_VstcoreWordAutomation#36](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#36)]
     [!code-csharp[Trin_VstcoreWordAutomation#36](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#36)]

11. Kullanım <xref:Microsoft.Office.Interop.Word.Range.InsertAfter%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Range> sonra özgün paragraf iki içerik eklemek için nesne `firstRange`ve ardından `firstRange`.

     [!code-vb[Trin_VstcoreWordAutomation#37](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#37)]
     [!code-csharp[Trin_VstcoreWordAutomation#37](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#37)]

## <a name="document-level-customization-example"></a>Belge düzeyi özelleştirmesi örneği

### <a name="to-control-paragraph-structure-when-inserting-text-in-document-level-customizations"></a>Metin belge düzeyinde özelleştirmeler eklerken paragraf yapısı denetlemek için

1. Aşağıdaki örnek, bir belge düzeyi özelleştirmesi için ayrıntılı bir yöntemi gösterir. Bu kodu kullanmak için çalıştırın `ThisDocument` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomation#26](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#26)]
     [!code-csharp[Trin_VstcoreWordAutomation#26](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#26)]

## <a name="vsto-add-in-example"></a>VSTO eklenti örneği

### <a name="to-control-paragraph-structure-when-inserting-text-in-a-vsto-add-in"></a>Metin bir VSTO eklenti eklenirken paragraf yapısını kontrol etmek için

1. Aşağıdaki örnek, VSTO eklentisi için ayrıntılı bir yöntemi gösterir. Bu kodu kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#26](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#26)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#26](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#26)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Belgelerde aralıkları program aracılığıyla genişletme](../vsto/how-to-programmatically-extend-ranges-in-documents.md)
- [Nasıl yapılır: Aralıkları veya seçimleri program aracılığıyla daraltma](../vsto/how-to-programmatically-collapse-ranges-or-selections-in-documents.md)
- [Nasıl yapılır: Word belgelerine program aracılığıyla metin ekleme](../vsto/how-to-programmatically-insert-text-into-word-documents.md)
- [Nasıl yapılır: Word belgelerinde aralıkları program aracılığıyla sıfırlama](../vsto/how-to-programmatically-reset-ranges-in-word-documents.md)
- [Nasıl yapılır: Program aracılığıyla tanımlama ve belgelerde aralıkları seçin](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
