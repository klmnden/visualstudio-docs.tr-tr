---
title: 'Nasıl yapılır: Program aracılığıyla Word arama seçeneklerini ayarlama'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- settings, Word search options
- documents [Office development in Visual Studio], search options
- Word, searching options
- searching, Word options
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 6e3b66bfd7f3f5d0ef0f4893efeb81c80df5d4ae
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62961881"
---
# <a name="how-to-programmatically-set-search-options-in-word"></a>Nasıl yapılır: Program aracılığıyla Word arama seçeneklerini ayarlama
  Microsoft Office Word belgelerinde seçimleri için arama seçeneklerini ayarlamak için iki yolu vardır:

- Özelliklerini ayarlamak bir <xref:Microsoft.Office.Interop.Word.Find> nesne.

- Bağımsız değişkenlerini kullanmak <xref:Microsoft.Office.Interop.Word.Find.Execute%2A> yöntemi bir <xref:Microsoft.Office.Interop.Word.Find> nesne.

  [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="use-properties-of-a-find-object"></a>Bir bulma nesnesinin özelliklerini kullanma
 Aşağıdaki kod özelliklerini ayarlar bir <xref:Microsoft.Office.Interop.Word.Find> Geçerli seçimdeki metni aramak için nesne. İleri, sarmalama ve metin, aramak için arama gibi arama ölçütleri özelliklerini olduğunu fark <xref:Microsoft.Office.Interop.Word.Find> nesne.

 Her özelliklerini ayarlama <xref:Microsoft.Office.Interop.Word.Find> nesne değil yararlı parametreler olarak aynı özelliklerini belirtmeniz gerekir çünkü C# kodu yazarken <xref:Microsoft.Office.Interop.Word.Find.Execute%2A> yöntemi. Bu nedenle bu örnekte, yalnızca Visual Basic kodunu içerir.

### <a name="to-set-search-options-using-a-find-object"></a>Bir bulma nesnesi ile arama seçeneklerini ayarlama

1. Özelliklerini ayarlama bir <xref:Microsoft.Office.Interop.Word.Find> seçim metin için ileriye doğru arama nesnesine **bana Bul**.

     [!code-vb[Trin_VstcoreWordAutomation#76](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#76)]

## <a name="use-execute-method-arguments"></a>Execute yöntemi bağımsız değişkenleri kullanma
 Aşağıdaki kod <xref:Microsoft.Office.Interop.Word.Find.Execute%2A> yöntemi bir <xref:Microsoft.Office.Interop.Word.Find> Geçerli seçimdeki metni aramak için nesne. İleri, sarmalama ve metin, aramak için arama gibi arama ölçütleri bir parametre olarak geçirilen bildirimi <xref:Microsoft.Office.Interop.Word.Find.Execute%2A> yöntemi.

### <a name="to-set-search-options-using-execute-method-arguments"></a>Execute yöntemi bağımsız değişken ile arama seçeneklerini ayarlama

1. Arama ölçütleri bir parametre olarak geçirmeniz <xref:Microsoft.Office.Interop.Word.Find.Execute%2A> seçim metin için ileriye doğru arama yapmanız gereken yöntemini **bana Bul**.

     [!code-vb[Trin_VstcoreWordAutomation#77](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#77)]
     [!code-csharp[Trin_VstcoreWordAutomation#77](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#77)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Program aracılığıyla arama ve belgelerdeki metni değiştirme](../vsto/how-to-programmatically-search-for-and-replace-text-in-documents.md)
- [Nasıl yapılır: Program aracılığıyla bulunan öğeler arasında döngü](../vsto/how-to-programmatically-loop-through-found-items-in-documents.md)
- [Nasıl yapılır: Program aracılığıyla aramalardan sonra seçimleri geri yükleme](../vsto/how-to-programmatically-restore-selections-after-searches.md)
