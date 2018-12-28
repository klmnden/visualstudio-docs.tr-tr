---
title: Excel için belge düzeyi özelleştirmelerini programlama kullanmaya başlayın
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Excel solutions in Visual Studio
- Excel projects [Office development in Visual Studio], getting started
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 808b463445934ecf5cc973b571b4b64d181eb692
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53646951"
---
# <a name="get-started-programming-document-level-customizations-for-excel"></a>Excel için belge düzeyi özelleştirmelerini programlama kullanmaya başlayın
  Yeni Visual Studio kullanarak, Microsoft Office Excel için belge düzeyi özelleştirmeleri oluşturmaya başlıyor, işte bilmeniz gerekenler.  
  
 [!INCLUDE[appliesto_xlalldoc](../vsto/includes/appliesto-xlalldoc-md.md)]  
  
## <a name="understand-how-document-level-customizations-for-excel-work"></a>Excel çalışma için belge düzeyi özelleştirmeleri anlama  
 Excel için belge düzeyi özelleştirmeyi tek bir çalışma kitabı temel alır. Özelleştirme kullanmaya başlamak için son kullanıcı çalışma kitabını açar veya çalışma kitabını Excel şablonundan oluşturur. Örneğin hücrelerde yazarak ya da menü öğeleri ve düğmelere çalışma kitabında, olaylar, derlemede olay işleme yöntemleri çağırabilir. Çalışma kitabı kapalıyken özelleştirme tarafından sağlanan özellikleri artık bunları içeren belgesinde Excel'de kullanılabilir değildir.  
  
 Daha fazla bilgi için [belge düzeyi özelleştirmeler mimarisi](../vsto/architecture-of-document-level-customizations.md).  
  
## <a name="create-document-level-projects-for-excel"></a>Excel için belge düzeyi projeler oluşturma  
 Excel için belge düzeyi özelleştirmesinin için Excel çalışma kitabı veya Excel Şablonu proje şablonu kullanın. **yeni proje** iletişim kutusu. Bu şablonlar, gerekli bütünleştirilmiş kod başvuruları ve proje dosyaları içerir.  
  
 Excel için belge düzeyi projesi oluşturma hakkında daha fazla bilgi için bkz. [nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md). Proje şablonları hakkında daha fazla bilgi için bkz. [Office proje şablonlarına genel bakış](../vsto/office-project-templates-overview.md).  
  
## <a name="program-excel-workbooks-by-using-host-items-and-host-controls"></a>Konak denetimlerinin ve konak öğelerinin kullanarak Excel çalışma kitaplarını program  
 *Konak öğelerini* ve *konak denetimlerini* , Visual Studio kullanılarak oluşturulan belge düzeyi özelleştirmeleri için programlama modeli sağlar.  
  
 Konak öğeleri, kodunuz için giriş noktası sağlar ve bunlar da konak denetimleri ve Windows Forms denetimleri için kapsayıcılar olarak görev yapabilir. Excel için belge düzeyinde projelerde, bu konak öğeleri tarafından temsil edilen `ThisWorkbook`, `Sheet1`, `Sheet2`, ve `Sheet3` sınıfları.  
  
 Konak denetimleri listesi nesneleri ve aralıklar gibi yerel Excel nesneleri temel alır. Konak denetimleri için yerel Excel nesneleri için benzer bir işlevsellik sağlasa da, ayrıca yeni olaylar, tasarımcı desteği ve veri bağlama özelliği vardır. Proje kodunu ve Excel nesne modeline gitmek zorunda kalmadan doğrudan kodunuzdaki belirli nesnelere başvuru kolaylaştırması IntelliSense, birinci sınıf nesne olarak görünürler.  
  
 Daha fazla bilgi için aşağıdaki konulara bakın:  
  
-   [Belge düzeyi özelleştirmelerini programlama](../vsto/programming-document-level-customizations.md)  
  
-   [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)  
  
-   [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)  
  
## <a name="customize-the-user-interface-of-excel"></a>Excel kullanıcı arabirimini özelleştirme  
 Microsoft Office çözümlerinin çoğu, kullanıcıların çözümü ile etkileşim kurmak herhangi bir şekilde sağlamak için Office uygulamasının kullanıcı arabirimini (UI) değiştirin. Belge düzeyi özelleştirmesi kullanılarak Excel UI değiştirmeniz için birçok yol vardır. Örneğin, Şerit denetimleri ekleyebilirsiniz veya Eylemler bölmesinde görüntüleyebilirsiniz. Daha fazla bilgi için [Office UI özelleştirmesi](../vsto/office-ui-customization.md).  
  
 Doğrudan Visual Studio'da projenizle ilişkili çalışma kitabını da açabilirsiniz. Visual Studio'da çalışma kitabını açtığınızda, çalışma kitabını Excel kullanıcı arabirimini kullanarak değiştirebilirsiniz. Çalışma sayfasına denetimler sürükleyin olanak tanıyan bir tasarım yüzeyine olarak, çalışma kitabını da kullanabilirsiniz. Daha fazla bilgi için [Visual Studio ortamında Office projeleri](../vsto/office-projects-in-the-visual-studio-environment.md).  
  
## <a name="use-data-binding"></a>Veri bağlama kullanın  
 Konak denetimleri, sürükleyebilirsiniz denetim listesini de bulunan **veri kaynakları** penceresi. Konak denetimleri bu yolla ekleme penceresi kullanılarak ayarlanan veri kaynağına doğru bağlar. Herhangi bir kod yazmadan, veritabanları, web hizmetleri ve iş nesneleri verilerini görüntüleyebilirsiniz. Daha fazla bilgi için [Office çözümlerinde denetimlere veri bağlama](../vsto/binding-data-to-controls-in-office-solutions.md).  
  
## <a name="next-steps"></a>Sonraki adımlar  
 Excel için belge düzeyi özelleştirmesinin öğrenmek için bkz: [izlenecek yol: Excel için ilk belge düzeyi özelleştirmeyi oluşturma](../vsto/walkthrough-creating-your-first-document-level-customization-for-excel.md). Bu izlenecek yolda Office geliştirme araçlarını Visual Studio ve Excel belge düzeyi özelleştirmeleri için programlama modeli sunar.  
  
 Size bazı yaygın görevleri Excel projelerinde yol konuların listesi için bkz. [Office programlarındaki ortak görevler](../vsto/common-tasks-in-office-programming.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md)   
 [Belge düzeyi özelleştirmelerini programlama](../vsto/programming-document-level-customizations.md)   
 [Excel çözümleri](../vsto/excel-solutions.md)   
 [İzlenecek yol: Excel için ilk belge düzeyi özelleştirmeyi oluşturma](../vsto/walkthrough-creating-your-first-document-level-customization-for-excel.md)   
 [Excel kullanarak izlenecek yollar](../vsto/walkthroughs-using-excel.md)   
 [Excel nesne modeline genel bakış](../vsto/excel-object-model-overview.md)   
 [Office çözümlerinde kod yazma](../vsto/writing-code-in-office-solutions.md)  
  
  