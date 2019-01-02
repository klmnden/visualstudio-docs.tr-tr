---
title: Word için belge düzeyi özelleştirmelerini programlama kullanmaya başlayın
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Word solutions in Visual Studio
- Word projects [Office development in Visual Studio], getting started
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 651208958b40ff92804b9989234f8c3822ec83d9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53904805"
---
# <a name="get-started-programming-document-level-customizations-for-word"></a>Word için belge düzeyi özelleştirmelerini programlama kullanmaya başlayın
  Yeni Visual Studio kullanarak, Microsoft Office Word için belge düzeyi özelleştirmeleri oluşturmaya başlıyor, işte bilmeniz gerekenler.  
  
 [!INCLUDE[appliesto_wdalldoc](../vsto/includes/appliesto-wdalldoc-md.md)]  
  
## <a name="understand-how-document-level-customizations-for-word-work"></a>Word iş için belge düzeyi özelleştirmeleri anlama  
 Oluşturduğunuz her sözcük özelleştirme, tek bir belge çevresinde temel alır. Özelleştirme kullanmaya başlamak için son kullanıcı belge açılır veya Word şablondan belgesi oluşturur. Belgede, örneğin belirli alanlara imleci taşıma veya düğmeler ve menü öğeleri, olaylar, derlemede olay işleme yöntemleri çağırabilir. Word özelleştirme tarafından sağlanan özellikleri artık belge kapatıldığında kullanılamaz.  
  
 Daha fazla bilgi için [belge düzeyi özelleştirmeler mimarisi](../vsto/architecture-of-document-level-customizations.md).  
  
## <a name="create-document-level-projects-for-word"></a>Word için belge düzeyi projeler oluşturma  
 Word için belge düzeyi özelleştirmesinin için Word belgesi veya Word Şablonu proje şablonu kullanın. **yeni proje** iletişim kutusu. Bu şablonlar, gerekli bütünleştirilmiş kod başvuruları ve proje dosyaları içerir.  
  
 Word için belge düzeyi projesi oluşturma hakkında daha fazla bilgi için bkz. [nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md). Proje şablonları hakkında daha fazla bilgi için bkz. [Office proje şablonlarına genel bakış](../vsto/office-project-templates-overview.md).  
  
## <a name="program-word-documents-by-using-host-items-host-controls"></a>Konak öğeleri kullanarak Word belgelerine program denetimleri barındırma  
 *Konak öğelerini* ve *konak denetimlerini* için belge düzeyi özelleştirmelerini programlama modeli sağlayan sınıflar.  
  
 Konak öğeleri, kodunuz için giriş noktası sağlar ve bunlar da konak denetimleri ve Windows Forms denetimleri için kapsayıcılar olarak görev yapabilir. Word için belge düzeyinde projelerde konak öğesi tarafından temsil edilen `ThisDocument` sınıfı.  
  
 Konak denetimleri içerik denetimleri, yer işaretleri ve XML düğümüyle gibi yerel Word nesneleri temel alır. Konak denetimleri için yerel Word nesneleri için benzer bir işlevsellik sağlasa da, aynı zamanda yeni olaylar, tasarımcı desteği ve veri bağlama özelliği vardır. Proje kodunu ve Word nesne modeline gitmek zorunda kalmadan doğrudan kodunuzdaki belirli nesnelere başvuru kolaylaştırması IntelliSense, birinci sınıf nesne olarak görünürler.  
  
 Daha fazla bilgi için aşağıdaki konulara bakın:  
  
-   [Belge düzeyi özelleştirmelerini programlama](../vsto/programming-document-level-customizations.md)  
  
-   [Genişletilmiş nesneleri kullanarak Word'ü otomatikleştirirken](../vsto/automating-word-by-using-extended-objects.md)  
  
-   [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)  
  
## <a name="customize-the-user-interface-of-word"></a>Word kullanıcı arayüzünü özelleştirme  
 Microsoft Office çözümlerinin çoğu, kullanıcıların çözümü ile etkileşim kurmak herhangi bir şekilde sağlamak için Office uygulamasının kullanıcı arabirimini (UI) değiştirin. Belge düzeyi özelleştirmesi kullanılarak UI Word'ün değiştirmeniz için birçok yol vardır. Örneğin, Şerit denetimleri ekleyebilirsiniz ve Eylemler bölmesinde görüntüleyebilirsiniz. Daha fazla bilgi için [Office UI özelleştirmesi](../vsto/office-ui-customization.md).  
  
 Doğrudan Visual Studio'da projenizle ilişkili belgeyi da açabilirsiniz. Belge Visual Studio'da açıldığında belgenin Word kullanıcı arabirimini kullanarak değiştirebilirsiniz. Belge, denetimler sürükleyin olanak tanıyan bir tasarım yüzeyine olarak da kullanabilirsiniz. Daha fazla bilgi için [Visual Studio ortamında Office projeleri](../vsto/office-projects-in-the-visual-studio-environment.md).  
  
## <a name="bind-controls-to-data"></a>Verilere denetimler bağlama  
 İçerik denetimleri ve <xref:Microsoft.Office.Tools.Word.Bookmark> denetimi olan'ndan sürükleyebilirsiniz denetimleri listesinde **veri kaynakları** penceresi. İçerik denetimleri ve bu şekilde otomatik olarak yer imlerini ekleme penceresini kullanarak ayarladığınız veri kaynağına doğru bağlar. Herhangi bir kod yazmadan, veritabanları, hizmetleri ve iş nesneleri verilerini görüntüleyebilirsiniz. Daha fazla bilgi için [Office çözümlerinde denetimlere veri bağlama](../vsto/binding-data-to-controls-in-office-solutions.md).  
  
## <a name="next-steps"></a>Sonraki adımlar  
 Word için belge düzeyi özelleştirmesinin öğrenmek için bkz: [izlenecek yol: Word için ilk belge düzeyi özelleştirmeyi oluşturma](../vsto/walkthrough-creating-your-first-document-level-customization-for-word.md). Bu izlenecek yolda Office geliştirme araçlarını Visual Studio ve Word belge düzeyi özelleştirmeleri için programlama modeli sunar.  
  
 Size bazı yaygın görevleri Word projelerinde yol konuların listesi için bkz. [Office programlarındaki ortak görevler](../vsto/common-tasks-in-office-programming.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md)   
 [Belge düzeyi özelleştirmelerini programlama](../vsto/programming-document-level-customizations.md)   
 [Word çözümleri](../vsto/word-solutions.md)   
 [İzlenecek yol: Word için ilk belge düzeyi özelleştirmeyi oluşturma](../vsto/walkthrough-creating-your-first-document-level-customization-for-word.md)   
 [Word'ü kullanarak izlenecek yollar](../vsto/walkthroughs-using-word.md)   
 [Word nesne modeline genel bakış](../vsto/word-object-model-overview.md)   
 [Office çözümlerinde kod yazma](../vsto/writing-code-in-office-solutions.md)  
