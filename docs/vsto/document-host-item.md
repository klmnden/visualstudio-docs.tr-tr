---
title: Belge konak öğesi
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
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
manager: douge
ms.workload:
- office
ms.openlocfilehash: ea85d0f0f9435795abf75973373e6f0ae7e3a949
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53647358"
---
# <a name="document-host-item"></a>Belge konak öğesi
  <xref:Microsoft.Office.Tools.Word.Document> Konak öğesi olan bir türü genişleten <xref:Microsoft.Office.Interop.Word.Document> Word için birincil birlikte çalışma bütünleştirilmiş koddan tür. <xref:Microsoft.Office.Tools.Word.Document> Konak öğesi tüm özellikleri, yöntemleri ve olayları olarak sağlayan bir <xref:Microsoft.Office.Interop.Word.Document> nesne, ancak ayrıca ek olayları ortaya koyan ve konak denetimleri ve Windows Forms denetimleri için kapsayıcı işlevi görür.  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
 Belge düzeyinde projelerde bir varsayılan yok <xref:Microsoft.Office.Tools.Word.Document> projenizdeki belgeyi temsil eden konak öğesi. VSTO eklentisi projelerinde oluşturabileceğiniz <xref:Microsoft.Office.Tools.Word.Document> çalışma zamanında konak öğelerini.  
  
## <a name="understand-the-document-host-item-in-document-level-projects"></a>Belge düzeyinde projelerde belge konak öğesi anlama  
 Projenizdeki belgeye erişmek için `ThisDocument` sınıfı. Bir belge düzeyi projesi oluşturduğunuzda, Visual Studio'nun oluşturduğu `ThisDocument` Word özelleştirme kodunuzu arasındaki iletişimi bağlantı olarak hizmet verecek sınıfı. `ThisDocument` Sınıf üyelerine erişim sağlar <xref:Microsoft.Office.Tools.Word.Document> özelleştirme, belge açıldığında veya kod çalıştırma gibi temel görevleri gerçekleştirmek için konak öğesi. Sınıfı, belgeye denetim eklemek için de kullanabilirsiniz. Farklı denetim kümelerini birleştirerek ve verilere denetimler bağlayabilirsiniz kod yazarken, kullanıcıdan bilgi toplamak ve kullanıcı eylemlerine yanıt. Daha fazla bilgi için [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md).  
  
 `ThisDocument` Sınıfı başlangıç projenizde kod yazma bir konum sağlar. Sınıfı, tüm özellikleri, yöntemleri ve olayları olarak sağladığından <xref:Microsoft.Office.Interop.Word.Document> nesne birincil birlikte çalışma derlemesi Word için de kullanabilirsiniz `ThisDocument` Word nesne modeli erişmek için. Daha fazla bilgi için [Word nesne modeline genel bakış](../vsto/word-object-model-overview.md).  
  
### <a name="limitations-of-the-document-host-item-in-document-level-projects"></a>Belge düzeyinde projelerde belge konak öğesi sınırlamaları  
 Tek bir belge düzeyi projesi içerebilir <xref:Microsoft.Office.Tools.Word.Document> konak öğesi (diğer bir deyişle, `ThisDocument` sınıfı). Yeni eklenemiyor <xref:Microsoft.Office.Tools.Word.Document> konak öğeleri projenize tasarım zamanında ve yeni oluşturamazsınız <xref:Microsoft.Office.Tools.Word.Document> konak öğelerini bir belge düzeyi özelleştirmesinde zamanında.  
  
 Çalışma zamanında yeni bir Word belgesi oluşturun, türü olacaktır <xref:Microsoft.Office.Interop.Word.Document>. Bir konak öğesi olmadığı için tüm konak veya Windows Forms denetimleri içeremez. Çalışma zamanında belgeler oluşturma hakkında daha fazla bilgi için bkz. [nasıl yapılır: Program aracılığıyla yeni belgeler oluşturma](../vsto/how-to-programmatically-create-new-documents.md).  
  
## <a name="understand-document-host-items-in-application-level-projects"></a>Belge konak öğeleri uygulama düzeyi projelere anlama  
 VSTO eklentisi projelerinde oluşturabileceğiniz bir <xref:Microsoft.Office.Tools.Word.Document> çalışma zamanında konak öğesi herhangi bir belgede Word'de açık. Kullanabileceğiniz <xref:Microsoft.Office.Tools.Word.Document> ilişkili belge için denetimler ekleme ya da kullanılabilir olan olayları işlemek için ana bilgisayar öğesi <xref:Microsoft.Office.Interop.Word.Document> nesneleri.  
  
 Oluşturulacak bir <xref:Microsoft.Office.Tools.Word.Document> konak öğesi, kullanım `GetVstoObject` yöntemi. Daha fazla bilgi için [genişletmek Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında VSTO Add-Ins](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)   
 [Genişletilmiş nesneleri kullanarak Word'ü otomatikleştirirken](../vsto/automating-word-by-using-extended-objects.md)   
 [Word nesne modeline genel bakış](../vsto/word-object-model-overview.md)   
 [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)   
 [Word belgelerini ve Excel çalışma kitaplarını VSTO eklentileri çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)  
  
  