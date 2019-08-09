---
title: 'Nasıl yapılır: Temel Phong Gölgelendiricisi Oluşturma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c7c69da8-142b-4d3b-9be9-4be0d5970b25
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 895b797ad07018a9f4d4bf4c14b7f358a26f8eaa
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68924412"
---
# <a name="how-to-create-a-basic-phong-shader"></a>Nasıl yapılır: Temel Phong gölgelendiricisi oluşturma

Bu makalede, klasik Phong aydınlatma modelini uygulayan bir aydınlatma gölgelendiricisi oluşturmak için Gölgelendirici Tasarımcısının ve yönlendirilmiş Graf gölgelendirici dilinin (DGSL) nasıl kullanılacağı gösterilmektedir.

## <a name="the-phong-lighting-model"></a>Phong aydınlatma modeli

Phong aydınlatma modeli, bir yüzey 'nin yansıtıcı özelliklerini taklit eden yansımalı vurgulama 'i içerecek şekilde lambda Yansımalı bileşen Lambert aydınlatma modelinde kullanılan aynı yönlü ışık kaynaklarından ek aydınlatma sağlar, ancak nihai renge olan katkı farklı şekilde işlenir. Yansımalı vurgulama, Görünüm yönü, hafif kaynakların yönü ve yüzey yönü arasındaki ilişkiye bağlı olarak sahnenin her yüzeyi farklı şekilde etkiler. Bu, yüzeysel renk, yüzeysel güç, yüzey yönü ve açık kaynakların rengi, yoğunluğu ve yönü hakkında bir üründür. Açık kaynağı doğrudan görüntüleyicide yansıtan yüzeyler, görüntüleyicideki ışık kaynağını yansıtan maksimum yansımalı katkı ve yüzeyleri, hiçbir katkı almaz. Phong aydınlatma modelinde, bir veya daha fazla yansımalı bileşen, nesne üzerindeki her bir nokta için yansımalı Vurgulamanın rengini ve yoğunluğunu belirleyip, daha sonra pikselin son rengini oluşturmak için Lambert aydınlatma modelinin sonucuna eklenir .

Lambert aydınlatma modeli hakkında daha fazla bilgi için bkz [. nasıl yapılır: Temel Lambert gölgelendiricisi](../designers/how-to-create-a-basic-lambert-shader.md)oluşturun.

Başlamadan önce, **Özellikler** penceresinin ve **araç kutusunun** görüntülendiğinden emin olun.

1. Aşağıda açıklandığı [gibi bir Lambert gölgelendiricisi oluşturun: Temel Lambert gölgelendiricisi](../designers/how-to-create-a-basic-lambert-shader.md)oluşturun.

2. **Son renk** düğümünden **Lambert** düğümünün bağlantısını kesin. **Lambert** düğümünün **RGB** terminalini seçin ve ardından **Bağlantıları Kes**' i seçin. Bu, bir sonraki adımda eklenen düğüm için yer açar.

3. Grafiğe **ekleme** düğümü ekleyin. **Araç kutusunda**, **matematik**altında **Ekle** ' yi seçin ve tasarım yüzeyine taşıyın.

4. Grafiğe **Yansımalı** bir düğüm ekleyin. **Araç kutusu**' nda, **yardımcı program**altında **Yansımalı** ' ı seçin ve tasarım yüzeyine taşıyın.

5. Yansımalı katkı ekleyin. **Yansımalı** düğümün **Çıkış** terminalini **Add** düğümünün **X** terminaline taşıyın ve ardından **Lambert** düğümünün **Çıkış** terminalini **Add** düğümünün **Y** terminaline taşıyın. Bu bağlantılar piksel için toplam dağıtma ve yansımalı renk katkıları birleştirir.

6. Hesaplanan renk değerini son renge bağlayın. **Add** düğümünün **çıktı** terminalini **son renk** düğümünün **RGB** terminaline taşıyın.

   Aşağıdaki çizimde, tamamlanmış gölgelendirici grafiği ve bir ekip modeline uygulanan gölgelendirici önizlemesi gösterilmektedir.

> [!NOTE]
> Bu çizimde gölgelendirici etkisini daha iyi göstermek için, gölgelendiricinin **Materialdağıt** parametresi kullanılarak turuncu bir renk belirtilmiştir ve bu, bir metalik bakış ve **Materialspeculargüç** parametreleri. Malzeme parametreleri hakkında daha fazla bilgi için bkz. [gölgelendirici tasarımcısında](../designers/shader-designer.md)gölgelendiricilerin önizlemesi bölümü.

![Gölgelendirici Grafiği ve efektinin önizlemesi](../designers/media/digit-lighting-graph.png)

Bazı biçimler bazı gölgelendiriciler için daha iyi önizleme sağlayabilir. Gölgelendirici tasarımcısında gölgelendiriciler önizlemesi hakkında daha fazla bilgi için bkz. [gölgelendirici tasarımcısında](../designers/shader-designer.md) gölgelendiricilerin önizlemesi bölümü

Aşağıdaki çizimde, bu belgede bir 3B modele uygulanan gölgelendirici gösterilmektedir. **Materialspecsel** özelliği (1,00, 0,50, 0,20, 0,00) olarak ayarlanır ve **MaterialSpecularPower** özelliği 16 olarak ayarlanmıştır.

> [!NOTE]
> **Materialspecsel** özelliği, yüzey malzemelerinin görünen bitişini belirler. Cam veya plastik gibi yüksek parlak bir yüzey, parlak bir beyaz gölgeye sahip olan yansımalı bir renge sahiptir. Metalik bir yüzey, kendi dağıtma rengine yakın bir yansımalı renge sahip olacak şekilde eğilimi gösterir. Bir tam bitiş yüzeyi, koyu bir gri gölge olan yansımalı bir renge sahip olma eğilimi gösterir.
>
> **MaterialSpecularPower** özelliği, Yansımalı vurguların ne kadar kuvvetli olduğunu belirler. Yüksek yansımalı güçler, daha fazla yerelleştirilmiş vurguları taklit etmez. Çok düşük yansımalı güçler, tüm yüzeyin rengini açığa çıkaran ve gizlemek için yoğun ve keskin vurguları taklit edebilir.

![Bir modele uygulanan Phong aydınlatma](../designers/media/digit-lighting-model.png)

Bir 3B modele gölgelendirici uygulama hakkında daha fazla bilgi için bkz [. nasıl yapılır: 3B modele](../designers/how-to-apply-a-shader-to-a-3-d-model.md)gölgelendirici uygulayın.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: 3B modele gölgelendirici uygulama](../designers/how-to-apply-a-shader-to-a-3-d-model.md)
- [Nasıl yapılır: Gölgelendiriciyi dışarı aktarma](../designers/how-to-export-a-shader.md)
- [Nasıl yapılır: Temel Lambert gölgelendiricisi oluşturma](../designers/how-to-create-a-basic-lambert-shader.md)
- [Gölgelendirici Tasarımcısı](../designers/shader-designer.md)
- [Gölgelendirici Tasarımcısı düğümleri](../designers/shader-designer-nodes.md)