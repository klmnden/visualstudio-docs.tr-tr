---
title: Genişletilmiş nesneleri kullanarak Word'ü otomatikleştirirken
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Word [Office development in Visual Studio], automating
- extended objects [Office development in Visual Studio], Word
- automation [Office development in Visual Studio], Word
- host items [Office development in Visual Studio], Word
- automating Word
- controls [Office development in Visual Studio], Word host controls
- host controls, Word
- host controls [Office development in Visual Studio], Word
- Word [Office development in Visual Studio], host controls
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: c75708afa3c230dcc4bba308cf2d7c97b77d802b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62939557"
---
# <a name="automate-word-by-using-extended-objects"></a>Genişletilmiş nesneleri kullanarak Word'ü otomatikleştirirken
  Visual Studio'da Word çözümleri geliştirirken kullanabileceğiniz *konak öğelerini* ve *konak kontrolü*Çözümlerinizdeki s. Bunlar gibi Word nesne modeli (Word için birincil birlikte çalışma derlemesi tarafından sunulan diğer bir deyişle, nesne modeli) yaygın olarak kullanılan belirli nesneleri genişleten nesnelerdir <xref:Microsoft.Office.Interop.Word.Document> ve <xref:Microsoft.Office.Interop.Word.ContentControl> nesneleri. Genişletilmiş nesneler temel aldıkları Word nesneleri gibi davranırlar fakat nesnelere veri bağlama becerileri ve ek olaylar ekleyin.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

 Bu kullanılabilecek bağlam çözümü her tür için farklı olmasına karşın konak denetimlerinin ve konak öğelerinin VSTO eklentileri hem belge düzeyi özelleştirmeleri için de kullanılabilir. Daha fazla bilgi için [konak öğelerini ve denetimlerine genel bakış için ana bilgisayar](../vsto/host-items-and-host-controls-overview.md).

## <a name="document-host-item"></a>Belge konak öğesi
 Word projeleri verin erişmenizi <xref:Microsoft.Office.Tools.Word.Document> konak öğesi. <xref:Microsoft.Office.Tools.Word.Document> Konak öğesi konak denetimleri ve Windows Forms denetimleri de dahil olmak üzere, diğer denetimler için kapsayıcı olarak davranır ve yüzeyinde denetimler hakkında bilgi içerir. <xref:Microsoft.Office.Tools.Word.Document> Konak öğesi de aynı üyeleri çoğunu sağlar <xref:Microsoft.Office.Interop.Word.Document> Word nesne modelinde karşılık gelen sınıf olan sınıf.

 Daha fazla bilgi için [belge konak öğesi](../vsto/document-host-item.md).

## <a name="word-host-controls"></a>Word konak denetimleri
 Word için yardımcı denetimler oluşturmak, düzenlemek ve belgeleri otomatikleştirmek birden çok konak vardır. Çoğu işlevleriyle alma, sunmak ve veri koruma içerir. Bu konak denetimleri, olayları ve yerel Word nesne modelinde karşılıkları olmayan veri bağlama özellikleri sağlar.

 Belge düzeyinde projelerde, tasarım zamanında belgenize herhangi bir ana bilgisayar denetimi ekleyebilirsiniz veya içerik denetimleri ve yer işareti denetimlerini çalışma zamanında ekleyebilirsiniz. VSTO eklenti projesinde herhangi bir açık belgeye çalışma zamanında içerik denetimleri ve yer işareti denetimi ekleyebilirsiniz.

 Word projelerinde kullanabileceğiniz konak denetimleri hakkında daha fazla bilgi için aşağıdaki konulara bakın:

- [İçerik denetimleri](../vsto/content-controls.md)

- [Yer işareti denetimi](../vsto/bookmark-control.md)

- [XMLNode denetimi](../vsto/xmlnode-control.md)

- [XMLNodes denetimi](../vsto/xmlnodes-control.md)

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Word belgelerine içerik denetimleri ekleme](../vsto/how-to-add-content-controls-to-word-documents.md)
- [Nasıl yapılır: Word belgelerine yer işareti denetimi ekleme](../vsto/how-to-add-bookmark-controls-to-word-documents.md)
- [Nasıl yapılır: Word belgelerine XMLNode denetimleri ekleme](../vsto/how-to-add-xmlnode-controls-to-word-documents.md)
- [Nasıl yapılır: Word belgelerine XMLNodes denetimleri ekleme](../vsto/how-to-add-xmlnodes-controls-to-word-documents.md)
- [Nasıl yapılır: Yer işareti denetimlerini yeniden boyutlandırma](../vsto/how-to-resize-bookmark-controls.md)
- [İzlenecek yol: İçerik denetimlerini kullanarak şablon oluşturma](../vsto/walkthrough-creating-a-template-by-using-content-controls.md)
- [İzlenecek yol: İçerik denetimlerini özel XML bölümlerine bağlama](../vsto/walkthrough-binding-content-controls-to-custom-xml-parts.md)
- [İzlenecek yol: Yer işaretleri için kısayol menüleri oluşturma](../vsto/walkthrough-creating-shortcut-menus-for-bookmarks.md)
- [Word çözümleri](../vsto/word-solutions.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Word belgelerini ve Excel çalışma kitaplarını VSTO eklentileri çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
