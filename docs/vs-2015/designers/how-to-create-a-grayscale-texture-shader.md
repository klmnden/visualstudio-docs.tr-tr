---
title: 'Nasıl yapılır: Gri tonlamalı doku gölgelendiricisi oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: 79181d81-44af-445e-9a18-03483dd70260
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: e7d35347a4b656f9610097bc8dfe03e7c8488c01
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54779613"
---
# <a name="how-to-create-a-grayscale-texture-shader"></a>Nasıl yapılır: Gri tonlamalı doku gölgelendiricisi oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu belge, gölgelendirici Tasarımcısı ve yönlendirilmiş grafik gölgelendirici dili (DGSL) gri tonlamalı doku gölgelendiricisi oluşturmak için nasıl kullanılacağını gösterir. Bu gölgelendiriciyi RGB renk doku örneğinin değerini değiştirir ve ardından son rengini ayarlamak için birlikte değiştirilmemiş alfa değeri kullanır.  
  
## <a name="creating-a-grayscale-texture-shader"></a>Gri tonlamalı doku gölgelendiricisi oluşturma  
 Son Çıkış Rengi yazmadan önce bir doku örneğinin renk değeri değiştirerek bir gri tonlamalı doku gölgelendiricisi uygulayabilirsiniz.  
  
 Başlamadan önce emin **özellikleri** penceresi ve **araç kutusu** görüntülenir.  
  
#### <a name="to-create-a-grayscale-texture-shader"></a>Gri tonlamalı doku gölgelendiricisi oluşturma  
  
1. Bölümünde anlatıldığı gibi bir temel doku gölgelendiricisi oluşturma [nasıl yapılır: Temel doku gölgelendiricisi oluşturma](../designers/how-to-create-a-basic-texture-shader.md).  
  
2. Bağlantı kesme **RGB** , terminal **doku örneğinin** düğümünden **RGB** , terminal **son rengini** düğümü. İçinde **seçin** modunu seçin **RGB** , terminal **doku örneğinin** düğümünü seçip **Bağlantıları Kes**. Bu, sonraki adımda eklenen düğümü için yer sağlar.  
  
3. Ekleme bir **doygunluğunu azaltma** grafiğe düğüm. İçinde **araç kutusu**altında **filtreleri**seçin **doygunluğunu azaltma** ve tasarım yüzeyine taşıyın.  
  
4. Gri tonlamalı değeri hesaplamak **doygunluğunu azaltma** düğümü. İçinde **seçin** modu, taşıma **RGB** , terminal **doku örneğinin** düğüme **RGB** , terminal **Doygunluğu Azalt**  düğümü.  
  
   > [!NOTE]
   >  Varsayılan olarak, **doygunluğunu azaltma** düğümü tam olarak giriş rengi desaturates ve standart aydınlatma ağırlıkları gri tona dönüştürme için kullanır. Değiştirebileceğiniz nasıl **doygunluğunu azaltma** düğüm davranışını değerini değiştirerek **aydınlatma** özelliği veya yalnızca kısmen giriş rengi desaturating. Kısmen giriş Renk Doygunluğu Azalt için aralıktaki skaler bir değer belirtin [0,1) için **yüzde** , terminal **doygunluğunu azaltma** düğümü.  
  
5. Gri renk değeri son rengi bağlanın. Taşıma **çıkış** , terminal **doygunluğunu azaltma** düğüme **RGB** , terminal **son rengini** düğümü.  
  
   Aşağıdaki resimde tamamlanmış gölgelendirici grafiği ve bir küpe uygulanan gölgelendiricinin önizlemesini gösterir.  
  
> [!NOTE]
>  Bu çizimde, bir önizleme şeklinde kullanılır ve bir doku gölgelendirici etkisini daha iyi göstermek için belirtilen.  
  
 ![Gölgelendirici grafiği ve etkisini önizlemesini](../designers/media/digit-grayscale-effect.png "basamak gri tonlamalı etkisi")  
  
 Belirli şekiller daha iyi önizlemeleri için bazı gölgelendiricileri sağlayabilir. Gölgelendirici Tasarımcısı'nda gölgelendiricileri önizleme hakkında daha fazla bilgi için bkz. [gölgelendirici Tasarımcısı](../designers/shader-designer.md)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: 3B modele gölgelendirici uygulama](../designers/how-to-apply-a-shader-to-a-3-d-model.md)   
 [Nasıl yapılır: Gölgelendiriciyi dışarı aktarma](../designers/how-to-export-a-shader.md)   
 [Görüntü Düzenleyicisi](../designers/image-editor.md)   
 [Gölgelendirici Tasarımcısı](../designers/shader-designer.md)   
 [Gölgelendirici Tasarımcısı Düğümleri](../designers/shader-designer-nodes.md)
