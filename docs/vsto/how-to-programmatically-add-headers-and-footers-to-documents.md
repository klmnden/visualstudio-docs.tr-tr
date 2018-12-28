---
title: 'Nasıl Yapılır: Program aracılığıyla belgelere üstbilgiler ve altbilgiler ekleme'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- headers, adding to Office documents
- documents [Office development in Visual Studio], adding headers
- documents [Office development in Visual Studio], adding footers
- footers, adding to documents
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: d6baf57f8b34f6dc591a8e1a131bd665671322e9
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53803382"
---
# <a name="how-to-programmatically-add-headers-and-footers-to-documents"></a>Nasıl Yapılır: Program aracılığıyla belgelere üstbilgiler ve altbilgiler ekleme
  Metin için üstbilgiler ve altbilgiler belgenize kullanarak ekleyebileceğiniz <xref:Microsoft.Office.Interop.Word.Section.Headers%2A> özelliği ve <xref:Microsoft.Office.Interop.Word.Section.Footers%2A> özelliği <xref:Microsoft.Office.Interop.Word.Section>. Her bir belge bölümü, üç üstbilgiler ve altbilgiler içerir:  
  
- <xref:Microsoft.Office.Interop.Word.WdHeaderFooterIndex.wdHeaderFooterPrimary>  
  
- <xref:Microsoft.Office.Interop.Word.WdHeaderFooterIndex.wdHeaderFooterEvenPages>  
  
- <xref:Microsoft.Office.Interop.Word.WdHeaderFooterIndex.wdHeaderFooterFirstPage>  
  
  Yordamları, belge düzeyinde özelleştirmeler ve VSTO eklentileri için farklıdır.  
  
  [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
## <a name="document-level-customizations"></a>Belge düzeyinde özelleştirmeler  
 Aşağıdaki kod örnekleri kullanmak için onlardan çalıştırın `ThisDocument` projenizdeki sınıfı.  
  
### <a name="to-add-text-to-footers-in-the-document"></a>Altbilgi belgesi metin eklemek için  
  
1.  Aşağıdaki kod örneği, her bölümüne belgesinin birincil alt bilgisi eklenecek metin yazı tipini ayarlar ve sonra alt bilgi metni ekler.  
  
     [!code-vb[Trin_VstcoreWordAutomation#114](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#114)]
     [!code-csharp[Trin_VstcoreWordAutomation#114](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#114)]  
  
### <a name="to-add-text-to-headers-in-the-document"></a>Üst bilgileri belgede metin eklemek için  
  
1.  Aşağıdaki kod örneği, belgedeki her üst bilgisindeki sayfa numarasını gösteren bir alan ekler ve ardından metni üstbilgisinin sağa hizalar Paragraf hizalamasını ayarlar.  
  
     [!code-vb[Trin_VstcoreWordAutomation#116](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#116)]
     [!code-csharp[Trin_VstcoreWordAutomation#116](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#116)]  
  
## <a name="vsto-add-ins"></a>VSTO eklentileri  
 Aşağıdaki kod örnekleri kullanmak için onlardan çalıştırın `ThisAddIn` projenizdeki sınıfı.  
  
### <a name="to-add-text-to-footers-in-a-document"></a>Altbilgi bir belgede metin eklemek için  
  
1.  Aşağıdaki kod örneği, her bölümüne belgesinin birincil alt bilgisi eklenecek metin yazı tipini ayarlar ve sonra alt bilgi metni ekler. Bu kod örneği, etkin belgeyi kullanır.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#114](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#114)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#114](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#114)]  
  
### <a name="to-add-text-to-headers-in-the-document"></a>Üst bilgileri belgede metin eklemek için  
  
1.  Aşağıdaki kod örneği, belgedeki her üst bilgisindeki sayfa numarasını gösteren bir alan ekler ve ardından metni üstbilgisinin sağa hizalar Paragraf hizalamasını ayarlar. Bu kod örneği, etkin belgeyi kullanır.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#116](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#116)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#116](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#116)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Program aracılığıyla yeni belgeler oluşturma](../vsto/how-to-programmatically-create-new-documents.md)   
 [Nasıl yapılır: Belgelerde aralıkları program aracılığıyla genişletme](../vsto/how-to-programmatically-extend-ranges-in-documents.md)   
 [Nasıl yapılır: Program aracılığıyla bulunan öğeler arasında döngü](../vsto/how-to-programmatically-loop-through-found-items-in-documents.md)  
   