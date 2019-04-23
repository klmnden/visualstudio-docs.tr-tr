---
title: 'Nasıl yapılır: Program aracılığıyla belgeleri kapatma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], closing
- Word [Office development in Visual Studio], closing documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ca8537e6e28461bfd2e3b3d6d116571d15c04ea5
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60084446"
---
# <a name="how-to-programmatically-close-documents"></a>Nasıl yapılır: Program aracılığıyla belgeleri kapatma
  Etkin belgeyi kapatabilir veya kapatmak için bir belge belirtebilirsiniz.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="close-the-active-document"></a>Etkin belgeyi Kapat
 Etkin belgeyi kapatma için iki yordam vardır: belge düzeyi özelleştirmeleri ve VSTO eklentileri için.

### <a name="to-close-the-active-document-in-a-document-level-customization"></a>Etkin belgeyi belge düzeyi özelleştirmesinde kapatmak için

1. Çağrı <xref:Microsoft.Office.Tools.Word.Document.Close%2A> yöntemi `ThisDocument` özelleştirme ile ilişkilendirilen belge kapatmak için projenizdeki sınıfı. Aşağıdaki kod örneği kullanmak için çalıştırın `ThisDocument` sınıfı.

    > [!NOTE]
    >  Bu örnekte geçirir <xref:Microsoft.Office.Interop.Word.WdSaveOptions.wdDoNotSaveChanges> değerini *SaveChanges* değişiklikleri kaydetmeden veya kullanıcıdan kapatmak için parametre.

     [!code-vb[Trin_VstcoreWordAutomation#3](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#3)]
     [!code-csharp[Trin_VstcoreWordAutomation#3](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#3)]

### <a name="to-close-the-active-document-in-a-vsto-add-in"></a>Bir VSTO Eklentisi etkin belgede kapatmak için

1. Çağrı <xref:Microsoft.Office.Interop.Word._Document.Close%2A> yöntemi <xref:Microsoft.Office.Interop.Word._Application.ActiveDocument%2A> özelliği etkin belgeyi kapat. Aşağıdaki kod örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.

    > [!NOTE]
    >  Bu örnekte geçirir <xref:Microsoft.Office.Interop.Word.WdSaveOptions.wdDoNotSaveChanges> değerini *SaveChanges* değişiklikleri kaydetmeden veya kullanıcıdan kapatmak için parametre.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#3](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#3)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#3](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#3)]

## <a name="close-a-document-that-you-specify-by-name"></a>Belirttiğiniz ada göre bir belgeyi Kapat
 Belirttiğiniz ada göre bir belgeyi Kapat şekilde VSTO eklentileri ve belge düzeyi özelleştirmeleri için aynıdır.

### <a name="to-close-a-document-that-you-specify-by-name"></a>Belirttiğiniz ada göre bir belgeyi kapatmak için

1. Belge adı bağımsız değişkeni olarak belirtin <xref:Microsoft.Office.Interop.Word._Application.Documents%2A> koleksiyonu ve ardından bir çağrı <xref:Microsoft.Office.Interop.Word._Document.Close%2A> yöntemi. Aşağıdaki kod örneği bir belge adlı olduğunu varsayar **NewDocument** Word'de açık olduğu.

    > [!NOTE]
    >  Bu örnekte geçirir <xref:Microsoft.Office.Interop.Word.WdSaveOptions.wdDoNotSaveChanges> değerini *SaveChanges* değişiklikleri kaydetmeden veya kullanıcıdan kapatmak için parametre.

     [!code-vb[Trin_VstcoreWordAutomation#4](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#4)]
     [!code-csharp[Trin_VstcoreWordAutomation#4](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#4)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Varolan belgeleri program aracılığıyla açma](../vsto/how-to-programmatically-open-existing-documents.md)
- [Nasıl yapılır: Program aracılığıyla belgeleri kaydetme](../vsto/how-to-programmatically-save-documents.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
