---
title: Gölgelendiricilerle çalışma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: 6b2ea1ed-b995-4e75-af19-c68fd37a3bc5
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: b912708e7cc2f811e9cd18a24096ef66e128c375
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65690063"
---
# <a name="working-with-shaders"></a>Gölgelendiricilerle Çalışma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Grafik tabanlı gölgelendirici Tasarımcısı'nda kullanabileceğiniz [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] tasarım özel gölgelendirici efektleri için. Bu gölgelendiricileri DirectX tabanlı oyunlarda veya uygulamalarda de kullanabilirsiniz.  
  
## <a name="shaders"></a>Gölgelendiriciler  
 A *gölgelendirici* grafik hesaplamalar yapan bir bilgisayar program — dönüşümleri köşe veya piksel renklendirme gibi — ve genellikle CPU yerine bir grafik işlem birimi (GPU) çalıştırır. Çoğu geleneksel, sabit işlevi grafik ardışık düzen aşamaları artık gölgelendirici programlar tarafından gerçekleştirildiğinden, uygulamanızın ihtiyaçlarına özel bir işlem hattı oluşturmak için kullanabilirsiniz.  
  
 Gölgelendiricileri en yaygın tür olan *köşe gölgelendiricileri*, köşe başına hesaplamalar ve sabit işlevi dönüştürme ve programlanabilir olmayan grafik donanımı aydınlatma devresi değiştirin ve *piksel gölgelendiricileri*, bir piksel rengi belirler ve sabit işlevi renk-Birleştirici devresi programlanabilir olmayan grafik donanımı değiştirme piksel başına hesaplamalar gerçekleştirin. Modern grafik donanımının vermiştir gölgelendiricileri daha da fazla tür mümkün —*Kabuk gölgelendirici*, *etki alanı gölgelendirici*, ve *geometri gölgelendirici* vegrafikhesaplamaları*gölgelendiricileri işlem* grafik olmayan hesaplamalar için. Bu aşamalar hiçbiri, programlanabilir olmayan grafik donanımının, hatta kullanılabilir değil. Gölgelendiricileri özgün veri-paralel (SIMD) ve grafik merkezli (nokta çarpımını) yönergeler sağlayan bir derleme benzeri bir dil kullanarak oluşturulur. Şimdi, gölgelendiriciler genellikle HLSL (yüksek düzey gölgelendirici dili) gibi üst düzey, C benzeri diller kullanılarak oluşturulur.  
  
 Piksel gölgelendiricileri etkileşimli olarak veya girme ve kod derleme oluşturmak için gölgelendirici Tasarımcısı'nı kullanabilirsiniz. Gölgelendirici Tasarımcısı'nda bir gölgelendirici verileri ve işlemleri ve veri değerlerini akışını temsil eden düğümler ve gölgelendirici aracılığıyla Ara sonuçlar arasında bağlantılar temsil eden bir düğüm sayısına göre tanımlanır. Bu yaklaşım ve gerçek zamanlı Önizleme gölgelendirici Tasarımcısı'nda kullanarak gölgelendirici yürütülmesini daha kolay görselleştirin ve "deneme aracılığıyla ilginç gölgelendirici çeşitlemeleri Bul".  
  
## <a name="dgsl-documents"></a>DGSL belgeleri  
 Gölgelendirici Tasarımcısı gölgelendiricilerin, yönlendirilmiş grafik işaretleme dili (DGML üzerinde) dayalı olarak XML formatında yönlendirilmiş grafik gölgelendirici dili (DGSL) biçiminde kaydeder. 3B modeller Model Düzenleyicisi'nde için doğrudan DGSL gölgelendirici uygulayabilirsiniz. Uygulamanızda bir DGSL gölgelendirici kullanmadan önce ancak bunu DirectX anlayan bir biçime dışa aktarmanız gerekir — Örneğin, HLSL.  
  
 DGSL DGML ile uyumlu olmadığından, DGSL gölgelendirici çözümlemek için DGML belgelerinin analiz etmek için tasarlanan araçları kullanabilirsiniz. DGML hakkında daha fazla bilgi için bkz. [anlama yönlendirilmiş grafik işaretleme dili (DGML)](https://msdn.microsoft.com/library/ee842619.aspx).  
  
## <a name="related-topics"></a>İlgili konular  
  
|Başlık|Açıklama|  
|-----------|-----------------|  
|[Gölgelendirici Tasarımcısı](../designers/shader-designer.md)|Nasıl kullanılacağını açıklar [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] gölgelendiricilerle çalışmak için gölgelendirici Tasarımcısı.|  
|[Gölgelendirici Tasarımcısı Düğümleri](../designers/shader-designer-nodes.md)|Grafik efektler elde etmek için kullanabileceğiniz gölgelendirici Tasarımcısı düğümleri türlerini açıklar.|  
|[Gölgelendirici Tasarımcısı Örnekleri](../designers/shader-designer-examples.md)|Gölgelendirici Tasarımcısı ortak grafik efektler elde etmek için nasıl kullanılacağını gösteren konulara bağlantılar sağlar.|
