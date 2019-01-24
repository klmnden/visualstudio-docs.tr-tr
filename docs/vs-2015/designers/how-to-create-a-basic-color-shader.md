---
title: 'Nasıl yapılır: Temel renk gölgelendiricisi oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: c301328a-079a-49e8-b688-4749c01657c0
caps.latest.revision: 26
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: b1e202f84fb3b4e0e865e2cebb96b6728289ff6b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54774120"
---
# <a name="how-to-create-a-basic-color-shader"></a>Nasıl yapılır: Temel renk gölgelendiricisi oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu belge gölgelendirici Tasarımcısı ve yönlendirilmiş grafik gölgelendirici dili (DGSL) bir düz renk gölgelendiricisi oluşturma için nasıl kullanılacağını gösterir. Bu gölgelendirici için sabit bir RGB renk değeri son rengini ayarlar.  
  
 Bu belgede şu faaliyetler gösterilmiştir:  
  
-   Bir grafikten düğümleri kaldırma  
  
-   Grafiğe düğüm ekleme  
  
-   Düğüm özelliklerini ayarlama  
  
-   Düğümleri bağlanma  
  
## <a name="creating-a-flat-color-shader"></a>Düz renk gölgelendiricisi oluşturma  
 Son çıkış rengi bir RGB renk sabiti renk değerini yazarak düz renk gölgelendiricisi uygulayabilirsiniz.  
  
 Başlamadan önce emin **özellikleri** penceresi ve **araç kutusu** görüntülenir.  
  
#### <a name="to-create-a-flat-color-shader"></a>Düz renk gölgelendiricisi oluşturma  
  
1. Çalışmak için bir DGSL gölgelendirici oluşturun. Projenize DGSL gölgelendirici ekleme hakkında daha fazla bilgi için bkz. Başlarken bölümünde [gölgelendirici Tasarımcısı](../designers/shader-designer.md).  
  
2. Silme **nokta rengi** düğümü. Kullanım **seçin** seçme aracı **nokta rengi** düğümünü ve ardından menü çubuğunda, **Düzenle**, **Sil**.  
  
3. Ekleme bir **renk sabit** grafiğe düğüm. İçinde **araç kutusu**altında **sabitleri**seçin **renk sabit** ve tasarım yüzeyine taşıyın.  
  
4. Renk için bir değer belirtmeniz **renk sabit** düğümü. Kullanım **seçin** seçme aracı **Color sabit** düğümünü ve ardından **özellikleri** penceresi, **çıkış** özelliği belirtin bir renk değeri. Turuncu için (1.0, 0,5, 0.2, 1.0) değerini belirtin.  
  
5. Renk sabiti için son rengini bağlanın. Bağlantılar oluşturmak için taşıma **RGB** , terminal **renk sabit** düğüme **RGB** , terminal **son rengini** düğümünü ve ettirin **alfa** , terminal **renk sabit** düğüme **alfa** , terminal **son rengini** düğümü. Bu bağlantılar, önceki adımda tanımlanan renk sabiti için son rengini ayarlayın.  
  
   Aşağıdaki resimde tamamlanmış gölgelendirici grafiği ve bir küpe uygulanan gölgelendiricinin önizlemesini gösterir.  
  
> [!NOTE]
>  Çizimde, daha iyi gölgelendirici etkisini göstermek için turuncu renk belirtildi.  
  
 ![Gölgelendirici grafiği ve sonucu 3&#45;D modeli](../designers/media/digit-flat-color-effect.png "basamak düz renk etkisi")  
  
 Belirli şekiller daha iyi önizlemeleri için bazı gölgelendiricileri sağlayabilir. Gölgelendirici Tasarımcısı'nda gölgelendiricileri önizleme hakkında daha fazla bilgi için bkz: [gölgelendirici Tasarımcısı](../designers/shader-designer.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: 3B modele gölgelendirici uygulama](../designers/how-to-apply-a-shader-to-a-3-d-model.md)   
 [Nasıl yapılır: Gölgelendiriciyi dışarı aktarma](../designers/how-to-export-a-shader.md)   
 [Gölgelendirici Tasarımcısı](../designers/shader-designer.md)   
 [Gölgelendirici Tasarımcısı Düğümleri](../designers/shader-designer-nodes.md)
