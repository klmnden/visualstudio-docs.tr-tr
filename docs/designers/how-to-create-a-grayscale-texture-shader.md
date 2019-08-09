---
title: 'Nasıl yapılır: Gri Tonlamalı Doku Gölgelendiricisi Oluşturma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 79181d81-44af-445e-9a18-03483dd70260
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4a8e0295864986ad5cfae2f304f5b0f802f2fb12
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68924313"
---
# <a name="how-to-create-a-grayscale-texture-shader"></a>Nasıl yapılır: Gri tonlamalı doku gölgelendiricisi oluşturma

Bu makalede, bir gri tonlamalı doku gölgelendiricisi oluşturmak için Gölgelendirici Tasarımcısının ve yönlendirilmiş Graf gölgelendirici dilinin (DGSL) nasıl kullanılacağı gösterilmektedir. Bu gölgelendirici, doku örneğinin RGB renk değerini değiştirir ve ardından son rengi ayarlamak için onu değiştirilmemiş Alfa değeriyle birlikte kullanır.

## <a name="create-a-grayscale-texture-shader"></a>Gri tonlamalı doku gölgelendiricisi oluşturma

Son çıkış rengine yazmadan önce bir doku örneğinin renk değerini değiştirerek bir gri tonlamalı doku gölgelendiricisi uygulayabilirsiniz.

Başlamadan önce, **Özellikler** penceresinin ve **araç kutusunun** görüntülendiğinden emin olun.

1. Temel doku gölgelendiricisi oluşturma bölümünde [açıklandığı gibi: Temel doku gölgelendiricisi](../designers/how-to-create-a-basic-texture-shader.md)oluşturun.

2. **Doku örneği** düğümünün **RGB** terminalinin, **son renk** düğümünün **RGB** terminalden bağlantısını kesin. **Seç** modunda, **doku örnek** düğümünün **RGB** terminalini seçin ve ardından **Bağlantıları Kes**' i seçin. Bu, bir sonraki adımda eklenen düğüm için yer açar.

3. Grafiğe gri bir düğüm ekleyin. **Araç kutusunda**, **Filtreler**altında, doygunluğu Kaldır ' ı seçin ve tasarım yüzeyine taşıyın.

4. Gri tonlamalı değeri, doygunluğu Azalt düğümünü kullanarak hesaplayın. **Seç** modunda, **doku örnek** düğümünün **RGB** terminalini gri olan düğümün **RGB** terminaline taşıyın.

    > [!NOTE]
    > Varsayılan olarak, doygunluğu azalt düğümü, giriş rengini tamamen kaldırır ve gri tona dönüştürme dönüştürmesi için standart ışıklılık ağırlıklarını kullanır. **Işıklılık** özelliğinin değerini değiştirerek veya giriş renginin yalnızca kısmen doygunluğu yaparak, doygunluğu kaplama düğümünün nasıl davranacağını değiştirebilirsiniz. Giriş renginin kısmen borçlandırçıkarılması için, [0, 1) aralığında, doygunluğu Azalt düğümünün **yüzde** terminaline bir skaler değer sağlayın.

5. Gri tonlamalı renk değerini son renge bağlayın. **Yarım gri** düğümün **Çıkış** terminalini **son renk** düğümünün **RGB** terminaline taşıyın.

Aşağıdaki çizimde, tamamlanmış gölgelendirici grafiği ve bir küpe uygulanan gölgelendirici önizlemesi gösterilmektedir.

> [!NOTE]
> Bu çizimde, önizleme şekli olarak bir düzlem kullanılır ve gölgelendirici efektini daha iyi göstermek için bir doku belirtilmiştir.

![Gölgelendirici Grafiği ve efektinin önizlemesi](../designers/media/digit-grayscale-effect.png)

Bazı biçimler bazı gölgelendiriciler için daha iyi önizleme sağlayabilir. Gölgelendirici tasarımcısında gölgelendiricilerin önizlemesi hakkında daha fazla bilgi için bkz. [Gölgelendirici Tasarımcısı](../designers/shader-designer.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: 3B modele gölgelendirici uygulama](../designers/how-to-apply-a-shader-to-a-3-d-model.md)
- [Nasıl yapılır: Gölgelendiriciyi dışarı aktarma](../designers/how-to-export-a-shader.md)
- [Görüntü Düzenleyicisi](../designers/image-editor.md)
- [Gölgelendirici Tasarımcısı](../designers/shader-designer.md)
- [Gölgelendirici Tasarımcısı düğümleri](../designers/shader-designer-nodes.md)