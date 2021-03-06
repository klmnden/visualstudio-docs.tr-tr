---
title: Gölgelendiricilerle Çalışma
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 6b2ea1ed-b995-4e75-af19-c68fd37a3bc5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d1f07b293447a10a7d39e24ef42b1faedc27c7d6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62892409"
---
# <a name="work-with-shaders"></a>Gölgelendiricilerle çalışma

Visual Studio'da tasarım özel gölgelendirici efektleri için grafik tabanlı gölgelendirici Tasarımcısı'nı kullanabilirsiniz. Bu gölgelendiricileri DirectX tabanlı oyunlarda veya uygulamalarda de kullanabilirsiniz.

## <a name="shaders"></a>Gölgelendiriciler

A *gölgelendirici* grafik hesaplamalar yapan bir bilgisayar program — dönüşümleri köşe veya piksel renklendirme gibi — ve genellikle CPU yerine bir grafik işlem birimi (GPU) çalıştırır. Çoğu geleneksel, sabit işlevi grafik ardışık düzen aşamaları artık gölgelendirici programlar tarafından gerçekleştirildiğinden, uygulamanızın ihtiyaçlarına özel bir işlem hattı oluşturmak için kullanabilirsiniz.

Gölgelendiricileri en yaygın tür olan *köşe gölgelendiricileri*, köşe başına hesaplamalar ve sabit işlevi dönüştürme ve programlanabilir olmayan grafik donanımı aydınlatma devresi değiştirin ve *piksel gölgelendiricileri*, bir piksel rengi belirler ve sabit işlevi renk-Birleştirici devresi programlanabilir olmayan grafik donanımı değiştirme piksel başına hesaplamalar gerçekleştirin. Modern grafik donanımının vermiştir gölgelendiricileri daha da fazla tür mümkün —*Kabuk gölgelendirici*, *etki alanı gölgelendirici*, ve *geometri gölgelendirici* vegrafikhesaplamaları*gölgelendiricileri işlem* grafik olmayan hesaplamalar için. Bu aşamalar hiçbiri, programlanabilir olmayan grafik donanımının, hatta kullanılabilir değil. Gölgelendiricileri özgün veri-paralel (SIMD) ve grafik merkezli (nokta çarpımını) yönergeler sağlayan bir derleme benzeri bir dil kullanarak oluşturulur. Şimdi, gölgelendiriciler genellikle HLSL (yüksek düzey gölgelendirici dili) gibi üst düzey, C benzeri diller kullanılarak oluşturulur.

Piksel gölgelendiricileri etkileşimli olarak veya girme ve kod derleme oluşturmak için gölgelendirici Tasarımcısı'nı kullanabilirsiniz. Gölgelendirici Tasarımcısı'nda bir gölgelendirici verileri ve işlemleri ve veri değerlerini akışını temsil eden düğümler ve gölgelendirici aracılığıyla Ara sonuçlar arasında bağlantılar temsil eden bir düğüm sayısına göre tanımlanır. Bu yaklaşım ve gerçek zamanlı Önizleme gölgelendirici Tasarımcısı'nda kullanarak gölgelendirici yürütülmesini daha kolay görselleştirin ve "deneme aracılığıyla ilginç gölgelendirici çeşitlemeleri Bul".

## <a name="dgsl-documents"></a>DGSL belgeleri

Gölgelendirici Tasarımcısı gölgelendiricilerin, yönlendirilmiş grafik işaretleme dili (DGML üzerinde) dayalı olarak XML formatında yönlendirilmiş grafik gölgelendirici dili (DGSL) biçiminde kaydeder. 3B modeller Model Düzenleyicisi'nde için doğrudan DGSL gölgelendirici uygulayabilirsiniz. Uygulamanızda bir DGSL gölgelendirici kullanmadan önce ancak bunu DirectX anlayan bir biçime dışa aktarmanız gerekir — Örneğin, HLSL.

DGSL DGML ile uyumlu olmadığından, DGSL gölgelendirici çözümlemek için DGML belgelerinin analiz etmek için tasarlanan araçları kullanabilirsiniz. DGML hakkında daha fazla bilgi için bkz. [anlama yönlendirilmiş grafik işaretleme dili (DGML)](../modeling/customize-code-maps-by-editing-the-dgml-files.md).

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[Gölgelendirici Tasarımcısı](../designers/shader-designer.md)|Gölgelendiricilerle çalışmak için Visual Studio gölgelendirici Tasarımcısı kullanmayı açıklar.|
|[Gölgelendirici Tasarımcısı düğümleri](../designers/shader-designer-nodes.md)|Grafik efektler elde etmek için kullanabileceğiniz gölgelendirici Tasarımcısı düğümleri türlerini açıklar.|
|[Gölgelendirici Tasarımcısı örnekleri](../designers/shader-designer-examples.md)|Gölgelendirici Tasarımcısı ortak grafik efektler elde etmek için nasıl kullanılacağını gösteren konulara bağlantılar sağlar.|