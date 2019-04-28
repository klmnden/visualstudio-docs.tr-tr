---
title: 'Nasıl yapılır: Temel renk gölgelendiricisi oluşturma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c301328a-079a-49e8-b688-4749c01657c0
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f15bba37f5a03da934fae9ba4689da7775cfdb92
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62844880"
---
# <a name="how-to-create-a-basic-color-shader"></a>Nasıl yapılır: Temel renk gölgelendiricisi oluşturma

Bu makalede gölgelendirici Tasarımcısı ve yönlendirilmiş grafik gölgelendirici dili (DGSL) bir düz renk gölgelendiricisi oluşturma için nasıl kullanılacağını gösterir. Bu gölgelendirici için sabit bir RGB renk değeri son rengini ayarlar.

## <a name="create-a-flat-color-shader"></a>Düz renk gölgelendiricisi oluşturma

Son çıkış rengi bir RGB renk sabiti renk değerini yazarak düz renk gölgelendiricisi uygulayabilirsiniz.

Başlamadan önce emin **özellikleri** penceresi ve **araç kutusu** görüntülenir.

1. Çalışmak için bir DGSL gölgelendirici oluşturun. Projenize DGSL gölgelendirici ekleme hakkında daha fazla bilgi için bkz. Başlarken bölümünde [gölgelendirici Tasarımcısı](../designers/shader-designer.md).

2. Silme **nokta rengi** düğümü. Kullanım **seçin** seçme aracı **nokta rengi** düğümünü ve ardından menü çubuğunda, **Düzenle** > **Sil**.

3. Ekleme bir **renk sabit** grafiğe düğüm. İçinde **araç kutusu**altında **sabitleri**seçin **renk sabit** ve tasarım yüzeyine taşıyın.

4. Renk için bir değer belirtmeniz **renk sabit** düğümü. Kullanım **seçin** seçme aracı **Color sabit** düğümünü ve ardından **özellikleri** penceresi, **çıkış** özelliği belirtin bir renk değeri. Turuncu için (1.0, 0,5, 0.2, 1.0) değerini belirtin.

5. Renk sabiti için son rengini bağlanın. Bağlantılar oluşturmak için taşıma **RGB** , terminal **renk sabit** düğüme **RGB** , terminal **son rengini** düğümünü ve ettirin **alfa** , terminal **renk sabit** düğüme **alfa** , terminal **son rengini** düğümü. Bu bağlantılar, önceki adımda tanımlanan renk sabiti için son rengini ayarlayın.

Aşağıdaki resimde tamamlanmış gölgelendirici grafiği ve bir küpe uygulanan gölgelendiricinin önizlemesini gösterir.

> [!NOTE]
> Çizimde, daha iyi gölgelendirici etkisini göstermek için turuncu renk belirtildi.

![Gölgelendirici grafiği ve sonucu 3&#45;D modeli](../designers/media/digit-flat-color-effect.png)

Belirli şekiller daha iyi önizlemeleri için bazı gölgelendiricileri sağlayabilir. Gölgelendirici Tasarımcısı'nda gölgelendiricileri önizleme hakkında daha fazla bilgi için bkz: [gölgelendirici Tasarımcısı](../designers/shader-designer.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: 3B modele gölgelendirici uygulama](../designers/how-to-apply-a-shader-to-a-3-d-model.md)
- [Nasıl yapılır: Gölgelendiriciyi dışarı aktarma](../designers/how-to-export-a-shader.md)
- [Gölgelendirici Tasarımcısı](../designers/shader-designer.md)
- [Gölgelendirici Tasarımcısı düğümleri](../designers/shader-designer-nodes.md)