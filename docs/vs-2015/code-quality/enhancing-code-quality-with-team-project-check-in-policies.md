---
title: Takım projesi iade ilkeleri ile kod kalitesini arttırma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
helpviewer_keywords:
- code quality, using check-in policies
- team-based development, enhancing code quality
ms.assetid: 0ab72c33-148a-4a8a-a7bf-046995514c84
caps.latest.revision: 27
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 86aac26819e86455c8ab5c3676c8198bbb482e43
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65697191"
---
# <a name="enhancing-code-quality-with-team-project-check-in-policies"></a>Takım Projesi İade İlkeleriyle Kod Kalitesini Arttırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Team Foundation sürüm denetimi (TFVC) kullandığınızda, takım projeleriniz için iade ilkeleri oluşturabilirsiniz. zorlamak için daha iyi kod ve daha verimli Grup gelişimi yol açan uygulamalar. İade ilkeleri takım projesi düzeyinde ayarlanan ve kod iade edilmesine izin verilmesinden önce Geliştirici bilgisayarlarında mecburi olan kurallardır.  
  
 Bu takım projesi iade ilkeleri belirtebilirsiniz:  
  
- **Yapılar**: Bir derleme sırasında oluşturulan yapı aralarının bir yeni iadeden önce düzeltilmesi gereken gerektirir.  
  
- **Değişiklik kümesi açıklamalarını**: Kullanıcılar değişiklikler iade edilirken açıklama sağlamanızı gerektirir.  
  
- **Kod Analizi**: Kod Analizi iade önce çalışmasını gerektirir.  
  
- **İş öğelerini**: İş öğelerinin biri veya daha fazla onay-'ile ilişkili olmasını gerektirir.  
  
> [!IMPORTANT]
> İade ilkelerini kullanmak için bağlanmalıdır [!INCLUDE[vststfsLong](../includes/vststfslong-md.md)].  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Görev|Destekleyici İçerik|  
|----------|------------------------|  
|**Oluşturup iade ilkeleri kullanabilirsiniz:** Takım proje ayarlarını kullanarak iade ilkeleri oluşturma [!INCLUDE[esprscc](../includes/esprscc-md.md)].|[Ayarlama ve kalite kapıları](https://msdn.microsoft.com/library/bdc5666e-6cf0-45b2-a0a1-133c3f61e852)|  
|**Oluşturma ve kod çözümleme iade ilkeleri kullanın:** Kod çözümleme kuralların standart kümesinden seçebilir veya özel bir grup oluşturabilirsiniz.|[Kod Çözümleme İade İlkeleri Oluşturma ve Kullanma](../code-quality/creating-and-using-code-analysis-check-in-policies.md)|  
  
## <a name="related-tasks"></a>İlişkili görevler  
  
|Görev|Destekleyici İçerik|  
|----------|------------------------|  
|**Geliştirme ortamınızı ayarlayın:** Oluşturma veya kod değiştirme önce geliştirme sürecinizi ve uygun kaynak kodu kullanarak test ortamları. Veritabanları ile çalışıyorsanız, ayrıca veritabanlarının çevrimdışı gösterimine erişiminiz olmalıdır.|[Geliştirme ortamlarını ayarlama](https://msdn.microsoft.com/7b686610-d379-4ca0-9608-73ef0e576e3a)|  
|**Kod analizini, geliştirme sürecine kullanın:** Ekip üyeleri kendi geliştirme bilgisayarlarına kod analizini Çalıştır. Visual Studio'da geliştiriciler yapılandırmak ve bireysel kod projeleri için Kod Analizi yürütmeleri çalıştırın, görüntüleme ve sorunlarını analiz etmenize bulunan ve Uyarılar için iş öğeleri oluşturun.|[Uygulama Kalitesini Analiz Etme](../code-quality/analyzing-application-quality-by-using-code-analysis-tools.md)|  
|**Oluşturma ve birim testleri çalıştırma:** Birim testleri, sınıfların yöntemlerinde mantık hataları aramak için hızlı bir şekilde geliştiricilere ve test edicilere vermek C#, Visual Basic .NET ve C++ projeleri. Birim test bir kez oluşturulabilir ve kaynak kodun hiçbir hatanın emin emin olmak için değiştirildiği her seferde çalıştırın.|[Kodunuza Birim Testi Uygulama](../test/unit-test-your-code.md)|  
|**İş öğelerini ve kusurları izleyin:** İş öğeleri, takım projesi hakkındaki işleri ve bilgileri yönetmek ve izlemek için kullanabilirsiniz. Bir iş öğesi bir veritabanıdır bu kayıt [!INCLUDE[esprfound](../includes/esprfound-md.md)] atamasını ve çalışmanın ilerlemesini izlemek için kullanır. Farklı türlerde iş öğeleri, iş, müşteri gereksinimleri, ürün hataları ve geliştirme görevleri gibi farklı türlerde izlemek için kullanabilirsiniz.|[İş izleme ve iş akışını yönetme &#91;yönlendirildi&#93;](https://msdn.microsoft.com/d2d8637d-0ef8-4ca3-874e-a04713344032)|  
  
## <a name="external-resources"></a>Dış kaynaklar  
  
### <a name="guidance"></a>Kılavuz  
 [Visual Studio 2012 – bölüm 2 ile sürekli teslimat testi: Birim testi: İç testler](http://go.microsoft.com/fwlink/?LinkID=255188)
