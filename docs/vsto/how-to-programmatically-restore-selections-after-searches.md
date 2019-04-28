---
title: 'Nasıl yapılır: Program aracılığıyla aramalardan sonra seçimleri geri yükleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- searches, restoring selection after
- documents [Office development in Visual Studio], restoring selections
- selections, restoring after a search
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 672c66fef5d7400601ce69270b5cd4f525b34c7d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62955712"
---
# <a name="how-to-programmatically-restore-selections-after-searches"></a>Nasıl yapılır: Program aracılığıyla aramalardan sonra seçimleri geri yükleme
  Bul ve Değiştir bir belgede metin arama tamamlandıktan sonra kullanıcının özgün seçimi geri yüklemek isteyebilirsiniz.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

 Kod örneği yordamı kullanır iki <xref:Microsoft.Office.Interop.Word.Range> nesneleri. Geçerli depolar <xref:Microsoft.Office.Interop.Word.Selection>, ve diğeri bir arama aralığı olarak kullanmak için belgenin tamamını ayarlar.

## <a name="to-restore-the-users-original-selection-after-a-search"></a>Arama yaptıktan sonra kullanıcının özgün seçimi geri yüklemek için

1. Oluşturma <xref:Microsoft.Office.Interop.Word.Range> belge ve geçerli seçim nesneleri.

    [!code-vb[Trin_VstcoreWordAutomation#83](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#83)]
    [!code-csharp[Trin_VstcoreWordAutomation#83](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#83)]

2. Arama yapın ve işlemi değiştirin.

    [!code-vb[Trin_VstcoreWordAutomation#84](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#84)]
    [!code-csharp[Trin_VstcoreWordAutomation#84](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#84)]

3. Kullanıcının özgün seçimi geri yüklemek için başlangıç aralığı seçin.

    [!code-vb[Trin_VstcoreWordAutomation#85](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#85)]
    [!code-csharp[Trin_VstcoreWordAutomation#85](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#85)]

   Aşağıdaki örnek, ayrıntılı bir yöntemi gösterir.

## <a name="example"></a>Örnek
 [!code-vb[Trin_VstcoreWordAutomation#82](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#82)]
 [!code-csharp[Trin_VstcoreWordAutomation#82](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#82)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Program aracılığıyla arama ve belgelerdeki metni değiştirme](../vsto/how-to-programmatically-search-for-and-replace-text-in-documents.md)
- [Nasıl yapılır: Program aracılığıyla Word arama seçeneklerini ayarlama](../vsto/how-to-programmatically-set-search-options-in-word.md)
- [Nasıl yapılır: Program aracılığıyla bulunan öğeler arasında döngü](../vsto/how-to-programmatically-loop-through-found-items-in-documents.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
