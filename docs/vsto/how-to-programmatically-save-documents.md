---
title: 'Nasıl yapılır: Program aracılığıyla belgeleri kaydetme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], saving
- Word [Office development in Visual Studio], saving documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: b4fbf8e4cb67d5216dc17c325911bb243fae6e1c
ms.sourcegitcommit: 5b34052a1c7d86179d7898ed532babb2d9dad4a3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2019
ms.locfileid: "69490616"
---
# <a name="how-to-programmatically-save-documents"></a>Nasıl yapılır: Program aracılığıyla belgeleri kaydetme

Microsoft Office Word belgelerini kaydetmek için birkaç yol vardır. Belge adını değiştirmeden bir belgeyi kaydedebilir veya bir belgeyi yeni bir adla kaydedebilirsiniz.

[!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="save-a-document-without-changing-the-name"></a>Adı değiştirmeden bir belgeyi kaydetme

### <a name="to-save-the-document-associated-with-a-document-level-customization"></a>Belge düzeyi özelleştirmesiyle ilişkili belgeyi kaydetmek için

1. <xref:Microsoft.Office.Tools.Word.Document> Sınıfının <xref:Microsoft.Office.Tools.Word.Document.Save%2A> yöntemini çağırın. Bu kod örneğini kullanmak için projenizdeki `ThisDocument` sınıftan çalıştırın.

     [!code-vb[Trin_VstcoreWordAutomation#7](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#7)]
     [!code-csharp[Trin_VstcoreWordAutomation#7](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#7)]

### <a name="to-save-the-active-document"></a>Etkin belgeyi kaydetmek için

1. Etkin belge için yöntemini çağırın. <xref:Microsoft.Office.Interop.Word._Document.Save%2A> Bu kod örneğini kullanmak için, projenizdeki `ThisDocument` veya `ThisAddIn` sınıfından çalıştırın.

    [!code-vb[Trin_VstcoreWordAutomation#8](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#8)]
    [!code-csharp[Trin_VstcoreWordAutomation#8](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#8)]

   Kaydetmek istediğiniz belgenin etkin belge olup olmadığından emin değilseniz, bu belgeye adına göre başvurabilirsiniz.

### <a name="to-save-a-document-specified-by-name"></a>Ada göre belirtilen bir belgeyi kaydetmek için

1. <xref:Microsoft.Office.Interop.Word.Documents> Koleksiyon için bir bağımsız değişken olarak belge adını kullanın. Bu kod örneğini kullanmak için, projenizdeki `ThisDocument` veya `ThisAddIn` sınıfından çalıştırın.

     [!code-vb[Trin_VstcoreWordAutomation#9](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#9)]
     [!code-csharp[Trin_VstcoreWordAutomation#9](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#9)]

## <a name="save-a-document-with-a-new-name"></a>Belgeyi yeni bir adla kaydetme

Yeni bir ada sahip bir belgeyi kaydetmek için yönteminikullanın.`SaveAs` Bir belge düzeyi Word projesinde veya herhangi <xref:Microsoft.Office.Tools.Word.Document> bir Word projesindeki yerel <xref:Microsoft.Office.Interop.Word.Document> bir nesne için konak öğesinin bu yöntemini kullanabilirsiniz. Bu yöntem, yeni dosya adını belirtmenizi gerektirir, ancak diğer bağımsız değişkenler isteğe bağlıdır.

> [!NOTE]
> <xref:Microsoft.Office.Interop.Word.ApplicationEvents4_Event.DocumentBeforeSave> Olay işleyicisinin`ThisDocument` içinde **SaveAs** iletişim kutusunu gösterip *Cancel* parametresini **false**olarak ayarlarsanız uygulama beklenmedik şekilde çıkabilir. *Cancel* parametresini **true**olarak ayarlarsanız, otomatik kaydetme 'nin devre dışı bırakıldığını belirten bir hata iletisi görüntülenir.

### <a name="to-save-the-document-associated-with-a-document-level-customization-with-a-new-name"></a>Belge düzeyi özelleştirmesiyle ilişkili belgeyi yeni bir adla kaydetmek için

1. Tam nitelenmiş bir yol ve `ThisDocument` dosya adı kullanarak, projenizdeki sınıfının yönteminiçağırın.`SaveAs` Bu adda bir dosya zaten varsa, bu klasörde sessizce üzerine yazılır. Bu kod örneğini kullanmak için `ThisDocument` sınıfından çalıştırın.

    > [!NOTE]
    > Bir hedef dizin yoksa veya dosya kaydetme ile ilgili başka sorunlar varsa yöntemibirözeldurumoluşturur.`SaveAs` Yöntemi etrafında veya çağırma yöntemi içinde bir`try...catch` blok kullanmak iyi bir uygulamadır. `SaveAs`

     [!code-vb[Trin_VstcoreWordAutomation#10](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#10)]
     [!code-csharp[Trin_VstcoreWordAutomation#10](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#10)]

### <a name="to-save-a-native-document-with-a-new-name"></a>Yerel bir belgeyi yeni bir adla kaydetmek için

1. Tam nitelikli bir yol ve <xref:Microsoft.Office.Interop.Word.Document> dosya adı kullanarak kaydetmek istediğiniz yönteminiçağırın.<xref:Microsoft.Office.Interop.Word._Document.SaveAs%2A> Bu adda bir dosya zaten varsa, bu klasörde sessizce üzerine yazılır.

     Aşağıdaki kod örneği, etkin belgeyi yeni bir adla kaydeder. Bu kod örneğini kullanmak için, projenizdeki `ThisDocument` veya `ThisAddIn` sınıfından çalıştırın.

    > [!NOTE]
    > Bir hedef dizin yoksa veya dosya kaydetme ile ilgili başka sorunlar varsa yöntemibirözeldurumoluşturur.<xref:Microsoft.Office.Interop.Word._Document.SaveAs%2A> TRY kullanmak iyi bir uygulamadır **...** yöntemi <xref:Microsoft.Office.Interop.Word._Document.SaveAs%2A> etrafında veya çağırma yöntemi içinde catch bloğu.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#10](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#10)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#10](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#10)]

## <a name="compile-the-code"></a>Kod derleme

Bu kod örneği şunları gerektirir:

- Belgeyi ada göre kaydetmek için *NewDocument. doc* adlı bir belge C sürücüsünde *Test* adlı bir dizinde bulunmalıdır.

- Belgeyi yeni bir adla kaydetmek için, C sürücüsünde *Test* adlı bir dizin bulunmalıdır.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Program aracılığıyla belgeleri kapatma](../vsto/how-to-programmatically-close-documents.md)
- [Nasıl yapılır: Varolan belgeleri program aracılığıyla açma](../vsto/how-to-programmatically-open-existing-documents.md)
- [Belge konak öğesi](../vsto/document-host-item.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
