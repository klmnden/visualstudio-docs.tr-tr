---
title: 'Nasıl yapılır: Çarpımlı alfa kullanan doku dışa aktarma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 05348afa-f079-4f53-a05b-ecd91d13adab
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 64c336db07eab794a6595cb2de9026c1269a33c4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62893394"
---
# <a name="how-to-export-a-texture-that-has-premultiplied-alpha"></a>Nasıl yapılır: Ön çarpımlı alfa kullanan dokuyu dışarı aktarma

Görüntü içeriği ardışık düzeni bir kaynak görüntüden önceden çoğaltılmış alfa dokular oluşturabilir. Bunlar, kullanımı daha basit ve daha sağlamdır ön çarpımlı alfa içermeyen dokular olabilir.

Bu belgede şu faaliyetler gösterilmiştir:

- Görüntü içeriği ardışık düzeni tarafından işlenecek kaynak görüntüyü yapılandırma.

- Ön çarpımlı alfa oluşturmak için görüntü içeriği ardışık yapılandırma.

## <a name="premultiplied-alpha"></a>Ön çarpımlı alfa
 Ön çarpımlı alfa, texel'ın renk katkısı ayırarak daha iyi fiziksel malzemelerle ışığın gerçek etkileşimi temsil ettiğinden alfa, Geleneksel, önceden çoğaltılmamış Alfaya kıyasla çeşitli avantajlar sunar (ekler rengi Sahne) kendi saydamlığından (izin verdiği temel rengin miktarını). Önceden çoğaltılmış alfa kullanmanın avantajlarından bazıları şunlardır:

- Ön çarpımlı alfa karıştırma ilişkilendirilebilir bir işlemdir; birden çok saydam Dokuların karıştırılması sonucu, hangi dokular karışık sıra bağımsız olarak aynıdır.

- Ön çarpımlı alfa karıştırmanın ilişkilendirilebilir yapısı nedeniyle saydam nesnelerin çoklu geçiş işlemesi basitleştirilir.

- Ön çarpımlı alfa kullanarak hem saf artırıcı (alfayı sıfıra ayarlayarak tarafından) karıştırma hem de doğrusal Ara değerli karıştırma aynı anda elde edilebilir. Örneğin, bir sistemde harmanlanan bir Ateş partikülü doğrusal enterpolasyon kullanılarak harmanlanan bir yarı saydam Duman partikülü olabilir. Önceden çoğaltılmış alfa olmadan, Ateş parçacıklarını Duman parçacıklarından ayrı olarak çizme ve çizim çağrıları arasında işleme durumunu değiştirmek gerekir.

- Ön çarpımlı alfa kullanan doku sıkıştırma Eşleşmeyenleri daha yüksek kaliteli ve rengi kenarları göstermesi yoksa — veya "halo etkisi" — önceden çoğaltılmış alfa kullanmayan dokuları karıştırdığınızda neden olur.

#### <a name="to-create-a-texture-that-uses-premultiplied-alpha"></a>Ön çarpımlı alfa kullanan doku oluşturma

1. Temel doku ile başlayın. Varolan bir resim dosyasını yükleyin ya da açıklandığı gibi oluşturmak [nasıl yapılır: Temel doku oluşturma](../designers/how-to-create-a-basic-texture.md).

2. Doku dosyasını yapılandırarak, böylece görüntü içeriği ardışık düzeni tarafından işlenir. İçinde **Çözüm Gezgini**, doku dosyası için kısayol menüsünü açın ve ardından **özellikleri**. Üzerinde **yapılandırma özellikleri** > **genel** sayfasında **öğesi türü** özelliğini **görüntü içeriği ardışık düzeni**. Emin olun **içerik** özelliği **Evet** ve **yapıdan hariç tut** ayarlanır **Hayır**ve ardından  **Uygulama** düğmesi. **Görüntü içeriği ardışık düzeni** yapılandırma özellik sayfası görüntülenir.

3. Ön çarpımlı alfa oluşturmak için görüntü içeriği ardışık yapılandırın. Üzerinde **yapılandırma özellikleri** > **görüntü içeriği ardışık düzeni** > **genel** sayfasında **Dönüştür Ön çarpımlı alfa biçimine** özelliğini **Evet (/ generatepremultipliedalpha)**.

4. Seçin **Tamam** düğmesi.

   Proje oluşturduğunuzda, görüntü içeriği ardışık düzeni kaynak görüntüyü çalışma biçiminden sizin belirttiğiniz çıkış biçimine dönüştürür — bu görüntünün önceden çoğaltılmış alfa biçimine dönüştürülmesi içerir — ve sonuç projenin çıkış için kopyalanır. Dizin.