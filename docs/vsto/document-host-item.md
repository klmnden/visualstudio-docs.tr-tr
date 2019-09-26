---
title: Belge konak öğesi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio]
- documents [Office development in Visual Studio], document host items
- document host items
- Word [Office development in Visual Studio], Word documents
- Word [Office development in Visual Studio]
- Word documents
- host items [Office development in Visual Studio], Document
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ebea0c3a09d08741523deddce94def170d844202
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253704"
---
# <a name="document-host-item"></a>Belge konak öğesi
  Konak öğesi, Word için birincil birlikte çalışma derlemesinden <xref:Microsoft.Office.Interop.Word.Document> türü genişleten bir türdür. <xref:Microsoft.Office.Tools.Word.Document> Konak öğesi, aynı özellikleri, yöntemleri ve olayları bir <xref:Microsoft.Office.Interop.Word.Document> nesne olarak sağlar, ancak ayrıca ek olaylar sunar ve konak denetimleri ve Windows Forms denetimleri için bir kapsayıcı görevi görür. <xref:Microsoft.Office.Tools.Word.Document>

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

 Belge düzeyi projelerinde, projenizdeki belgeyi temsil eden bir varsayılan <xref:Microsoft.Office.Tools.Word.Document> konak öğesi vardır. VSTO eklenti projelerinde, <xref:Microsoft.Office.Tools.Word.Document> çalışma zamanında konak öğeleri oluşturabilirsiniz.

## <a name="understand-the-document-host-item-in-document-level-projects"></a>Belge düzeyi projelerdeki belge konak öğesini anlayın
 Projenizdeki belgeye erişmek için `ThisDocument` sınıfını kullanın. Belge düzeyinde bir proje oluşturduğunuzda, Visual Studio Word ile özelleştirme kodunuz arasında `ThisDocument` iletişim bağlantısı olarak kullanılacak sınıfı oluşturur. Sınıfı, özelleştirme sırasında kod çalıştırma veya kapatma gibi <xref:Microsoft.Office.Tools.Word.Document> temel görevleri gerçekleştirmek için konak öğesinin üyelerine erişmenizi sağlar. `ThisDocument` Belgeye denetim eklemek için sınıfını da kullanabilirsiniz. Farklı denetim kümelerini birleştirerek ve kod yazarken, denetimleri verilere bağlayabilir, kullanıcıdan bilgi toplayabilir ve kullanıcı eylemlerine yanıt verebilirsiniz. Daha fazla bilgi için bkz. [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md).

 Sınıfı `ThisDocument` , projenizde kod yazmaya başlayabilmeniz için bir konum sağlar. Sınıfı, Word için birincil birlikte çalışma derlemesindeki <xref:Microsoft.Office.Interop.Word.Document> nesne olarak aynı özellikleri, yöntemleri ve olayları sağladığından, Word nesne modeline erişmek için de kullanabilirsiniz. `ThisDocument` Daha fazla bilgi için bkz. [Word nesne modeline genel bakış](../vsto/word-object-model-overview.md).

### <a name="limitations-of-the-document-host-item-in-document-level-projects"></a>Belge düzeyi projelerdeki belge konak öğesinin sınırlamaları
 Belge düzeyindeki bir proje yalnızca bir <xref:Microsoft.Office.Tools.Word.Document> konak öğesi (yani `ThisDocument` , sınıfı) içerebilir. Tasarım zamanında projenize yeni <xref:Microsoft.Office.Tools.Word.Document> konak öğeleri ekleyemez ve çalışma zamanında belge düzeyi özelleştirmesindeki yeni <xref:Microsoft.Office.Tools.Word.Document> konak öğeleri oluşturamazsınız.

 Çalışma zamanında yeni bir Word belgesi oluşturursanız, bu, türü <xref:Microsoft.Office.Interop.Word.Document>olacaktır. Konak öğesi olmadığından, hiçbir konak denetimi veya Windows Forms denetimi içeremez. Çalışma zamanında belge oluşturma hakkında daha fazla bilgi için bkz [. nasıl yapılır: Program aracılığıyla yeni belgeler](../vsto/how-to-programmatically-create-new-documents.md)oluşturun.

## <a name="understand-document-host-items-in-application-level-projects"></a>Uygulama düzeyi projelerindeki belge konak öğelerini anlama
 VSTO eklenti projelerinde, Word 'de açık olan herhangi bir belge <xref:Microsoft.Office.Tools.Word.Document> için çalışma zamanında bir konak öğesi oluşturabilirsiniz. İlişkili belgeye denetim eklemek <xref:Microsoft.Office.Tools.Word.Document> veya <xref:Microsoft.Office.Interop.Word.Document> nesnelerde kullanılamayan olayları işlemek için konak öğesini kullanabilirsiniz.

 Bir <xref:Microsoft.Office.Tools.Word.Document> konak öğesi oluşturmak için `GetVstoObject` yöntemini kullanın. Daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Genişletilmiş nesneleri kullanarak Word 'Ü otomatikleştirme](../vsto/automating-word-by-using-extended-objects.md)
- [Word nesne modeline genel bakış](../vsto/word-object-model-overview.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
