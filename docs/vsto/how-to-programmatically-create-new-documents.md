---
title: 'Nasıl Yapılır: Program aracılığıyla yeni belgeler oluşturma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- templates [Office development in Visual Studio], custom document
- Word [Office development in Visual Studio], creating documents
- documents [Office development in Visual Studio], creating
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 71610d0bd2e957d932e31d83d06aca914bf8b585
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71251959"
---
# <a name="how-to-programmatically-create-new-documents"></a>Nasıl yapılır: Program aracılığıyla yeni belgeler oluşturma
  Programlı olarak bir belge oluşturduğunuzda, yeni belge yerel <xref:Microsoft.Office.Interop.Word.Document> bir nesnedir. Bu nesne, bir <xref:Microsoft.Office.Tools.Word.Document> konak öğesinin ek olaylarına ve veri bağlama özelliklerine sahip değil. Daha fazla bilgi için bkz. [konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md).

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

 Belge düzeyi projesi geliştirirken, projenize programlama yoluyla konak öğeleri ekleyemezsiniz <xref:Microsoft.Office.Tools.Word.Document> . Bir VSTO eklenti projesinde, çalışma zamanında herhangi <xref:Microsoft.Office.Interop.Word.Document> bir nesneyi bir <xref:Microsoft.Office.Tools.Word.Document> konak öğesine dönüştürebilirsiniz. Daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

## <a name="to-create-a-new-document-based-on-the-normal-template"></a>Normal şablona dayalı yeni bir belge oluşturmak için

- Normal şablonu temel alan yeni <xref:Microsoft.Office.Interop.Word.Documents> bir belge oluşturmak için koleksiyonun yönteminikullanın.<xref:Microsoft.Office.Interop.Word.Documents.Add%2A> Bu kod örneğini kullanmak için, projenizdeki `ThisDocument` veya `ThisAddIn` sınıfından çalıştırın.

     [!code-vb[Trin_VstcoreWordAutomation#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#1)]
     [!code-csharp[Trin_VstcoreWordAutomation#1](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#1)]

## <a name="use-custom-templates"></a>Özel Şablonlar kullanma
 Yöntemi, normal şablondan başka bir şablonu temel alan yeni bir belge oluşturmak için isteğe bağlı bir şablon bağımsız değişkenine sahiptir. <xref:Microsoft.Office.Interop.Word.Documents.Add%2A> Şablonun dosya adını ve tam yolunu sağlamanız gerekir.

### <a name="to-create-a-new-document-based-on-a-custom-template"></a>Özel bir şablonu temel alan yeni bir belge oluşturmak için

- <xref:Microsoft.Office.Interop.Word.Documents> Koleksiyonun yöntemini çağırın ve şablonun yolunu belirtin. <xref:Microsoft.Office.Interop.Word.Documents.Add%2A> Bu kod örneğini kullanmak için, projenizdeki `ThisDocument` veya `ThisAddIn` sınıfından çalıştırın.

     [!code-vb[Trin_VstcoreWordAutomation#2](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#2)]
     [!code-csharp[Trin_VstcoreWordAutomation#2](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#2)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Varolan belgeleri program aracılığıyla açma](../vsto/how-to-programmatically-open-existing-documents.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
