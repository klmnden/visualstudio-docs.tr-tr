---
title: Blend'de nesnlerin stilini değiştirme
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1b9cd7e785b1c4ffa8613b6f5440a33b99dd2de6
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55955316"
---
# <a name="modify-the-style-of-objects-in-blend"></a>Blend'de nesnlerin stilini değiştirme

Özellikleri ayarlamak için bir nesne özelleştirmek için en kolay yolu olan **özellikleri** bölmesi.

Ayarları yeniden kullanmak veya ayar gruplarını istiyorsanız, yeniden kullanılabilir bir kaynak oluşturun. Bunun bir *stili*, *şablon*, ya da özel bir renk gibi basit bir şeyden. Ayrıca, bir denetim üzerinde durumuna göre farklı şekilde görünür yapabilirsiniz. Örneğin, kullanıcı tıkladığında bir düğme yeşile döner.

## <a name="brushes-modify-the-appearance-of-an-object"></a>Fırçalar: Bir nesnenin görünümünü değiştirme

Görünümünü değiştirmek istiyorsanız bir fırça bir nesneye uygulayın.

### <a name="paint-a-repeating-image-or-pattern-on-an-object"></a>Yinelenen bir görüntü veya bir nesne üzerinde deseni boyama

Yinelenen bir görüntü veya bir nesne üzerinde deseni kullanılarak boyama bir *döşeme Fırçası*.

Döşeme Fırçası oluşturmak için oluşturarak başlayın bir *resim fırçası*, *çizim Fırçası*, veya *görsel fırça* kaynak.

Resim fırçası bir görüntü kullanarak oluşturun. Aşağıdaki çizimler resim fırçası ve döşemeli resim fırçası çevrilmiş resim fırçası göstermektedir.

![Resim fırçası](../designers/media/81f84f56-906d-456b-8288-d77da1e01e31.png) ![döşeli mage fırça](../designers/media/d3782ca8-64da-47a4-a095-c6cdd0fa47a2.png) ![Çevrilmiş resim fırçası](../designers/media/38ae3691-f3f1-4a1e-82ca-c7fa164bf56e.png)

Çizim Fırçası bir vektör bir yol veya şekil gibi çizim kullanarak oluşturun. Aşağıdaki çizimler çizim Fırçası ve döşemeli çizim Fırçası çevrilmiş çizim Fırçası göstermektedir.

![Çizim Fırçası](../designers/media/197666ac-ef57-4c5c-9779-669e991a00a5.png) ![Çizme döşeli fırça](../designers/media/ba09cda3-4cee-40ba-b3d4-edc032158bdc.png) ![Çizim Fırçası çevrilmiş](../designers/media/15bf6021-620c-4490-9eae-086153d3f14f.png)

Görsel bir fırçayı bir düğme gibi bir denetim oluşturun. Aşağıdaki çizimler görsel fırça ve döşemeli görsel fırça göstermektedir.

![Görsel fırça](../designers/media/fb6c90e0-153c-48fe-b563-e601beac6227.png) ![Döşeli görsel fırça](../designers/media/e261b99f-7d8f-4d91-bc84-19c7beccc255.png)

## <a name="styles-and-templates-create-a-consistent-look-and-feel-across-controls"></a>Stilleri ve şablonları: Denetimler arasında tutarlı bir görünüm oluşturma

Görünümünü ve davranışını bir kez tasarlayabilir ve ayrı ayrı tutmak zorunda kalmazsınız, tasarım diğer denetimlere uygulanır.

**Bir stil kullanmalısınız?** : (Örneğin, bir düğme rengi) varsayılan özellikleri ayarlamak istiyorsanız kullanmak bir *stil*. Bile sizin için bir stil uygulamış olduğunuz sonra bir denetim değiştirebilirsiniz.

**Bir şablonu kullanmalısınız?** : Bir denetimin yapısını değiştirmek istiyorsanız, kullanmak bir *şablon*. Bir grafik veya logosu, bir düğmeye dönüştürme olduğunu düşünün. Bir şablon uyguladığınız sonra bir denetim değiştiremezsiniz.

### <a name="create-a-template-or-style"></a>Bir şablon veya stil oluşturma

Bir şablon oluşturmanın iki yolu demektir. Çalışma yüzeyindeki bir denetime herhangi bir nesneye dönüştürebilir veya varolan bir denetimi şablonunuzu temel alabilir.

Herhangi bir nesne için bir denetim şablonu dönüştürmek için nesneyi seçin ve ardından **Araçları** menüsünde seçin **denetim haline Dönüştür**.

Varolan bir denetimi, şablona istiyorsanız, çalışma yüzeyinde bir nesneyi seçin. Ardından, çalışma yüzeyinin üst kısmında içerik haritası düğmeyi seçin, **şablonu Düzen**ve ardından **kopya Düzenle** veya **oluşturma boş**.

![Düzen şablonu menüsü](../designers/media/5ebdb33f-aad2-4c10-a328-5e8b04c56a36.png)

Stil oluşturma, nesneyi seçin ve ardından **nesne** menüsünde seçin **stili Düzenle**ve ardından **kopya Düzenle** veya **boş oluşturma**.

- Seçin **kopya Düzenle** varsayılan stil veya şablon denetimi ile başlatmak için.

- Seçin **oluşturma boş** sıfırdan başlatmak için.

**Geçerli olanı Düzenle** seçeneği, yalnızca bir stil veya önceden oluşturduğunuz bir şablonu düzenlerseniz görüntülenir. Bir denetim için varsayılan sistem şablonunu yine de kullandığı görünmeyecektir.

İçinde **stil kaynağı oluştur** iletişim kutusu, ya da adını stil veya şablon daha sonra kullanabileceğiniz ya da bu türdeki tüm denetimlere stili veya şablonu uygulayabilirsiniz.

![Stil kaynağı iletişim kutusu oluşturma](../designers/media/4818ee6a-ce60-4b79-91c8-3b1871829eea.png)

> [!NOTE]
> Stilleri veya şablonları her denetim türü için oluşturulamıyor. Bir denetim onları desteklemiyorsa, içerik haritası düğmesi çalışma yüzeyi üzerinde görünmez.
> Ana belgenizin düzenleme kapsamına dönmek için tıklayın **kapsamına dönmek** ![kapsam simgesini döndürür](../designers/media/55844eb3-ed98-4f20-aa66-a6f5b23eeb2b.png).

### <a name="apply-a-style-or-template-to-a-control"></a>Bir denetime stil veya şablon uygulama

Bir nesneye sağ [nesneler ve zaman çizelgesi](../designers/creating-a-ui-by-using-blend-for-visual-studio.md#tour-of-the-objects-and-timeline-panel) panelinde öğesini **şablonu Düzen**ve ardından **kaynağı Uygula**.

![Kaynak menüsünde Uygula](../designers/media/dc12debc-7711-47d9-84ce-10322a384397.png)

### <a name="restore-the-default-style-or-template-of-a-control"></a>Varsayılan stil veya şablon denetiminin geri yükleme

İstediğiniz denetimi seçin ve [özellikleri](../designers/creating-a-ui-by-using-blend-for-visual-studio.md#tour-of-the-properties-panel) paneli, bulun **stili** veya **şablon** özelliği. Seçin **Gelişmiş Seçenekler**ve ardından **sıfırlama** kısayol menüsünde.

## <a name="visual-states-change-the-appearance-of-a-control-based-on-its-state"></a>Görsel durumlar: Kendi durumunu temel alan bir denetiminin görünüşünü değiştirme

Denetimlerin kullanıcı denetimine göre farklı görsel görünümlerini olabilir. Örneğin, bir kullanıcı buna tıkladığında veya bir animasyon çalıştırabileceğiniz yeşile bir düğme yapabilirsiniz. Kısaltır veya geçişleri kullanarak görsel durumlar arasındaki süreyi uzatabilir.

![Durum üzerinde fare](../designers/media/a95c671a-5639-40b9-83db-1e6b214330d5.png)

**Kısa bir video izleyin:** ![Yürüt düğmesi](../designers/media/bldadminconsoleinitialconfigicon.PNG) [WPF denetimleri durumunu yöneten](https://www.youtube.com/watch?v=m0PlkF5i6uw).

## <a name="resources-create-colors-styles-and-templates-and-reuse-them-later"></a>Kaynaklar: Renkleri, Stiller ve şablonlar oluşturma ve bunları daha sonra yeniden

Her şey, projenizdeki bir kaynağa dönüştürebilirsiniz. Farklı yerlerde uygulamanızda yeniden bir nesne bir kaynaktır. Örneğin, bir renk bir kez oluşturun, bir kaynak yapın ve ardından bu renk birkaç nesnelerinde kullanın. Tüm bu nesneleri rengini değiştirmek için renk kaynağı değiştirmeniz yeterlidir.

![Kaynak düğmeye renk Dönüştür](../designers/media/89203705-cf66-46e0-b153-52a23cd744f7.png) ![Renk kaynağı iletişim kutusu oluşturma](../designers/media/6bff8b19-3cd5-41a0-bbf9-ff65532d5aae.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio için Blend’i kullanarak kullanıcı arabirimi oluşturma](../designers/creating-a-ui-by-using-blend-for-visual-studio.md)